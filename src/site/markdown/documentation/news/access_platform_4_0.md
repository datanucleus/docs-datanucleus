<head><title>AccessPlatform 4.0</title></head>

#Release Notes for DataNucleus AccessPlatform v4.0

The 4.0 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 4.0_ includes the following over 3.2/3.3

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

<br/>

# DataNucleus AccessPlatform 4.0.6

__Mar 1st 2015__ : _Version 4.0.6_ includes the following changes

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1273'>NUCCORE-1273</a>] -         Support for NUCRDBMS-848 for DN 4.0
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1274'>NUCCORE-1274</a>] -         Support CASE / IF/ELSE &quot;when&quot; conditions that are not completely defined (i.e depend on previous when conditions)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-854'>NUCRDBMS-854</a>] -         Support NUCCORE-1274
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-848'>NUCRDBMS-848</a>] -         &quot;max&quot; value generator provides wrong id if 2 objects are persisted in one transaction  
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-856'>NUCRDBMS-856</a>] -         ViewImpl seems to have regression in validate() method
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-81'>NUCEXCEL-81</a>] -         Numeric object wrapper fields can fail on retrieval due to falling back to TypeConverter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-82'>NUCEXCEL-82</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-84'>NUCEXCEL-84</a>] -         Persist of object with composite PK results in blank row in worksheet before the next inserted object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-61'>NUCODF-61</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.5

__Feb 2nd 2015__ : _Version 4.0.5_ includes the following changes

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-845'>NUCRDBMS-845</a>] -         Handling of case expression should check for non-Boolean conditional expression, and convert to CaseNumericExpression if possible
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-852'>NUCRDBMS-852</a>] -         Support query fetch of Collection/Map/Array fields when serialised (i,e stored in single column of owner table).
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-851'>NUCRDBMS-851</a>] -         Add check on CASE &quot;action&quot; expression types for consistency
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-847'>NUCRDBMS-847</a>] -         JDOQL statement with multi-tenant PersistenceManager
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-151'>NUCMONGODB-151</a>] -         JDOQL COUNT query fails for unknown classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCLDAP-66'>NUCLDAP-66</a>] -         AttributeStrategy : When reassigning N-1 owner, allow for new owner not yet being persistent
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-80'>NUCEXCEL-80</a>] -         Make sure StoreData is populated before using fetchObject(...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-60'>NUCODF-60</a>] -         Make sure StoreData is populated before using fetchObject(...)
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.4

__Nov 15th 2014__ : _Version 4.0.4_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCLDAP-63'>NUCLDAP-63</a>] -         Add ability to specify &quot;mapping-strategy&quot; for a field without relying on random &quot;join&quot; information
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1262'>NUCCORE-1262</a>] -         Simplify Invalid[Class/Member]MetaDataException constructor to just take in params list and no class/member name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCLDAP-64'>NUCLDAP-64</a>] -         StoreFieldManager/FetchFieldManager create an instance of mapping strategy for every objects instance of every basic field!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-838'>NUCRDBMS-838</a>] -         Start restructuring of ClassAdder to allow easier updates/locking in the future
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1257'>NUCCORE-1257</a>] -         AbstractMetaData population moving of ColumnMetaData to element/value when using collection/map is incomplete, should MOVE not COPY
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1259'>NUCCORE-1259</a>] -         AbstractConnectionFactory/ConnectionFactory should have factoryName and resourceType and not use &quot;options&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1261'>NUCCORE-1261</a>] -         Backing store wrappers don't need to hold &quot;queued&quot; property
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1258'>NUCCORE-1258</a>] -         transaction options is lost, leading to ISOLATION LEVEL violation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-80'>NUCAPIJDO-80</a>] -         JDOPersistenceManagerFactory.getPersistenceManagerFactory(Map overridingProps) doesn't cater for people abusing API of java.util.Properties
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-60'>NUCCASSANDRA-60</a>] -         Make sure resultObjects in CassandraQueryResults are dereferenced
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-792'>NUCRDBMS-792</a>] -         Map.containsKey generates invalid query
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.3

