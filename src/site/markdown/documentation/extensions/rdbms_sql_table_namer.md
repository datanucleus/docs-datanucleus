<head><title>Extensions : RDBMS SQL Table Namer</title></head>

## Extensions : RDBMS SQL Table Naming Support
![Plugin](../../images/nucleus_plugin.gif)

DataNucleus is developed as a plugin-driven framework and one of the components that is 
pluggable is the support for controlling the naming of table aliases in (some) SQL statements.
DataNucleus provides a few options out of the box.
The default is _alpha-scheme_ which names tables based on the table-group they are in
and the number in that group, so giving names like A0, A1, A2, B0, B1, C0, D0.
It also provides a simpler option <i>t-scheme</i> that names all tables as "T{number}" so T0, T1, T2, T3, etc.

The following sections describe how to create your own SQL Table Namer plugin for DataNucleus.

### Interface

Any SQL Table Namer plugin will need to implement _org.datanucleus.store.rdbms.sql.SQLTableNamer_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/store.rdbms/latest/org/datanucleus/store/rdbms/sql/SQLTableNamer.html).
So you need to implement the following interface

	package org.datanucleus.store.rdbms.sql;
	
	import org.datanucleus.store.rdbms.sql.SQLStatement;
	import org.datanucleus.store.mapped.DatastoreContainerObject;
	
	public interface SQLTableNamer
	{
    	/**
    	 * Method to return the alias to use for the specified table.
    	 * @param stmt The statement where we will use the table
    	 * @param table The table
    	 * @return The alias to use
    	 */
    	public String getAliasForTable(SQLStatement stmt, DatastoreContainerObject table);
	}

### Implementation

So there is only one method to provide in your implementation. The arguments to this are

* The SQLStatement that is being constructed and that we create the names for
* The table that we want to generate the alias for

Lets just go through our default namer scheme to understand how it works

	package mydomain;
	
	import org.datanucleus.store.rdbms.sql.SQLTableNamer;
	import org.datanucleus.store.rdbms.sql.SQLStatement;
	import org.datanucleus.store.mapped.DatastoreContainerObject;
	
	public class MySQLTableNamer implements SQLTableNamer
	{
    	public String getAliasForTable(SQLStatement stmt, DatastoreContainerObject table)
    	{
        	if (stmt.getPrimaryTable() == null)
        	{
            	return "T0";
        	}
        	else
        	{
            	return "T" + (stmt.getNumberOfTables() < 0 ? "1" : (stmt.getNumberOfTables()+1));
        	}
    	}
	}

So we simply name the primary table of the statement as "T0", and then all subsequent
tables based on the number of the table. That was hard!

### Plugin Specification

So we now have our custom SQL method and we just need to make this into a DataNucleus plugin. To do this you simply add a file 
_plugin.xml_ to your JAR at the root. The file _plugin.xml_ should look like this


	<?xml version="1.0"?>
	<plugin id="mydomain" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.store.rdbms.sql_tablenamer">
        	<sql-tablenamer name="my-t-scheme" class="mydomain.MySQLTableNamer"/>
    	</extension>
	</plugin>

Note that you also require a MANIFEST.MF file as per the [Extensions Guide](index.html).

So now if we define a query using the extension _datanucleus.sqlTableNamingStrategy_ set to "my-t-scheme" then it will use our table namer.
