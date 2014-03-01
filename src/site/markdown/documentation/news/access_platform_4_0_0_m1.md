<head><title>AccessPlatform 4.0.0.M1</title></head>

# DataNucleus AccessPlatform 4.0.0.M1

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.0.M1 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_0_m1.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__1st March 2014__ - DataNucleus AccessPlatform 4.0.0.M1 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1116'>NUCCORE-1116</a>] -         SchemaTool : support create/delete of schema, and rename the current options to reflect that they only processes it for the input classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1124'>NUCCORE-1124</a>] -         Add ability to specify NamingFactory (non-RDBMS datastores)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1126'>NUCCORE-1126</a>] -         Add support to NamingFactory so that it can provide names for embedded member(s), including nested embedded members
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1129'>NUCCORE-1129</a>] -         Add persistence property to allow single connection to be used for a PM/EM, shared between transactional and nontransactional operations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1136'>NUCCORE-1136</a>] -         Provide method on StoreManager to remove knowledge of a class, so it can be reloaded (by such as JRebel)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-72'>NUCAPIJDO-72</a>] -         Add method to PMF to &quot;unmanage&quot; a class, allowing for it to be reloaded by such as JRebel
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-1'>NUCCASSANDRA-1</a>] -         Support basic CRUD operations (CassandraPersistenceHandler)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-2'>NUCCASSANDRA-2</a>] -         Support datastore-identity
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-4'>NUCCASSANDRA-4</a>] -         Support schema generation of tables/constraints
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-5'>NUCCASSANDRA-5</a>] -         Support schema generation of keyspace (create/drop)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-8'>NUCCASSANDRA-8</a>] -         Support &quot;increment&quot;/&quot;table&quot; value generator
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-9'>NUCCASSANDRA-9</a>] -         Support execution and in-memory evaluation of queries
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-11'>NUCCASSANDRA-11</a>] -         Support embedded PC fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-12'>NUCCASSANDRA-12</a>] -         Support serialised fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-13'>NUCCASSANDRA-13</a>] -         Support multitenancy by discriminator
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-14'>NUCCASSANDRA-14</a>] -         Support persistence of Enums
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-15'>NUCCASSANDRA-15</a>] -         Support persistence of Maps
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-19'>NUCCASSANDRA-19</a>] -         Support DDL with SchemaTool
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-708'>NUCRDBMS-708</a>] -         Add ability to create/drop a schema ultimately via SchemaTool
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-760'>NUCRDBMS-760</a>] -         Support transaction savepoint API, relaying call to JDBC Connection object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMAVEN-45'>NUCMAVEN-45</a>] -         Support SchemaTool &quot;createSchema&quot; and &quot;deleteSchema&quot; options
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1112'>NUCCORE-1112</a>] -         Make NucleusContext an interface, and have implementation(s) for the different contexts. Move static methods into a NucleusContextUtils
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1113'>NUCCORE-1113</a>] -         Improve efficiency of identity lookups to find class name that it equates to
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1128'>NUCCORE-1128</a>] -         Move store schema management operations to StoreSchemaHandler
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1141'>NUCCORE-1141</a>] -         StoreManager &quot;supportedOptions&quot; should be standardised in core rather than just text strings
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-17'>NUCCASSANDRA-17</a>] -         Make use of &quot;persistable-identity&quot; when storing relations to persistable objects
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-27'>NUCCASSANDRA-27</a>] -         Provide PreparedStatement caching since Cassandra doesn't
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-69'>NUCEXCEL-69</a>] -         Use &quot;persistable identity&quot; for storing references to persistable objects instead of &quot;id.toString()&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-71'>NUCEXCEL-71</a>] -         Support NUCCORE-1128 (move schema management into StoreSchemaHandler)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-43'>NUCJSON-43</a>] -         Use &quot;persistable identity&quot; for storing references to persistable objects instead of &quot;id.toString()&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-89'>NUCHBASE-89</a>] -         Support NUCCORE-1128 (move schema management into StoreSchemaHandler)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-139'>NUCMONGODB-139</a>] -         Use &quot;persistable identity&quot; for storing references to persistable objects instead of &quot;id.toString()&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-141'>NUCMONGODB-141</a>] -         Support NUCCORE-1128 (move schema management into StoreSchemaHandler)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-50'>NUCODF-50</a>] -         Use &quot;persistable identity&quot; for storing references to persistable objects instead of &quot;id.toString()&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-52'>NUCODF-52</a>] -         Support NUCCORE-1128 (move schema management into StoreSchemaHandler)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-757'>NUCRDBMS-757</a>] -         getClassNameForObjectID should check on number of concrete candidates, and return if just 1
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-759'>NUCRDBMS-759</a>] -         PostgreSQL : support detection of sequence existence using SELECT
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-763'>NUCRDBMS-763</a>] -         Support NUCCORE-1128 (move schema management into StoreSchemaHandler)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-767'>NUCRDBMS-767</a>] -         OSGi manifest contains old HSQLD driver import
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1109'>NUCCORE-1109</a>] -         Extend SchemaAwareStoreManager to allow for create/delete of an actual schema (where supported)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1110'>NUCCORE-1110</a>] -         Drop deprecated MetaDataManager method
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1111'>NUCCORE-1111</a>] -         Mark any class using &quot;DatastoreUniqueOID&quot; as not being L2 cacheable to avoid problems
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1114'>NUCCORE-1114</a>] -         Change MetaDataManager to be interface, and have MetaDataManagerImpl as implementation, extended by JDO/JPA APIs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1117'>NUCCORE-1117</a>] -         Clean up MetaDataManager interface
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1118'>NUCCORE-1118</a>] -         Rename StoreManager addClass, addClasses, removeAllClasses to better match their purpose
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1119'>NUCCORE-1119</a>] -         Remove use of persistence property &quot;datanucleus.metadata.validate&quot; - as deprecated some time back
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1120'>NUCCORE-1120</a>] -         NucleusContext should be responsible for loading up default properties appropriate to that context, not Configuration
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1122'>NUCCORE-1122</a>] -         Rename &quot;datanucleus.defaultInheritanceStrategy&quot; to &quot;datanucleus.metadata.defaultInheritanceStrategy&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1123'>NUCCORE-1123</a>] -         Change IndexMetaData/UniqueMetaData to not have child ColumnMetaData, just String column name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1125'>NUCCORE-1125</a>] -         Support NUCRDBMS-761 (rename to core/RDBMS plugin points)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1127'>NUCCORE-1127</a>] -         Refactor schema persistence properties to have standard naming &quot;datanucleus.schema.XXX&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1135'>NUCCORE-1135</a>] -         Change JDOImplementationCreator to use current JRE as default rather than 1.3!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1137'>NUCCORE-1137</a>] -         Add autoCreateSchema to add database schema if it doesn't exist (for datastores that support it)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1139'>NUCCORE-1139</a>] -         Add TypeConverter for BigDecimal-Double and BigInteger-Long for datastores that don't gave high precision types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1140'>NUCCORE-1140</a>] -         Add TypeConverter for sql.Date-Date, sql.Time-Date, and sql.Timestamp-Date for datastores that only support java.util.Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-68'>NUCAPIJDO-68</a>] -         Support NUCCORE-159
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-69'>NUCAPIJDO-69</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-70'>NUCAPIJDO-70</a>] -         Support NUCCORE-1114
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-71'>NUCAPIJDO-71</a>] -         JDO register process (class instantiation and JDOImplHelper) can register metadata but leave uninitialised
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-264'>NUCJPA-264</a>] -         Default &quot;datanucleus.allowAttachOfTransient&quot; to true for JPA
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-265'>NUCJPA-265</a>] -         Support NUCCORE-159
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-266'>NUCJPA-266</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-267'>NUCJPA-267</a>] -         Support NUCCORE-1114
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-15'>NUCREST-15</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-6'>NUCCASSANDRA-6</a>] -         Update AccessPlatform docs with Cassandra plugin info
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-16'>NUCCASSANDRA-16</a>] -         Add log utility to show CQL statements with ? replaced by value
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-20'>NUCCASSANDRA-20</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-22'>NUCCASSANDRA-22</a>] -         Support primitive wrappers
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-26'>NUCCASSANDRA-26</a>] -         Support java.util.TimeZone
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-68'>NUCEXCEL-68</a>] -         Support NUCCORE-1109
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-70'>NUCEXCEL-70</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-44'>NUCJSON-44</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-87'>NUCHBASE-87</a>] -         Support NUCCORE-1109
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-88'>NUCHBASE-88</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCLDAP-61'>NUCLDAP-61</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-138'>NUCMONGODB-138</a>] -         Support NUCCORE-1109
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-140'>NUCMONGODB-140</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-47'>NUCNEOFORJ-47</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEODATIS-29'>NUCNEODATIS-29</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-49'>NUCODF-49</a>] -         Support NUCCORE-1109
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-51'>NUCODF-51</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-753'>NUCRDBMS-753</a>] -         Support NUCCORE-1109
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-754'>NUCRDBMS-754</a>] -         Remove deprecated JDBCUtils code
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-755'>NUCRDBMS-755</a>] -         If DatastoreAdapter doesn't support catalog/schema then don't bother trying to find defaults from datastore connection
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-756'>NUCRDBMS-756</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-761'>NUCRDBMS-761</a>] -         Move RDBMS plugin point schema definitions from &quot;datanucleus-core&quot; plugin.xml
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-762'>NUCRDBMS-762</a>] -         NuoDB adapter updates
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCXML-53'>NUCXML-53</a>] -         Support NUCCORE-1112
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCXML-54'>NUCXML-54</a>] -         Add flexibility to ConnectionFactory to consider having different XSLT/DOM handlers
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-36'>NUCSPATIAL-36</a>] -         Remove ESRI/ArcGIS and Linar/Jintegra code since was never really ready for release, no docs and no tests
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-37'>NUCSPATIAL-37</a>] -         Drop OracleTypeInfo.SDO_GEOMETRY and move to geospatial
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-38'>NUCSPATIAL-38</a>] -         Support NUCRDBMS-761 (rename to core/RDBMS plugin points)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-6'>NUCGUAVA-6</a>] -         Support NUCRDBMS-761 (rename to core/RDBMS plugin points)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-17'>NUCJODATIME-17</a>] -         Support NUCRDBMS-761 (rename to core/RDBMS plugin points)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCACHE-38'>NUCCACHE-38</a>] -         Support NUCCORE-1112
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1115'>NUCCORE-1115</a>] -         TypeManager extraction of datastore type for a TypeConverter can fail when we are using an interface as the member type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1134'>NUCCORE-1134</a>] -         PrimaryKeyGenerator equals is incorrect in some situations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1138'>NUCCORE-1138</a>] -         L2 cache configuration not reset when getting ExecutionContext from pool
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-758'>NUCRDBMS-758</a>] -         Wrong SQL generated for bulk fetch for queries with order by
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-764'>NUCRDBMS-764</a>] -         Current handling of &quot;datanucleus.connection.nontx.releaseAfterUse=false&quot; is being applied to schema connections when shouldn't
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-765'>NUCRDBMS-765</a>] -         H2 DatastoreAdapter should have SEQUENCES as supported but doesn't currently
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-766'>NUCRDBMS-766</a>] -         ManagedConnection.getXAResource is always returning a new XAResource but should return the current resource
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-768'>NUCRDBMS-768</a>] -         ResultClassROF because of generate field $jacocoData
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCXML-55'>NUCXML-55</a>] -         Setting the 'indent-number' attribute is incompatible with some external XSLT libraries.
</li>
</ul>