__Oct 2nd 2014__ : _Version 4.0.3_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-283'>NUCJPA-283</a>] -         Expose access to the underlying connection, so people can perform native operations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-285'>NUCJPA-285</a>] -         Allow EntityManager.createNativeQuery to create a query using a non-SQL query language
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-21'>NUCCASSANDRA-21</a>] -         Support native Cassandra CQL queries
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1256'>NUCCORE-1256</a>] -         Extend NUCCORE-1233 support for JDOQL &quot;IF ... ELSE IF ... ELSE ...&quot; to require final ELSE or throw exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-730'>NUCRDBMS-730</a>] -         Persist of M-N relation can be inefficient; currently always does SELECT to see if present then INSERT.
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1248'>NUCCORE-1248</a>] -         NamingFactory.getConstraintName for member should also pass in the class name so we can name indexes when part of table for subclasses
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1249'>NUCCORE-1249</a>] -         Drop SCOMtoN since we can just check if it is M-N relation or if collection
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1250'>NUCCORE-1250</a>] -         Add method to MetaDataManager that returns the enhanced method name prefix (i.e &quot;dn&quot;)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1253'>NUCCORE-1253</a>] -         Move identity conversion handling into core from api.jdo/api.jpa
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1255'>NUCCORE-1255</a>] -         Add method for what query language is considered &quot;native&quot; for a store
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-79'>NUCAPIJDO-79</a>] -         Add Transaction set/getNontransactionalWriteAutoCommit
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-282'>NUCJPA-282</a>] -         Support @ConstructorResult
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-58'>NUCCASSANDRA-58</a>] -         Support NUCCORE-1248
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-59'>NUCCASSANDRA-59</a>] -         Support NUCCORE-1255
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-150'>NUCMONGODB-150</a>] -         Support NUCCORE-1248
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-827'>NUCRDBMS-827</a>] -         Support constructor mappings in SQL query results
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-833'>NUCRDBMS-833</a>] -         Support NUCCORE-1255
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1252'>NUCCORE-1252</a>] -         ByteArrayByteBufferConverter toMemberType ByteBuffer to byte[] conversion fails
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1254'>NUCCORE-1254</a>] -         Backed SCO wrappers should not add operations to queue when the owner object is not yet inserted
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-281'>NUCJPA-281</a>] -         CriteriaQuery needs to respect any distinct specified on &quot;select&quot; but currently ignores it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-57'>NUCCASSANDRA-57</a>] -         JPQLQuery should have latest candidate class code (copy from HBase for example)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-829'>NUCRDBMS-829</a>] -         Embedded object causes: IllegalArgumentException: out of field index
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-830'>NUCRDBMS-830</a>] -         ResultClassROF can throw exception if it finds an enhancement method in the result class of a query
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-831'>NUCRDBMS-831</a>] -         RDBMSStoreManager generates comments which are bad syntax in Mysql
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-832'>NUCRDBMS-832</a>] -         Persist of object with Collection (via join table) containing some new and some detached elements doesn't create the join table entries
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.2

__Aug 29th 2014__ : _Version 4.0.2_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-814'>NUCRDBMS-814</a>] -         Support maxActive on DBCP2 connection pool
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-823'>NUCRDBMS-823</a>] -         SQLite only supports &quot;autoincrement&quot; on INTEGER columns, so should default to that
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-824'>NUCRDBMS-824</a>] -         Fields should be ordered by name in insert statement generation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-826'>NUCRDBMS-826</a>] -         Move org.datanucleus.store.rdbms.datasource.DriverManagerDataSource to inner class of DefaultConnectionPoolFactory
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1241'>NUCCORE-1241</a>] -         Support result set value conversion from Long/Integer to Boolean in ClassUtils.convertValue
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1242'>NUCCORE-1242</a>] -         Fix ByteBuffer converters to handle null input/output
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1245'>NUCCORE-1245</a>] -         JDO &quot;persistence-capable-superclass&quot; metadata was deprecated in JDO2. Remove it since we use reflection anyway
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-275'>NUCJPA-275</a>] -         Throw NoPersistenceUnitException when not found in creation of EMF via PersistenceProvider
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-280'>NUCJPA-280</a>] -         Enable close of query results at ExecutionContext close
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-52'>NUCNEOFORJ-52</a>] -         Upgrade to Neo4j 2.1
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1243'>NUCCORE-1243</a>] -         OSGI classloading problem
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1246'>NUCCORE-1246</a>] -         TypeConverter cannot use basic inheritance
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-277'>NUCJPA-277</a>] -         Annotation attribute for @Index &quot;unique&quot; is being used incorrectly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-278'>NUCJPA-278</a>] -         Some types of fields are setting allowsNull as false when shouldn't, dependent on annotations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-779'>NUCRDBMS-779</a>] -         Without explicit commit, fetching multiple results fails with Firebird
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-790'>NUCRDBMS-790</a>] -         Boolean fields are left as null when selecting objects using SQL query
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-815'>NUCRDBMS-815</a>] -         NullPointerException when setting multiple Date parameters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-816'>NUCRDBMS-816</a>] -         Incorrect handling of join expressions when using multiple joins
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-817'>NUCRDBMS-817</a>] -         Using Collection with class (Discriminator.value_map) with no subclasses (i.e redundant discriminator)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-818'>NUCRDBMS-818</a>] -         Schema Tool throws NullPointerException when @Index name does not match a field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-819'>NUCRDBMS-819</a>] -         HSQL getSecond returns Integer/Decimal depending on millisecs, so should cast to INTEGER
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-820'>NUCRDBMS-820</a>] -          PostgreSQL getSecond returns Integer/Decimal depending on millisecs, so should cast to INTEGER
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-821'>NUCRDBMS-821</a>] -         SQLTableAlphaNamer doesn't check for lowercase when looking for name clashes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-822'>NUCRDBMS-822</a>] -         possible bug in org.datanucleus.store.rdbms.mapping.datastore.BigIntRDBMSMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-15'>NUCJAVAEIGHT-15</a>] -         HSQL getSecond returns Integer/Decimal depending on millisecs, so should cast to INTEGER
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-16'>NUCJAVAEIGHT-16</a>] -         Persist of LocalDateTime/LocalTime is not setting nanos
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-17'>NUCJAVAEIGHT-17</a>] -         PostgreSQL getSecond returns Integer/Decimal depending on millisecs, so should cast to INTEGER
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.1

