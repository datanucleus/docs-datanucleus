<head><title>Extensions : RDBMS Datatypes</title></head>

# Section : [Documentation](../index.html) > [Extensions](index.html)

## Extensions : RDBMS Datastore Types
![Plugin](../../images/nucleus_plugin.gif)

When persisting a class to an RDBMS datastore there is a _mapping_ process from class/field to table/column. The most common thing to configure is the 
[JavaTypeMapping](rdbms_java_types.html) so that it maps between the java type and the column(s) in the desired way. We can also configure the 
mapping to the datastore type. So, for example, we define what JDBC types we can map a particular Java type to. 
By "datastore type" we mean the JDBC type, such as BLOB, INT, VARCHAR etc. 
DataNucleus provides datastore mappings for the vast majority of JDBC types and the handlings will almost always be adequate. 
What you could do though is make a particular Java type persistable using a different JDBC type if you wished.


### Interface

To define your own datastore mapping you need to implement _org.datanucleus.store.rdbms.mapping.datastore.DatastoreMapping_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/store.rdbms/latest/org/datanucleus/store/rdbms/mapping/datastore/DatastoreMapping.html).


	public interface DatastoreMapping
	{
    	/**
    	 * Whether the field mapped is nullable.
    	 * @return true if is nullable
    	 */
    	boolean isNullable();
	
    	/**
    	 * The datastore field mapped.
    	 * @return the DatastoreField
    	 */
    	DatastoreField getDatastoreField();
	
    	/**
    	 * The mapping for the java type that this datastore mapping is used by.
    	 * This will return null if this simply maps a datastore field in the datastore and has
    	 * no associated java type in a class.
    	 * @return the JavaTypeMapping
    	 */
    	JavaTypeMapping getJavaTypeMapping();
	
    	/**
    	 * Accessor for whether the mapping is decimal-based.
    	 * @return Whether the mapping is decimal based
    	 */
    	boolean isDecimalBased();

    	/**
    	 * Accessor for whether the mapping is integer-based.
    	 * @return Whether the mapping is integer based
    	 */
    	boolean isIntegerBased();
	
    	/**
    	 * Accessor for whether the mapping is string-based.
    	 * @return Whether the mapping is string based
    	 */
    	boolean isStringBased();
	
    	/**
    	 * Accessor for whether the mapping is bit-based.
    	 * @return Whether the mapping is bit based
    	 */
    	boolean isBitBased();
	
    	/**
    	 * Accessor for whether the mapping is boolean-based.
    	 * @return Whether the mapping is boolean based
    	 */
    	boolean isBooleanBased();
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setBoolean(Object preparedStatement, int paramIndex, boolean value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setChar(Object preparedStatement, int paramIndex, char value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setByte(Object preparedStatement, int paramIndex, byte value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setShort(Object preparedStatement, int paramIndex, short value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setInt(Object preparedStatement, int paramIndex, int value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
     	 */
    	void setLong(Object preparedStatement, int paramIndex, long value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setFloat(Object preparedStatement, int paramIndex, float value);

    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setDouble(Object preparedStatement, int paramIndex, double value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
     	 * @param value the value
    	 */
    	void setString(Object preparedStatement, int paramIndex, String value);
	
    	/**
    	 * Sets a <code>value</code> into <code>preparedStatement</code> 
    	 * at position specified by <code>paramIndex</code>. 
    	 * @param preparedStatement a datastore object that executes statements in the database 
    	 * @param paramIndex the position of the value in the statement
    	 * @param value the value
    	 */
    	void setObject(Object preparedStatement, int paramIndex, Object value);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	boolean getBoolean(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	char getChar(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	byte getByte(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	short getShort(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
     	 * @param resultSet an object returned from the datastore with values 
     	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	int getInt(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	long getLong(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	float getFloat(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	double getDouble(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	String getString(Object resultSet, int exprIndex);
	
    	/**
    	 * Obtains a value from <code>resultSet</code> 
    	 * at position specified by <code>exprIndex</code>. 
    	 * @param resultSet an object returned from the datastore with values 
    	 * @param exprIndex the position of the value in the result
    	 * @return the value
    	 */
    	Object getObject(Object resultSet, int exprIndex);
	}

So you can define how to convert the datastore column value to/from common Java types. Please refer to the existing types in 
Look at [datanucleus-rdbms](https://github.com/datanucleus/datanucleus-rdbms/tree/master/src/java/org/datanucleus/store/rdbms/mapping/datastore)
for examples. Note that your XXXDatastoreMapping should have a single constructor taking in 
_JavaTypeMapping mapping, StoreManager storeMgr, Column col_.

### Plugin Specification

To give an example of what the plugin specification looks like

	<?xml version="1.0"?>
	<plugin id="mydomain.myplugins" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.store.rdbms.rdbms_mapping">
        	<mapping java-type="java.lang.Character" 
            	rdbms-mapping-class="org.datanucleus.store.rdbms.mapping.datastore.CharRDBMSMapping" 
            	jdbc-type="CHAR" sql-type="CHAR" default="true"/>
        	<mapping java-type="java.lang.Character" 
            	rdbms-mapping-class="org.datanucleus.store.rdbms.mapping.datastore.IntegerRDBMSMapping" 
            	jdbc-type="INTEGER" sql-type="INT" default="false"/>
    	</extension>
	</plugin>

Note that you also require a MANIFEST.MF file as per the [Extensions Guide](index.html).
So in this definition we have defined that a field of type "Character" can be mapped to JDBC type of CHAR or INTEGER (with CHAR the default)


### Missing JDBC definitions

While DataNucleus attempts to provide all useful JDBC type mappings out of the box, occasionally
you may come across one that is not defined, even though we provide an RDBMSMapping class for that
JDBC type. For example, if you got this error message

	JDBC type XXX declared for field "org.datanucleus.test.MyClass.yyyField" of java type java.lang.YYY cant be mapped for this datastore.


This means that while the JDBC driver may support this JDBC type, we haven't defined it for the java type "YYY" in the _plugin.xml_ file. 
All that you need to do is add a _plugin.xml_

	<?xml version="1.0"?>
	<plugin id="mydomain.myplugins" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.store.rdbms.rdbms_mapping">
        	<mapping java-type="java.lang.YYY" 
            	rdbms-mapping-class="org.datanucleus.store.rdbms.mapping.XXXRDBMSMapping" 
            	jdbc-type="XXX" sql-type="XXX" default="false"/>
    	</extension>
	</plugin>

together with MANIFEST.MF to your application, and it will be supported. Obviously if it is of
a type that you think we ought to support out-of-the-box then raise a JIRA on project "NUCRDBMS"
with your plugin.xml definition and mention the datastore it was needed for.
