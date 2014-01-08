<head><title>Extensions : RDBMS SQL Operations</title></head>

# Section : [Documentation](../index.html) > [Extensions](index.html)

## Extensions : RDBMS SQL Expression Support
![Plugin](../../images/nucleus_plugin.gif)

DataNucleus is developed as a plugin-driven framework and one of the components that is 
pluggable is the support for JDOQL/JPQL expressions for java types in the "new" query mechanism.
When you add support for a new java type, if you want to query fields of that type you will need to provide this.

While you can define details of how your type is queryable, we only document here what you would do
for a type that is mapped to a String (since that's the most common use-case). Here you simply
need to add an entry into _plugin.xml_ defining which expression and literal class you would use for handling that type.


### Plugin Specification

Say we have a java type that is mapped using _mydomain.MyTypeMapping_.
Simply add a file _plugin.xml_ to your JAR at the root, and it should look like this

	<?xml version="1.0"?>
	<plugin id="mydomain" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.store.rdbms.sql_expression">
        	<sql-expression mapping-class="mydomain.MyTypeMapping" 
            	literal-class="org.datanucleus.store.rdbms.sql.expression.StringLiteral"
            	expression-class="org.datanucleus.store.rdbms.sql.expression.StringExpression"/>
    	</extension>
	</plugin>

Note that you also require a MANIFEST.MF file as per the [Extensions Guide](index.html).