__Jul 19th 2014__ : _Version 4.0.1_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1233'>NUCCORE-1233</a>] -         Support JDOQL compilation of &quot;IF (expr) expr ELSE IF (expr) expr ELSE expr&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-56'>NUCCASSANDRA-56</a>] -         Adding support for uuid datastoreType of Cassandra
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-96'>NUCHBASE-96</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-78'>NUCEXCEL-78</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-59'>NUCODF-59</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-53'>NUCJSON-53</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-148'>NUCMONGODB-148</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-807'>NUCRDBMS-807</a>] -         Support mapping java.util.UUID to PostgreSQL native &quot;uuid&quot; column type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-810'>NUCRDBMS-810</a>] -         Support for TIME and DATE JDBC data types for MS SQL Server 2008 and newer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-51'>NUCNEOFORJ-51</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-59'>NUCODF-59</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-14'>NUCJAVAEIGHT-14</a>] -         Provide Java8 variants of Collection/Map wrappers so that any new methods can be supported.
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1237'>NUCCORE-1237</a>] -         CompleteClassTable should check for columns with same name in the table and throw an exception
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1230'>NUCCORE-1230</a>] -         Upgrade ASM to 5.0.3
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1231'>NUCCORE-1231</a>] -         Add basic support for temporal literals as Strings
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1236'>NUCCORE-1236</a>] -         Support update of L2 cache when refresh() is called
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-805'>NUCRDBMS-805</a>] -         Add simple handling of temporal literal as String
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-806'>NUCRDBMS-806</a>] -         Mappings for Oracle should be merged into org.datanucleus.store.rdbms.mapping.[java|datastore]
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1235'>NUCCORE-1235</a>] -         RDBMSStoreManager.addSchemaCallback does not populate the schemaCallbacks correctly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1239'>NUCCORE-1239</a>] -         1-1 Birdirecional relation management fails when using optimistic tx
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-78'>NUCAPIJDO-78</a>] -         Creation of implementation of persistent abstract class / interface creates metadata with full name (including package)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-274'>NUCJPA-274</a>] -         NamedStoredProcedureQueries doesn't set procedure name on processed stored procs metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-55'>NUCCASSANDRA-55</a>] -         Could not serialize byte[] @Serialized member on Cassandra store
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-79'>NUCEXCEL-79</a>] -         SchemaTool doesn't make full use of generalised Table; should create CompleteClassTable when not present
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-149'>NUCMONGODB-149</a>] -         SchemaTool doesn't make full use of generalised Table; should create CompleteClassTable when not present
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-808'>NUCRDBMS-808</a>] -         Datanucleus can't find sequence in PostrgreSQL when persistence property 'datanucleus.identifier.case' is set
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-809'>NUCRDBMS-809</a>] -         Inconsistent behavior in enum value conversion to/from numeric value in RDBMS using 'enum-value-getter' extension
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-811'>NUCRDBMS-811</a>] -         Enum extension &quot;enum-check-constraint&quot; is incorrectly handled if also using extension &quot;enum-value-getter&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-812'>NUCRDBMS-812</a>] -         When executing StoredProcedure with multiple result sets, the close of the first results will close the statement!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-813'>NUCRDBMS-813</a>] -         1-N FK bidir relationship management failing when using optimistic tx
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.0.RELEASE

