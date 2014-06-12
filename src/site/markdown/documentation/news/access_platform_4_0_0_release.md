<head><title>AccessPlatform 4.0.0.RELEASE</title></head>

# DataNucleus AccessPlatform 4.0.0.RELEASE

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.0.RELEASE Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_0_release.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__13th June 2014__ - DataNucleus AccessPlatform 4.0.0.RELEASE ("Einstein") is released.
DataNucleus AccessPlatform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, Cassandra, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


DataNucleus AccessPlatform 4.0 includes the following features relative to version 3.3

<ul>
<li>Java 1.8 : Upgrade to ASM v5 to allow for Java 1.8 bytecode changes</li>
<li>Java 1.8 : support for the majority of java.time types</li>
<li>Changed the bytecode enhancement contract to use an internal definition rather than the JDO contract</li>
<li>JPA : no longer needs to have jdo-api.jar present</li>
<li>Cassandra : support for Cassandra 1.2+</li>
<li>Support for multicolumn TypeConverters (used by RDBMS, Cassandra, Excel, ODF, Neo4j, MongoDB, JSON, HBase)</li>
<li>SchemaTool : support for create/delete of a schema (where the datastore supports it)</li>
<li>RDBMS : support for HikariCP and DBCP2 connection pools</li>
<li>RDBMS : ability to use single connection per PM/EM (rather than 1 for transactional operations, and 1 for non-transactional operations)</li>
<li>RDBMS : removed the need to create JavaTypeMapping classes when the user type has a TypeConverter</li>
<li>JSON : support for embedded 1-1 relation fields/properties</li>
<li>Excel/ODF/JSON/MongoDB/Neo4j/HBase/Cassandra : move to using "core" definition of table/columns meaning access to generalised features tested on other datastores</li>
</ul>


This release includes the following changes over the previous release (4.0.0.M4)

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-147'>NUCMONGODB-147</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-94'>NUCHBASE-94</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-50'>NUCNEOFORJ-50</a>] -         Support multicolumn TypeConverters
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1223'>NUCCORE-1223</a>] -         org.datanucleus.store.StoreData should have Table field since many store plugins use this now and we should encourage it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1227'>NUCCORE-1227</a>] -         UUIDStringConverter should implement ColumnLengthDefiningTypeConverter and set length to 36
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-802'>NUCRDBMS-802</a>] -         Change org.datanucleus.store.rdbms.table.Table to extend org.datanucleus.store.schema.table.Table
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-39'>NUCSPATIAL-39</a>] -         Formatting ol files with the latest Datanucleus code convention xml.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-50'>NUCSPATIAL-50</a>] -         JDK 1.8 related javadoc enhancements needed
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1121'>NUCCORE-1121</a>] -         Remove AbstractMemberMetaData.getColumn since deprecated for some time
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1221'>NUCCORE-1221</a>] -         NamingFactory getIndexName() methods should be renamed to getConstraintName() so we can use for unique constraint and FK constraint also
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1222'>NUCCORE-1222</a>] -         Change ForeignKeyMetaData to extend ConstraintMetaData
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1224'>NUCCORE-1224</a>] -         Refactor Table.getIdentifier -&gt; Table.getName, Column.getIdentifier -&gt; Column.getName
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1225'>NUCCORE-1225</a>] -         Update JdbcType to use ordinal as the java.sql.Types value allowing lookup in RDBMS
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1226'>NUCCORE-1226</a>] -         Add persistence property to set the preference for embedding of a PC object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1228'>NUCCORE-1228</a>] -         CompleteClassTable should add &quot;column&quot; for nested array/map holder
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-77'>NUCEXCEL-77</a>] -         Remove need for SchemaVerifierImpl since does nothing currently anyway
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-58'>NUCODF-58</a>] -         Remove need for SchemaVerifierImpl since does nothing currently anyway
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-146'>NUCMONGODB-146</a>] -         Change schema management to use org.datanucleus.store.schema.table.Table
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-85'>NUCHBASE-85</a>] -         HTablePool is deprecated in HBase 0.94.11, 0.95.2 onwards
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-93'>NUCHBASE-93</a>] -         Change schema management to use org.datanucleus.store.schema.table.Table
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-95'>NUCHBASE-95</a>] -         Use column name from Table/Column structure and extract familyName/qualifierName from that name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-52'>NUCJSON-52</a>] -         Remove need for SchemaVerifierImpl since does nothing currently anyway
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-49'>NUCNEOFORJ-49</a>] -         Use generic Table/Column code for Node/property namings and ditch ad-hoc code
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-803'>NUCRDBMS-803</a>] -         Refactor some of the method names around DatastoreIdentifier, Table, Column to make more logical to casual reader
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-804'>NUCRDBMS-804</a>] -         Enable TypeConverterMapping.getDefaultLength to use converter length (when defined)
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1204'>NUCCORE-1204</a>] -         Object is left in 2nd level cache when commit() fails
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-13'>NUCJAVAEIGHT-13</a>] -         Typoe in plugin.xml for InstantLongConverter
</li>
</ul>