__Jun 13th 2014__ : _Version 4.0 RELEASE_ includes the following changes

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

<br/>


# DataNucleus AccessPlatform 4.0.0.M4

__May 29th 2014__ : _Version 4.0 Milestone 4_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1216'>NUCCORE-1216</a>] -         Allow option of Query results being closed when ExecutionContext is closed
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-49'>NUCCASSANDRA-49</a>] -         Support schema creation &quot;USING&quot; options via metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-11'>NUCJAVAEIGHT-11</a>] -         Add support for Instant persisted as Long (numeric)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-12'>NUCJAVAEIGHT-12</a>] -         Support for OffsetTime, OffsetDateTime
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1203'>NUCCORE-1203</a>] -         Logging around transactional cache enlist/evict is far from optimum and can just show evictions
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1208'>NUCCORE-1208</a>] -         Transaction cache cpu improvement
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1209'>NUCCORE-1209</a>] -         Constructor cache in IdentityManagerImpl
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1210'>NUCCORE-1210</a>] -         Configuration.getManagerOverrideableProperties() costs quite a lot of cpu during ExecutionContext creation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1212'>NUCCORE-1212</a>] -         Change Localisation sub-system to allow each plugin to register its bundle, and specify language/errorCodes via System properties
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1213'>NUCCORE-1213</a>] -         Cache frequently accessed properties in fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1214'>NUCCORE-1214</a>] -         Cache populated ClassMetadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1215'>NUCCORE-1215</a>] -         org.datanucleus.store.types.SCO should be genericised with the java type it represents
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1217'>NUCCORE-1217</a>] -         Refactor ExecutionContext callback handler method names to make clearer their usage
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1219'>NUCCORE-1219</a>] -         Add method to AbstractJavaQuery to compile the query to get just the generic compilation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-75'>NUCAPIJDO-75</a>] -         Decrease lock contention during PersistenceManager.close()
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1195'>NUCCORE-1195</a>] -         Upgrade ASM to 5.0.2
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1196'>NUCCORE-1196</a>] -         Make StoreManager.getStrategyForNative public
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1197'>NUCCORE-1197</a>] -         Various ApiAdapter methods are now no longer needed since we use a DataNucleus-centric enhancement contract
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1198'>NUCCORE-1198</a>] -         Drop org.datanucleus.metadata.PersistenceFlags, now part of Persistable interface
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1200'>NUCCORE-1200</a>] -         ExecutionContext.newQuery is not needed and all queries should be instantiated via QueryManager
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1201'>NUCCORE-1201</a>] -         Move query language name conversion to JDO API layer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1205'>NUCCORE-1205</a>] -         Add accessor for the StoreManager for the managed object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1206'>NUCCORE-1206</a>] -         Add TypeConverter for Calendar to (millis, timezone)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1207'>NUCCORE-1207</a>] -         Collection wrappers (with backing store) should likely throw IllegalXXXException when add() fails in the datastore
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1211'>NUCCORE-1211</a>] -         Change QueryManager to be interface, with default implementation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1218'>NUCCORE-1218</a>] -         org.datanucleus.metadata.FieldRole should be enum to give type safety
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-271'>NUCJPA-271</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-273'>NUCJPA-273</a>] -         JPAAnnotationReader has line which sets jdbcType of all boolean fields to SMALLINT. No reason why we need this so disable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-74'>NUCAPIJDO-74</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-794'>NUCRDBMS-794</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-796'>NUCRDBMS-796</a>] -         Change default Calendar persistence to single column (timestamp)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-798'>NUCRDBMS-798</a>] -         PostgreSQL : support OFFSET/FETCH for ranges
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-799'>NUCRDBMS-799</a>] -         PostgreSQL : add dummy BOOLEAN JDBC type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-801'>NUCRDBMS-801</a>] -         PostgreSQL : add dummy TINYINT JDBC type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEODATIS-30'>NUCNEODATIS-30</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCESS-128'>NUCACCESS-128</a>] -         Migrate projects to standard maven 2 layout
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCESS-129'>NUCACCESS-129</a>] -         Release own version of javax.persistence jar and remove use of EclipseLink JPA API jar
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1199'>NUCCORE-1199</a>] -         Improve logic for transient id handling to check for null
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1202'>NUCCORE-1202</a>] -         Missing release resource in non-tx handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-270'>NUCJPA-270</a>] -         JPA spec 2.10.3.1 requires a unique constraint on a OneToOne unidir relation by default
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-272'>NUCJPA-272</a>] -         Query.getParameter methods using position return that parameter is not found for JPQL
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-795'>NUCRDBMS-795</a>] -         Query with aggreg.function on single-column calendar field doesn't work due to wrong metadata handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-797'>NUCRDBMS-797</a>] -         MSSQL OFFSET is not optional when using FETCH
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.0.M3

__Apr 27th 2014__ : _Version 4.0 Milestone 3_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-74'>NUCEXCEL-74</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-7'>NUCCASSANDRA-7</a>] -         Support in-datastore querying of primary JDOQL/JPQL operations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-47'>NUCCASSANDRA-47</a>] -         Support schema evolution (new columns, delete columns)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-47'>NUCJSON-47</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-50'>NUCJSON-50</a>] -         Supported embedded 1-1 fields stored as nested in the JSON object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-55'>NUCODF-55</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-9'>NUCJAVAEIGHT-9</a>] -         Support LocalTime, LocalDate, LocalDateTime getSecond, getMinute, getHour, getDayOfMonth, getMonth, getYear in in-memory query evaluation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-10'>NUCJAVAEIGHT-10</a>] -         Support getHour, getMinute, getSecond, getYear, getMonthValue, getDayOfMonth method invocation on LocalXXX classes with RDBMS
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-922'>NUCCORE-922</a>] -         JPA : Enhance classes to implement org.datanucleus.enhancer.Persistable to avoid dependency on JDO
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1097'>NUCCORE-1097</a>] -         Genericise ExecutionContext/ObjectProvider interfaces
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1175'>NUCCORE-1175</a>] -         Rename &quot;org.datanucleus.store.types.simple&quot; to &quot;org.datanucleus.store.types.wrappers&quot;, and &quot;org.datanucleus.store.types.backed&quot; to &quot;org.datanucleus.store.types.wrappers.backed&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1176'>NUCCORE-1176</a>] -         Add TypeConverters for converting Boolean to &quot;Y&quot;/&quot;N&quot; and 1,0
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1181'>NUCCORE-1181</a>] -         JDOQL/JPQL : add compiler checks for use of aggregate in result clause with incorrect arguments
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1186'>NUCCORE-1186</a>] -         ValueGeneration class is pointless and should be removed
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-73'>NUCAPIJDO-73</a>] -         Support NUCCORE-922 (change bytecode enhancement contract)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-269'>NUCJPA-269</a>] -         Support NUCCORE-922 (change bytecode enhancement contract)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-48'>NUCJSON-48</a>] -         javadoc improvements according to JDK1.8 warning and errors
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-782'>NUCRDBMS-782</a>] -         Add Expression/Literal for handling TypeConverterMapping so we can avoid having to create Expression/Literal (and hence XXXMapping) for more types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-8'>NUCJAVAEIGHT-8</a>] -         Refactor so that root package is org.datanucleus.store.types.java8
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-20'>NUCJODATIME-20</a>] -         Refactor so that root package is org.datanucleus.store.types.jodatime
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-8'>NUCGUAVA-8</a>] -         Refactor so that root package is org.datanucleus.store.types.guava
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-934'>NUCCORE-934</a>] -         Restrict all references to PersistenceCapable/Detachable to isolated packages
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1173'>NUCCORE-1173</a>] -         Remove checks on &quot;stackmapFrames&quot; since we are using JDK 1.7+ now
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1174'>NUCCORE-1174</a>] -         Upgrade to javax.cache v1.0.0 now that final is out
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1177'>NUCCORE-1177</a>] -         Rename &quot;org.datanucleus.query.evaluator.memory&quot; to &quot;org.datanucleus.query.inmemory&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1178'>NUCCORE-1178</a>] -         Names of in-memory query evaluators are too verbose
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1180'>NUCCORE-1180</a>] -         Add StoreManager.OPTION_ORM_EMBEDDED_PC_NESTED to signify that the store supports embedding an object nested in the owner object (like JSON)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1182'>NUCCORE-1182</a>] -         Split runReachability out of ObjectProvider so that ReachabilityFieldManager is the only place we provide the pbr-at-commit process
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1183'>NUCCORE-1183</a>] -         Move NullCallbackHandler to org.datanucleus.state
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1184'>NUCCORE-1184</a>] -         Move ObjectProvider.nullifyFields() to ExecutionContextImpl reachability at commit code
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1185'>NUCCORE-1185</a>] -         org.datanucleus.query.node adds no value and should be merged into org.datanucleus.query.compiler
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1187'>NUCCORE-1187</a>] -         ExecutionContext newObjectProviderForEmbedded are simply relays and should be removed; use ObjectProviderFactory direct
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1190'>NUCCORE-1190</a>] -         Change bytecode enhancement of copyKeyFieldsToObjectId to avoid use of JDOHelper
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1191'>NUCCORE-1191</a>] -         Remove EclipsePluginRegistry
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1194'>NUCCORE-1194</a>] -         Drop support for &lt;extension vendor-name=&quot;jpox&quot; ...&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-76'>NUCEXCEL-76</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-50'>NUCCASSANDRA-50</a>] -         If user specified jdbc-type of &quot;char&quot;, override with &quot;varchar&quot; internally (since there is no &quot;char&quot; in Cassandra)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-51'>NUCCASSANDRA-51</a>] -         IncrementGenerator should use key as &quot;sequence-name&quot; if provided (user input), otherwise &quot;field-name&quot; if for a field, otherwise &quot;root-class-name&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-52'>NUCCASSANDRA-52</a>] -         Detect members using TypeConverter with datastore type of subclass of java.util.Date, and change to converter with datastoreType=java.util.Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-53'>NUCCASSANDRA-53</a>] -         Move to Datastax Cassandra driver v2.0.1
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-54'>NUCCASSANDRA-54</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-92'>NUCHBASE-92</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-49'>NUCJSON-49</a>] -         Use Base64 under org.datanucleus.util instead of own copy
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-51'>NUCJSON-51</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCLDAP-62'>NUCLDAP-62</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-144'>NUCMONGODB-144</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-48'>NUCNEOFORJ-48</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-57'>NUCODF-57</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-785'>NUCRDBMS-785</a>] -         Support NUCCORE-1175
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-787'>NUCRDBMS-787</a>] -         SQLMethod method should have signature getExpression(SQLExpression, List&lt;SQLExpression&gt;) i.e include generics
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-789'>NUCRDBMS-789</a>] -         Support NUCCORE-1097
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-791'>NUCRDBMS-791</a>] -         Drop use of &quot;java-version&quot; on java types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-51'>NUCSPATIAL-51</a>] -         Add TypeConverter for Rectangle -&gt; x,y,width,height  and fix Point -&gt; x,y to use int
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-52'>NUCSPATIAL-52</a>] -         Add multicolumn TypeConverter for Point2D.Double and Point2D.Float
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-7'>NUCGUAVA-7</a>] -         Support NUCCORE-1175
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-9'>NUCGUAVA-9</a>] -         Support NUCCORE-1097
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1188'>NUCCORE-1188</a>] -         PersistenceUnit &quot;exclude-unlisted-classes&quot; is processed incorrectly ignoring the value in the element
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1193'>NUCCORE-1193</a>] -         Bad code in JavaUtils.initialiseJREVersion() [in general] // fails on Android [in concrete]
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-268'>NUCJPA-268</a>] -         inconsistent property name: javax.persistence.sql.load-script-source
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-783'>NUCRDBMS-783</a>] -         AVG on integral number drops decimals on some databases
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-784'>NUCRDBMS-784</a>] -         MapSizeMethod uses wrapper Map rather than java.util.Map!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-786'>NUCRDBMS-786</a>] -         Catch special case SQL method classes (ARRAY etc) to avoid ClassNotResolvedException
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-49'>NUCSPATIAL-49</a>] -         OSGi manifest is missing some package imports
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.0.0.M2

__Apr 1st 2014__ : _Version 4.0 Milestone 2_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1147'>NUCCORE-1147</a>] -         Extend datanucleus.readOnlyDatastore so that it can be specified on a PM
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1154'>NUCCORE-1154</a>] -         Add TypeConverter extension for converting object to multiple components, from java type to multiple datastore types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1160'>NUCCORE-1160</a>] -         Support javax.validation annotations @Size, @NotNull to imply metadata and avoid the need to duplicate that information with JDO/JPA annotations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1163'>NUCCORE-1163</a>] -         Allow a TypeConverter to define the default length limit of a String column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-3'>NUCCASSANDRA-3</a>] -         Support optimistic versioning
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-18'>NUCCASSANDRA-18</a>] -         Support non-PC collections, maps
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-28'>NUCCASSANDRA-28</a>] -         Support members (fields/properties) mapped to more than 1 column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-29'>NUCCASSANDRA-29</a>] -         Default to Session per PMF/EMF, but allow persistence property to set it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-35'>NUCCASSANDRA-35</a>] -         Support compound identity
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-36'>NUCCASSANDRA-36</a>] -         Support user-defined TypeConverter on field/property
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-37'>NUCCASSANDRA-37</a>] -         Support TypeConverter &quot;autoApply&quot; so user can define default handling for a java type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-27'>NUCJSON-27</a>] -         Support embedded 1-1 fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-771'>NUCRDBMS-771</a>] -         Support HikariCP connection pool
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCECLIPSE-6'>NUCACCECLIPSE-6</a>] -         DataNucleus Context Menu does not appear in Project Explorer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-7'>NUCJAVAEIGHT-7</a>] -         Add support for Duration, Period, Year, Month, DayOfWeek, YearMonth, MonthDay, ZoneId, Instant, OffsetTime, OffsetDateTime, ZonedDateTime
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1144'>NUCCORE-1144</a>] -         Update NamingFactory to take a set of reserved keywords that an identifier has to be quoted to use
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1145'>NUCCORE-1145</a>] -         Provide TypeConverters for byte[], int[], float[], etc to ByteBuffer and clean up TypeConversionHelper type safety
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1157'>NUCCORE-1157</a>] -         Split TypeManager converter helpers out into TypeConverterHelper
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1164'>NUCCORE-1164</a>] -         Add TypeConverters for javax.time LocalDateTime -&gt; Timestamp, LocalTime -&gt; Time, LocalDate -&gt; Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1166'>NUCCORE-1166</a>] -         Extend CompleteClassTable to support multiple columns per member
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1172'>NUCCORE-1172</a>] -         Some calls to ObjectProvider.loadUnloadedFields only require relation fields loading
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-25'>NUCCASSANDRA-25</a>] -         Change javaType-datastoreType conversion process to use TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-30'>NUCCASSANDRA-30</a>] -         Support persistence of members of type Locale (or array of Locale)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-42'>NUCCASSANDRA-42</a>] -         Support cascadePersist/cascadeUpdate for reachability
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-43'>NUCCASSANDRA-43</a>] -         Support interface fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-75'>NUCEXCEL-75</a>] -         Adopt Table/Column/CompleteClassTable data structures rather than ad-hoc index/schema control
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-56'>NUCODF-56</a>] -         Adopt Table/Column/CompleteClassTable data structures rather than ad-hoc index/schema control
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-46'>NUCJSON-46</a>] -         Adopt Table/Column/CompleteClassTable data structures rather than ad-hoc index/schema control
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-775'>NUCRDBMS-775</a>] -         UUIDMapping, URLMapping, URIMapping can be removed and just fallback to TypeConverterStringMapping to get the same results
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-776'>NUCRDBMS-776</a>] -         LocaleMapping, CurrencyMapping, TimeZoneMapping, StringBufferMapping, StringBuilderMapping can be removed and just fallback to TypeConverterStringMapping to get the same results
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-778'>NUCRDBMS-778</a>] -         Update mapping/mappingClass lookup process to allow for TypeConverter specified via jdbcType
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-781'>NUCRDBMS-781</a>] -         Support multi column TypeConverter and wrap them in a XXXMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-18'>NUCJODATIME-18</a>] -         Add TypeConverters for DateTime -&gt; Timestamp, LocalTime -&gt; Time, LocalDate -&gt; Date and maybe also Timestamp
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1105'>NUCCORE-1105</a>] -         Upgrade repackaged ASM to v5 when it is released
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1142'>NUCCORE-1142</a>] -         Add TypeConverter for Serializable -&gt; java.nio.ByteBuffer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1143'>NUCCORE-1143</a>] -         Add StoreManager.OPTION_ORM_FOREIGN_KEYS to signify that the store supports FKs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1146'>NUCCORE-1146</a>] -         Add StoreManager.OPTION_APPLICATION_COMPOSITE_ID to signify that the store supports multiple PK fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1148'>NUCCORE-1148</a>] -         Change &quot;datanucleus.identifier.case&quot; 'PreserveCase' to be 'MixedCase' to be match internal namings
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1151'>NUCCORE-1151</a>] -         In-memory query evaluation : improve ordering support so we can process DyadicExpression, InvokeExpression etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1152'>NUCCORE-1152</a>] -         In-memory query evaluation : support for Map.containsEntry(key,val)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1158'>NUCCORE-1158</a>] -         Change TypeManager to be an interface, and have default implementation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1159'>NUCCORE-1159</a>] -         Fix NamingFactory index generation to respect user-specified names, and add method for datastore-id, discriminator, multitenancy index
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1161'>NUCCORE-1161</a>] -         Add TypeConverter for converting java.sql.Timestamp -&gt; String
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1162'>NUCCORE-1162</a>] -         Fix MultiMap.remove(Object,Object) method to avoid clash with JDK1.8 new Map method
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1165'>NUCCORE-1165</a>] -         Change javax.time default TypeConverter so we persist as Timestamp/Time/Date wherever possible (hence queryable)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1168'>NUCCORE-1168</a>] -         Remove default TypeConverter for java.util.Date/java.sql.Date/java.sql.Time/java.sql.Timestamp/BigDecimal/BigInteger since persistable natively
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1169'>NUCCORE-1169</a>] -         Remove references to javax.time now that we use a separate plugin for JDK 1.8 time
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1170'>NUCCORE-1170</a>] -         Store Column &quot;jdbcType&quot; with org.datanucleus.store.schema.table.Column so store plugin don't need to do lookups
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1171'>NUCCORE-1171</a>] -         Add JdbcType enum and change ColumnMetaData.jdbcType to be of that type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-10'>NUCCASSANDRA-10</a>] -         Support quoted table/column identifiers (i.e case sensitive)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-23'>NUCCASSANDRA-23</a>] -         Add internal table/column definition, to avoid continual column naming lookups
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-32'>NUCCASSANDRA-32</a>] -         Add list of reserved keywords and prohibit use of them as identifiers
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-33'>NUCCASSANDRA-33</a>] -         Support persistence of Collection&lt;Enum&gt; etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-40'>NUCCASSANDRA-40</a>] -         Map BigDecimal to Cassandra &quot;decimal&quot; type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-41'>NUCCASSANDRA-41</a>] -         Support java.util.Queue as Cassandra &quot;list&quot; type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-45'>NUCCASSANDRA-45</a>] -         Support null elements in Collection&lt;PC&gt; and null keys in Map&lt;?, PC&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-46'>NUCCASSANDRA-46</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-90'>NUCHBASE-90</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-91'>NUCHBASE-91</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-143'>NUCMONGODB-143</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-72'>NUCEXCEL-72</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-73'>NUCEXCEL-73</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-53'>NUCODF-53</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-54'>NUCODF-54</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-45'>NUCJSON-45</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-769'>NUCRDBMS-769</a>] -         Adopt NamingCase instead of IdentifierCase so we have commonality across all store plugin
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-772'>NUCRDBMS-772</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-773'>NUCRDBMS-773</a>] -         Support DBCP2 as connection pool (changed class names from DBCP v1.x)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-774'>NUCRDBMS-774</a>] -         Support NUCCORE-1162, avoid JDK 1.8 naming clash
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-777'>NUCRDBMS-777</a>] -         Drop ObjectAsXXXMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-780'>NUCRDBMS-780</a>] -         Drop javax.time Mapping/Expression/Literal classes now that we have TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-19'>NUCJODATIME-19</a>] -         Drop Mapping/Expression/Literal classes for LocalDate, LocalTime, DateTime since we have TypeConverters now
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-1'>NUCJAVAEIGHT-1</a>] -         Update java.time support to reflect packaging in &quot;Java 8&quot;
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1149'>NUCCORE-1149</a>] -         Initialisation of org.datanucleus.store.types.simple.Properties is incorrect
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1150'>NUCCORE-1150</a>] -         InMemory query evaluation of max/min/avg/sum(arg) when no candidates is returning an integer : should return the type of the arg
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1156'>NUCCORE-1156</a>] -         java.sql.Timestamp SCO wrapper should also preserve nanos when cloning/detaching etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1167'>NUCCORE-1167</a>] -         NamingFactory column namer when embedded metadata has &lt;column&gt; but no name generates null column name!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-31'>NUCCASSANDRA-31</a>] -         Empty collection fields are being stored as null, and then when read back in are null rather than empty
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-39'>NUCCASSANDRA-39</a>] -         User specified table name for &quot;increment&quot; value generator table is not being respected
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-44'>NUCCASSANDRA-44</a>] -         Surrogate version should be long or Timestamp for consistency with RDBMS
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-770'>NUCRDBMS-770</a>] -         Timestamp maximum precision is milliseconds
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMAVEN-47'>NUCMAVEN-47</a>] -         Exception (Error 87 - commandline too long) when starting the enhancer in forked mode
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCECLIPSE-11'>NUCACCECLIPSE-11</a>] -         Exception (Error 87 - commandline too long) during the enhancer is called within eclipse (plugin version 3.0.1)
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.0.0.M1

__Mar 1st 2014__ : _Version 4.0 Milestone 1_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-159'>NUCCORE-159</a>] -         Support for transaction &quot;savepoints&quot;
</li>
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
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-767'>NUCRDBMS-767</a>] -         OSGi manifest should also include new HSQLDB (v2.0+) driver import
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

