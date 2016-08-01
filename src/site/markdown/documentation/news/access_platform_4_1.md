<head><title>AccessPlatform 4.1</title></head>

#Release Notes for DataNucleus AccessPlatform v4.1

The 4.1 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 4.1_ includes the following over 4.0

<ul>
<li>Minor upgrade to bytecode enhancement contract to allow for separation of enhancement API</li>
<li>Rewrite of handling of container field update code.</li>
<li>Types : support for Jodatime LocalDateTime</li>
<li>JDO : PersistenceManager and Query implementations now implement AutoCloseable</li>
<li>JDO : Ability to save a query as a "named" query, for later access</li>
<li>JDO : support for JDOQL subqueries in SELECT clause</li>
<li>JPA : support for non-standard value generators</li>
<li>JPA : support for "KEY", "VALUE" keywords in JPQL</li>
<li>JPA : support for parameters in FROM "ON" clause of JPQL</li>
<li>JPA : support for RIGHT OUTER JOIN in FROM clause of JPQL</li>
<li>JPA : support for JPQL subqueries in SELECT and HAVING clauses</li>
<li>JPA : support for JPQL ordering by result alias</li>
<li>JPA : support for AttributeConverters on map key/value and collection element</li>
<li>JPA : Ability to save a query as a "named" query, for later access</li>
<li>REST : support for map/array fields</li>
<li>REST : support for maxFetchDepth on GET requests</li>
<li>REST : support for GZIP compression on GET requests</li>
<li>MongoDB : much improved relation handling, and support for date and interface fields.</li>
<li>RDBMS : support for some HikariCP connection pool properties</li>
<li>Persistent Properties : you can now use inheritance in persistent properties, overriding getters etc</li>
</ul>

<br/>

# DataNucleus AccessPlatform 4.1.12

__Aug 2nd 2016__ : _Version 4.1.12_ includes the following changes

## Enhancements

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/24'>datanucleus-api-jdo-24</a>] - JDOPersistenceManager.close should null the pmf</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/31'>datanucleus-api-jpa-31</a>] - Null out some variables on close of EM, and assert when EM closed on all query methods</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/81'>datanucleus-rdbms-81</a>] - Cater for PostgreSQL specific default value :: syntax</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/82'>datanucleus-rdbms-82</a>] - ClassAdder mixes table validation with column initialisation. Should be separate</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/84'>datanucleus-rdbms-84</a>] - Allow control over whether to use column default values when a value is null</li>
</ul>

## Bugs

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/105'>datanucleus-core-105</a>] - Fix code typo in ExecutionContextImpl.getManagedObjects</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/28'>datanucleus-api-jpa-28</a>] - Fix IdentifiableType.getId when using generics</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/29'>datanucleus-api-jpa-29</a>] - Fix IdentifiableType.getVersion when using subtype</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.11

__Jun 6th 2016__ : _Version 4.1.11_ includes the following changes

## Enhancements

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/73'>datanucleus-core-73</a>] - CompleteClassTable : cater for columnMetaData on collection element when intended for field</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/70'>datanucleus-core-70</a>] - Federation : cater for simple use-cases of identity</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/44'>datanucleus-rdbms-44</a>] - jdbc timeouts are not propagated for SQL queries</li>
</ul>

## Bugs

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/68'>datanucleus-core-68</a>] - OperationQueue : performAll for backing store should only process for the specified ObjectProvider</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/76'>datanucleus-core-76</a>] - CompleteClassTable : mark embedded PK columns as being part of PK</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/78'>datanucleus-core-78</a>] - NamingFactory do not cater for unique index name for DISCRIMINATOR_COLUMN</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/15'>datanucleus-api-jdo-15</a>] - Bean Validation : don't fire off validation on prePersist and preStore, just on one</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/23'>datanucleus-api-jpa-23</a>] - Criteria in(...).not() is ignoring the NOT in the generic compilation (and generated SQL)</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/20'>datanucleus-api-jpa-20</a>] - Bean Validation : don't fire off validation on prePersist and preStore, just on one</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/49'>datanucleus-rdbms-49</a>] - Bulk fetch has bug when trying to handle array case, assumes it is a Collection resulting in NPE</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.10

__Apr 7th 2016__ : _Version 4.1.10_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1399'>NUCCORE-1399</a>] -         Add mechanism whereby if there is metadata for a class that is not in the classpath we can just ignore it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMAVEN-52'>NUCMAVEN-52</a>] -         Support &quot;datanucleus.metadata.ignoreMetaDataForMissingClasses&quot; via enhancer
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1389'>NUCCORE-1389</a>] -         java.awt.Color should be in DFG
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1391'>NUCCORE-1391</a>] -         SerializableByteBufferConverter should use wrap/remaining to convert to bytes but doesn't
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-332'>NUCJPA-332</a>] -         If metadata specified using orm.xml only, the entity name is not defaulted
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-333'>NUCJPA-333</a>] -         Criteria multiple join with no join alias results in exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-334'>NUCJPA-334</a>] -         Criteria join to a multiple valued path doesn't work.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1013'>NUCRDBMS-1013</a>] -         JPQL : join to embedded object generates incorrect SQL
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1017'>NUCRDBMS-1017</a>] -         Insert of array of persistable objects fails to insert join table when cascade not enabled
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.9

__Feb 20th 2016__ : _Version 4.1.9_ includes the following changes

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1368'>NUCCORE-1368</a>] -         List of &quot;simple&quot; result classes is very restrictive. Extend to include other commonly used &quot;simple&quot; classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1385'>NUCCORE-1385</a>] -         Query parsing can be improved to better cater for quoting and end of line characters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-25'>NUCREST-25</a>] -         Remove use of NucleusException
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-26'>NUCREST-26</a>] -         Change &quot;jdoql&quot; / &quot;jpql&quot; modes so that they take parameter &quot;query&quot; with the encoded query
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1001'>NUCRDBMS-1001</a>] -         Oracle supports NVARCHAR but JDBC driver doesn't acknowledge it
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1372'>NUCCORE-1372</a>] -         Nondurable classes should not be L2 cached, ever.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1379'>NUCCORE-1379</a>] -         Dont log about AutoStartMechanism if set to None
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-998'>NUCRDBMS-998</a>] -         Prevent SortedSet (and subclasses) be allocated a ListXXXStore since needs unsorted
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1007'>NUCRDBMS-1007</a>] -         Apparently need a call to ConnectionFactory.setPool() to avoid log message with DBCP2
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1009'>NUCRDBMS-1009</a>] -         Parameters in group by expressions are not set on the JDBC statement
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.8

__Jan 13th 2016__ : _Version 4.1.8_ includes the following changes

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-991'>NUCRDBMS-991</a>] -         Support for fetch of ReferenceMapping field when there is a single implementation and using FK
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1366'>NUCCORE-1366</a>] -         AbstractMemberMetaData.getClassName(false) can return fully qualified name in some situations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-329'>NUCJPA-329</a>] -         JPA MetaModel doesn't cater correctly for List&lt;nonPC&gt;, and sets to CollectionAttributeImpl instead of ListAttributeImpl
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-990'>NUCRDBMS-990</a>] -         Loading of interface field with single implementation with version field is not loading the version
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-992'>NUCRDBMS-992</a>] -         Name of candidate key (unique) on join table is not respected
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-995'>NUCRDBMS-995</a>] -         TypeConverterMapping.getJavaType is incorrect when roleForMember is set
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.7

__Nov 27th 2015__ : _Version 4.1.7_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1358'>NUCCORE-1358</a>] -         Allow JPQL to exclude subclasses of the candidate
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-983'>NUCRDBMS-983</a>] -         Support SAP &quot;SQLAnywhere&quot;
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1347'>NUCCORE-1347</a>] -         ClassMetaData has &quot;members&quot; that should be genericised to AbstractMemberMetaData, and lookup of member name improved
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1359'>NUCCORE-1359</a>] -         Determine Collection element and Map key/value type from TypeVariable when using ParametrizedType within ParameterizedType
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1363'>NUCCORE-1363</a>] -         CompleteClassTable : has check on duplicated column name, but that should not apply when supporting &quot;nested&quot; embedded
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1360'>NUCCORE-1360</a>] -         Support PK field conversions for types Currency, TimeZone, UUID
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-20'>NUCJAVAEIGHT-20</a>] -         InstantTimestampConverter : use convenience methods to do the conversion
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-165'>NUCMONGODB-165</a>] -         Make sure &quot;ownerMmd&quot; is set for FetchFieldManager when embedded, add TODO to resolve
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJDOQUERY-22'>NUCJDOQUERY-22</a>] -         Add support for TypeVariables
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1362'>NUCCORE-1362</a>] -         Persistable elements contained in Collection/Map that is serialised (whole field) are not detached/attached correctly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-981'>NUCRDBMS-981</a>] -         Support NUCCORE-1362
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-985'>NUCRDBMS-985</a>] -         SELECT statement generation handling of ordering when multiple cols per order expression should apply quoting as final step but doesnt
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-986'>NUCRDBMS-986</a>] -         Creation of mapping in some cases misses the MultiColumnConverter case and doesnt use TypeConverterMultiMapping
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.6

__Nov 16th 2015__ : _Version 4.1.6_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-970'>NUCRDBMS-970</a>] -         SQLStatement needs a way of generation where we don't use table aliases, and just use table names
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-977'>NUCRDBMS-977</a>] -         Support persisting a Collection/Map using a TypeConverter for the whole field
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-971'>NUCRDBMS-971</a>] -         SQLite doesn't provide explicit support for putting nulls last, but can use &quot;{col} IS NULL, {col}&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-972'>NUCRDBMS-972</a>] -         View creation : skip any token that is a &quot;comment&quot; since some RDBMS don't handle that
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-973'>NUCRDBMS-973</a>] -         Delete tables processing : goes off and calls DatabaseMetaData.getColumns for detection of table existence but could just get table type (quicker!)
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-322'>NUCJPA-322</a>] -         Support AttributeConverter on a collection field to be for the whole field not just the element
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-975'>NUCRDBMS-975</a>] -         Provide access to RDBMSQueryCompilation, and to the SQLStatement(s) that the compilation is made up of.
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1355'>NUCCORE-1355</a>] -         JPQLSingleStringParser has missing trimRight handling (typo in trimLeft)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1356'>NUCCORE-1356</a>] -         Metadata processing moves ColumnMetaData to ElementMetaData is not embedded/serialised but should also allow for full field type converter case
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-974'>NUCRDBMS-974</a>] -         Oracle, Firebird require that when using GROUP BY, all non-aggregate SELECT components are in the GROUP BY clause
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.1.5

__Oct 18th 2015__ : _Version 4.1.5_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1350'>NUCCORE-1350</a>] -         Extend NUCCORE-1344 to allow LEFT JOIN FETCH
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-944'>NUCRDBMS-944</a>] -         Support polymorphic joins when using UNION, so only apply to particular UNIONs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-954'>NUCRDBMS-954</a>] -         MySQL : allow setting the COLLATION and CHARACTER SET of any tables that are created
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-958'>NUCRDBMS-958</a>] -         Firebird supports date functions using EXTRACT(...)
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-951'>NUCRDBMS-951</a>] -         Index auto creation : detect reuse of fields so we don't try to duplicate indexes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-945'>NUCRDBMS-945</a>] -         SQLStatement needs more flexibility with joins; apply to just one union, pass in join type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-952'>NUCRDBMS-952</a>] -         SchemaTool : delete of schema for classes can try to validate the tables structure before dropping, but should just drop the tables if present
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-955'>NUCRDBMS-955</a>] -         Firebird v2 requires use of CHAR_LENGTH for length of VARCHAR fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-959'>NUCRDBMS-959</a>] -         MySQL doesn't support &quot;NULLS FIRST | LAST&quot; but does allow ISNULL(...) extra clause to put nulls last (default is first)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-962'>NUCRDBMS-962</a>] -         Candidate key auto creation : detect reuse of fields so we don't try to duplicate uniques
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-963'>NUCRDBMS-963</a>] -         HSQLDB v2+ doesn't have LONGVARBINARY, so need to provide own mapping
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-946'>NUCRDBMS-946</a>] -         Add RIGHT_OUTER_JOIN as option in DatastoreAdapter that can be unsupported (SQLite)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-949'>NUCRDBMS-949</a>] -         Support date/time methods on SQLite
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-957'>NUCRDBMS-957</a>] -         Firebird v2 requires use of SUBSTRING for substring of VARCHAR fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-967'>NUCRDBMS-967</a>] -         SQLite doesn't support &quot;ALL|ANY|SOME {subquery}&quot; keyword constructs, so throw exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-968'>NUCRDBMS-968</a>] -         SQLite LOCATE / String.indexOf should use INSTR(x,y) rather than LOCATE
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-969'>NUCRDBMS-969</a>] -         SQLite DELETE / UPDATE JPQL should not use alias since these are not supported with SQLite
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1351'>NUCCORE-1351</a>] -         IN predicate unexpectedly gets transformed to EQ predicate
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-942'>NUCRDBMS-942</a>] -         Changes to managed entities not detected when element collection is involved
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-943'>NUCRDBMS-943</a>] -         Use of query result aliases when using DatastoreAdapter in quoted case needs quotes adding to SQL
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-947'>NUCRDBMS-947</a>] -         SQLite String.substring should use SUBSTR(x,y,z) rather than SUBSTRING(x FROM y FOR z)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-948'>NUCRDBMS-948</a>] -         Fix for NUCRDBMS-823 was non-optimum. If using SQLite and IDENTITY but for a Long field, should get LongMapping with IntegerRDBMSMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-950'>NUCRDBMS-950</a>] -         Addition of datanucleus.schema.autoCreateSchema for generating schema can fail on some JDBC drivers that don't support catalog
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-953'>NUCRDBMS-953</a>] -         Schema generation unnecessarily creates indexes for the values of element collections
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-956'>NUCRDBMS-956</a>] -         JPQL : Referring to map key/value from outer query in a subquery can result in extra joins adding in the subquery
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-961'>NUCRDBMS-961</a>] -         Use of persistent property for persistable object (1-1, N-1), and adding override in subclass results in multiple (duplicate) FKs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-23'>NUCJODATIME-23</a>] -         Wrong Implementation of JodaLocalDateSqlDateConverter Class
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.4

__Sept 15th 2015__ : _Version 4.1.4_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1344'>NUCCORE-1344</a>] -         JPQL Compilation : support limited polymorphic join
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-932'>NUCRDBMS-932</a>] -         Support polymorphic joins for entities
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-939'>NUCRDBMS-939</a>] -         Support parameters in SELECT clause, particularly when as part of subqueries
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-935'>NUCRDBMS-935</a>] -         SQLStatement : change handling of selects to retain SQLText until statement generation
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1346'>NUCCORE-1346</a>] -         JDO 3.2 requires change to behaviour at close of EC with active transaction. Make it configurable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1348'>NUCCORE-1348</a>] -         Extend NUCCORE-1338 to EmbeddedMetaData
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1345'>NUCCORE-1345</a>] -         Unable to use version tag on ORM file without having to define the strategy again
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1349'>NUCCORE-1349</a>] -         JDOQL/JPQL parse of BigInteger value is parsed internally to be Long and loses precision
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-936'>NUCRDBMS-936</a>] -         Addendum to NUCRDBMS-917. Dont create indexes when not indexable column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-938'>NUCRDBMS-938</a>] -         Column creation for overridden field can try to create as IDENTITY when no value strategy defined!
</li>
</ul>

<br/>

# DataNucleus AccessPlatform 4.1.3

__Aug 16th 2015__ : _Version 4.1.3_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1335'>NUCCORE-1335</a>] -         Add ability to set JDOQL/JPQL strictness on query compilation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1336'>NUCCORE-1336</a>] -         JPQL : support CURRENT_TIMESTAMP(), CURRENT_DATE(), CURRENT_TIME()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1337'>NUCCORE-1337</a>] -         JPQL : support COUNT(*)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-914'>NUCRDBMS-914</a>] -         Support (numeric) bitwise AND, OR, XOR for PostgreSQL, MySQL/MariaDB and SQLServer
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-922'>NUCRDBMS-922</a>] -         Handle compilation of &quot;interfaceField == :param&quot;
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1331'>NUCCORE-1331</a>] -         Modify query parse/compile to split out bitwise operators (&amp;, |, ^) from conditional (&amp;&amp;, ||)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1334'>NUCCORE-1334</a>] -         Add StoreManager option for whether JDOQL bitwise ops are supported
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1338'>NUCCORE-1338</a>] -         Modularise the code for deciding if a persistable field comes from the enhancer, so we can ignore the right ones
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1340'>NUCCORE-1340</a>] -         When user specifies a TypeConverter for a field and not found later then exception should be thrown
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-106'>NUCAPIJDO-106</a>] -         JDO 3.2 : Add PMF supported option for &quot;JDOQL bitwise ops&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-55'>NUCNEOFORJ-55</a>] -         Access to TypeConverter in FetchFieldManager makes no sense since already available in CompleteClassTable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-56'>NUCJSON-56</a>] -         Access to TypeConverter in FetchFieldManager makes no sense since already available in CompleteClassTable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-97'>NUCHBASE-97</a>] -         Access to TypeConverter in FetchFieldManager makes no sense since already available in CompleteClassTable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-915'>NUCRDBMS-915</a>] -         Support NUCCORE-1334 for DatastoreAdapters that do support it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-923'>NUCRDBMS-923</a>] -         Support NUCCORE-1340
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1333'>NUCCORE-1333</a>] -         Object retrieval of bidir relation with non-RDBMS datastore can lead to StackOverflowException when non-transactional and relation fields in FetchPlan
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1341'>NUCCORE-1341</a>] -         StringUtils.getStringFromStackTrace is broken since 4.0
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-320'>NUCJPA-320</a>] -         Parameter inspection via javax.persistence.Query.getParameters is missing parameters from subqueries
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-321'>NUCJPA-321</a>] -         JPAQueryParameter needs equals/hashCode
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-54'>NUCNEOFORJ-54</a>] -         When doing a query, cater for the class not being known
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-916'>NUCRDBMS-916</a>] -         SQLite String.length should use &quot;LENGTH(col)&quot; rather than &quot;CHAR_LENGTH(col)&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-917'>NUCRDBMS-917</a>] -         Make schema index handling consistent for join tables
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-918'>NUCRDBMS-918</a>] -         Dynamic schema generation : if using superclass table and table already created, and have 1-N join table, can fail to generate join table
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-919'>NUCRDBMS-919</a>] -         TypeConverterMapping needs to cater for mapping basic type to different basic type but doesn't currently
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-924'>NUCRDBMS-924</a>] -         Wrong SQL join order when alias used in ON condition
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-925'>NUCRDBMS-925</a>] -         Using entity select in a subquery results in multiple columns selected
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-926'>NUCRDBMS-926</a>] -         NPE when using SUBSTRING in result clause
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-927'>NUCRDBMS-927</a>] -         Order by in subquery results in wrong SQL
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-929'>NUCRDBMS-929</a>] -         Select of candidate id only has bug when we have multiple PK fields, assigns DN_APPID alias twice which is a problem for some datastores
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.2

__Jul 14th 2015__ : _Version 4.1.2_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1325'>NUCCORE-1325</a>] -         Support Java generic TypeVariable where declared by class generic type bounds
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-314'>NUCJPA-314</a>] -         Support specification of datastore identity using XML metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-316'>NUCJPA-316</a>] -         Support specification of surrogate version using XML metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-317'>NUCJPA-317</a>] -         Provide access to &quot;datastore-id&quot; and &quot;surrogate-version&quot; via helper methods
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-901'>NUCRDBMS-901</a>] -         MariaDB support storing millisecs in time columns, needs recognising in adapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-911'>NUCRDBMS-911</a>] -         When RDBMS supports &quot;FOR UPDATE NOWAIT&quot; provide extension for specifying &quot;NOWAIT&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-912'>NUCRDBMS-912</a>] -         Ability to register an SQLMethod at runtime when not registered via the plugin mechanism
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-913'>NUCRDBMS-913</a>] -         Add COUNTSTAR function to equate to SQL &quot;COUNT(*)&quot; since not present in JDOQL/JPQL directly
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1323'>NUCCORE-1323</a>] -         Add generics for element, key, value to all wrappers and backing stores
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1324'>NUCCORE-1324</a>] -         Bump repackaged ASM to v5.0.4 from 5.0.3
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-315'>NUCJPA-315</a>] -         Rename @DatastoreIdentity to be @DatastoreId for consistency
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-899'>NUCRDBMS-899</a>] -         Add generics for element, key, value to backing stores (see NUCCORE-1323)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-904'>NUCRDBMS-904</a>] -         PostgreSQL doesn't support &quot;read uncommitted&quot; so disable in adapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-905'>NUCRDBMS-905</a>] -         PostgreSQL doesn't support stored procedures so disable in adapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-11'>NUCGUAVA-11</a>] -         Support NUCCORE-1323
</li>
</ul>

<br/>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-313'>NUCJPA-313</a>] -         JPQL generated for Criteria can have too many blanks in FROM clause when no alias
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-318'>NUCJPA-318</a>] -         Metamodel Type getJavaType returns wrong classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-900'>NUCRDBMS-900</a>] -         Schema generation fails if using a FK Map, and a separate unique constraint on a class, and not specifying constraint name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-902'>NUCRDBMS-902</a>] -         PostgreSQL function &quot;SUBSTRING&quot; needs explicit CAST of FROM/FOR args to INTEGER otherwise fails
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-903'>NUCRDBMS-903</a>] -         StringExpression.add creates CONCAT (||) of two expressions but should always be in parentheses, and in one case isn't
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-906'>NUCRDBMS-906</a>] -         Change entity after persist causes insert to fail
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-908'>NUCRDBMS-908</a>] -         DN4 does not seem to automatically create the DB schema (as in @PersistenceCapable(schema=...) for any entities annotated as such
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-909'>NUCRDBMS-909</a>] -         User specified catalog/schema should be translated into adapter case as required
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-910'>NUCRDBMS-910</a>] -         H2 adapter CREATE SCHEMA should use schema rather than catalog
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.1.1

__Jun 13th 2015__ : _Version 4.1.1_ includes the following changes

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1322'>NUCCORE-1322</a>] -         If user calls setXXX for a container field to replace the delegate container then we should swap the value being managed.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-10'>NUCGUAVA-10</a>] -         Support NUCCORE-1322
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-898'>NUCRDBMS-898</a>] -         Support passing required JoinType to nested fetches, so when one object is fetched LEFT OUTER then subobjects can be also
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1316'>NUCCORE-1316</a>] -         StateManagerImpl.setIdentity has a block of code that seemingly is not needed
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-309'>NUCJPA-309</a>] -         Code for processing AttributeConverters is dotted through code. Move to convenience location
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-897'>NUCRDBMS-897</a>] -         Support &quot;log&quot; function on Postgresql via &quot;LN&quot; rather than &quot;LOG&quot;
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1315'>NUCCORE-1315</a>] -         Persistable class with own writeObject() method should be enhanced to have a call to dnPreSerialize before the user code
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1317'>NUCCORE-1317</a>] -         literal timestamp parsing bug in JPQLParser.java resulting with &quot;'...' expected in JDBC escape syntax&quot; exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1320'>NUCCORE-1320</a>] -         persistence.xml &quot;exclude-unlisted-classes&quot; tag default value is incorrect
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-310'>NUCJPA-310</a>] -         error with entityManager.lock(..., LockModeType.OPTIMISTIC)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-311'>NUCJPA-311</a>] -         error in JPAEntityManager.find(Class, Object, LockModeType)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-312'>NUCJPA-312</a>] -         When converting Criteria query with Timestamp literal into JPQL string form, it omits the nanosecs part
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.1.0.RELEASE

__May 19th 2015__ : _Version 4.1 RELEASE_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1308'>NUCCORE-1308</a>] -         Support Java generic TypeVariable in 1-1/N-1 relations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1309'>NUCCORE-1309</a>] -         Support Java generic TypeVariable in 1-N/M-N relations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1312'>NUCCORE-1312</a>] -         Support JPQL with RIGHT OUTER JOIN
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-892'>NUCRDBMS-892</a>] -         Support JPQL with RIGHT OUTER JOIN
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1313'>NUCCORE-1313</a>] -         Support JPQL FROM &quot;ON&quot; clauses that are other than DyadicExpression
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1314'>NUCCORE-1314</a>] -         If annotation specified on field and method then take as field and use method annotations as if on field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-307'>NUCJPA-307</a>] -         Criteria API usage currently requires something to be selected (using select/multiSelect) whereas could default to candidate
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-894'>NUCRDBMS-894</a>] -         Query of Collection.contains where the element is of an invalid type should create query with 1=0 rather than throw exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-895'>NUCRDBMS-895</a>] -         Support JPQL &quot;COALESCE&quot;/&quot;NULLIF&quot; with non-numeric arguments
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-91'>NUCAPIJDO-91</a>] -         Support typesafe query StringExpression.add(...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-306'>NUCJPA-306</a>] -         Change &quot;datanucleus.rdbms.allowColumnReuse&quot; default to &quot;true&quot; for JPA usage
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-890'>NUCRDBMS-890</a>] -         JPQL : Support use of MEMBER OF on Map (and interpret as &quot;Map.containsValue&quot;)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-891'>NUCRDBMS-891</a>] -         Support query joins that join to EmbeddedId to provide access to the fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-896'>NUCRDBMS-896</a>] -         JDOQL : support CharacterLiteral.toUpperCase/toLowerCase methods
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1311'>NUCCORE-1311</a>] -         JPQL &quot;[NOT] IN&quot; not compiled correctly when we have parameter yet value type not yet known
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-308'>NUCJPA-308</a>] -         CriteriaBuilder.in always tries to create &quot;(val == collVal1 || val == collVal2 || ...) but should use IN if single value specified to allow for Collection parameter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-893'>NUCRDBMS-893</a>] -         FROM joins should process first part of the join expression and take the table for that as one side of the join
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.1.0.M4

__May 1st 2015__ : _Version 4.1 Milestone 4_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1292'>NUCCORE-1292</a>] -         Allow subquery in SELECT clause (JDOQL/JPQL)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-304'>NUCJPA-304</a>] -         Support @Convert with attributeName of &quot;key&quot; or &quot;value&quot; to apply to the key or value of a Map field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-305'>NUCJPA-305</a>] -         Support @Convert when specified on Collection to convert the element
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-17'>NUCRDBMS-17</a>] -         Classes with collection/map fields should be allowed to have &quot;subclass-table&quot; inheritance strategy, and the elements/keys/values should be allowed to have &quot;subclass-table&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-18'>NUCRDBMS-18</a>] -         1-1 undirectional relation needs the flexibility of allowing &quot;subclass-table&quot; at the other end
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-19'>NUCRDBMS-19</a>] -         Support for 1-N bidir relation between impl of interface with collection of elements
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-719'>NUCRDBMS-719</a>] -         Provide the ability to override a builtin method mapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-882'>NUCRDBMS-882</a>] -         Support for DEGREES/RADIANS functions and JDOQL Math.toDegrees/Math.toRadians
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1300'>NUCCORE-1300</a>] -         Call to PM.refreshObject/retrieveObject/evictObject gives unclear exception message when transient object passed 
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1306'>NUCCORE-1306</a>] -         TypeManager should use ConcurrentHashMap since multithreaded
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-89'>NUCAPIJDO-89</a>] -         Allow PM.getFetchGroup/PMF.getFetchGroup to include members of existing named/static query when available
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-878'>NUCRDBMS-878</a>] -         Query attempting to select a 1-1/N-1 field which uses subclass-table (hence no FK) throws exception on form of statement but should just select FK only
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-884'>NUCRDBMS-884</a>] -         When a JDBC driver provides multiple sql-type for a jdbc-type should be possible to have default matching plugin.xml
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-54'>NUCSPATIAL-54</a>] -         Support NUCRDBMS-884
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1293'>NUCCORE-1293</a>] -         Prevent SCOOperation's being added to OperationQueue when owner object is not yet flushed to datastore
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1294'>NUCCORE-1294</a>] -         ManagedRelations : backed Set wrappers initialise(Collection, Collection) register changes twice
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1296'>NUCCORE-1296</a>] -         In-memory evaluation of assorted Math.xxx functions
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1298'>NUCCORE-1298</a>] -         Move &quot;implementation-classes&quot; handling to be with CollectionMetaData, MapMetaData etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1301'>NUCCORE-1301</a>] -         Metadata load often resulted in attempt to find metadata for single-field identity classes when obviously not persistent
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1302'>NUCCORE-1302</a>] -         Clean up ExecutionContext.close to merge methods only used once, so we improve logging
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-90'>NUCAPIJDO-90</a>] -         Change JDOAdapter.isXXX to use Persistable direct rather than routing through JDOHelper.isXXX and then through JDOImplHelper.nonBinaryCompatibleIs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-302'>NUCJPA-302</a>] -         Support query hints on @NamedQuery, @NamedNativeQuery etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-877'>NUCRDBMS-877</a>] -         1-N FK Set of interface object doesn't allow update of FK reliably
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-883'>NUCRDBMS-883</a>] -         JPQL should allow ORDER BY using result alias
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1295'>NUCCORE-1295</a>] -         Generic compiler can fail to correctly detect class names in PrimaryExpression and result in invalid compilation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1299'>NUCCORE-1299</a>] -         Make sure that close of ExecutionContext completes, checking for null objects
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1303'>NUCCORE-1303</a>] -         Joining over map value not working when wanting to chain the join to sub-objects of the value
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1304'>NUCCORE-1304</a>] -         Generic compile of filter &quot;field NOT IN (:param)&quot; doesn't include the NOT in the resultant compile
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1305'>NUCCORE-1305</a>] -         Generic compile of filter something like &quot;field.method().field.method()&quot; is not compiled correctly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1307'>NUCCORE-1307</a>] -         List wrapper SCOs have error in initialise method when updating (setXXXField); should log with operation queue in more situations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-303'>NUCJPA-303</a>] -         Metamodel returns ONE_TO_ONE instead of MANY_TO_ONE
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-876'>NUCRDBMS-876</a>] -         When we try to fetch a N-1 &quot;owner&quot; field (with join table) where the owner has an interface, it doesn't get the implementation and fails
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-879'>NUCRDBMS-879</a>] -         Backing store of Collection with multiple root elements doesn't give correct info for size()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-880'>NUCRDBMS-880</a>] -         When storing java.sql.Timestamp as String it calls ps.setObject(Timestamp) and relies on JDBC driver
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-881'>NUCRDBMS-881</a>] -         RuntimeException caused by readl lock during preDelete is ignored
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-885'>NUCRDBMS-885</a>] -         Selecting a map value not working when the value has a Map field in it
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.1.0.M3

__Apr 4th 2015__ : _Version 4.1 Milestone 3_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1282'>NUCCORE-1282</a>] -         Allow a query to be registered as a named query
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1290'>NUCCORE-1290</a>] -         Support JPQL &quot;Simple CASE expression&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-85'>NUCAPIJDO-85</a>] -         Ability to save a (created) query as a named query for later use
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-295'>NUCJPA-295</a>] -         Allow a query to be registered as a named query
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-301'>NUCJPA-301</a>] -         Implement CriteriaBuilder &quot;selectSimpleCase&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-19'>NUCREST-19</a>] -         Support persistence of Maps - see JSON plugin
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-20'>NUCREST-20</a>] -         Support persistence of array fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-23'>NUCREST-23</a>] -         Support GZIP encoding on GET response
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-866'>NUCRDBMS-866</a>] -         Support JPQL KEY, VALUE
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-873'>NUCRDBMS-873</a>] -         Support specification of type-converter-name on &lt;element&gt;, &lt;key&gt;, &lt;value&gt;
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-86'>NUCAPIJDO-86</a>] -         Make PersistenceManager support AutoCloseable (JDK1.7+)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-87'>NUCAPIJDO-87</a>] -         Make JDOQuery implement AutoCloseable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-17'>NUCREST-17</a>] -         Allow specification of maxFetchDepth on GET requests
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-871'>NUCRDBMS-871</a>] -         Select of KEY or VALUE only selects the &quot;id&quot; of the key/value class currently, but should select the FetchPlan
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-872'>NUCRDBMS-872</a>] -         JPQL : Support for parameters in FROM &quot;ON&quot; clause
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-874'>NUCRDBMS-874</a>] -         Upgrade to HikariCP 2.3.5 and add some properties
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1284'>NUCCORE-1284</a>] -         Move AbstractSQLQuery across to RDBMS plugin since no other datastore supports &quot;SQL&quot; in the same way
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1287'>NUCCORE-1287</a>] -         Enhancement of persistent properties (getter/setter) does not cope with subclasses overriding getter/setter (and generic type of collection)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1289'>NUCCORE-1289</a>] -         Support parsing of JPQL &quot;KEY(myMap).field&quot; (ditto VALUE)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1291'>NUCCORE-1291</a>] -         Support compilation of JPQL queries with HAVING containing subquery
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-299'>NUCJPA-299</a>] -         PluralAttributeImpl.getElementType returns null for a Map, but should return something
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-300'>NUCJPA-300</a>] -          Implement CriteriaBuilder &quot;selectCase&quot; methods
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-21'>NUCREST-21</a>] -         Should not need to specify &quot;class&quot; in related object when sending PUT/POST
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-862'>NUCRDBMS-862</a>] -         Move AbstractSQLQuery across to RDBMS plugin since no other datastore supports &quot;SQL&quot; in the same way
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-864'>NUCRDBMS-864</a>] -         Support persisting a java.util.Calendar as jdbc-type=&quot;DATE&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-865'>NUCRDBMS-865</a>] -         Support persisting a java.util.Calendar as jdbc-type=&quot;TIME&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-870'>NUCRDBMS-870</a>] -         Consider upgrading cascade handling to process the forming of relations if elements/keys/values are present but no cascade set 
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1286'>NUCCORE-1286</a>] -         Check for setter of a persistent property doesn't allow for it being in superclass
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1288'>NUCCORE-1288</a>] -         Annotations for persistent properties are sometimes not processed leading to handling as persistable field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-284'>NUCJPA-284</a>] -         DataNucleus org.datanucleus.api.jpa.criteria.FromImpl.java class has a bug and hence a slightly complex two-level embedded query failed
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-296'>NUCJPA-296</a>] -         Use of EntityGraph with multiple levels only respects top level, subgraphs are stored with null fetchGroupName and discarded
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-16'>NUCREST-16</a>] -         GET using &quot;id&quot; and specified fetchGroup doesn't necessarily respect fetchGroup on return
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-22'>NUCJODATIME-22</a>] -         Difference in persistence of LocalDate when persisting to DATE column from 3.2
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-861'>NUCRDBMS-861</a>] -         Query using FetchPlan, and with maxFetchDepth set to != 1 will always just pull in candidate and next level
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-867'>NUCRDBMS-867</a>] -         Error in JDOQL Map.get handling for key stored in value table or value stored in key table cases
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-869'>NUCRDBMS-869</a>] -         NPE when using on condition with KEY
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-875'>NUCRDBMS-875</a>] -         UUIDMapping can NPE on initialize if creating as reference to a &quot;pk&quot; UUIDMapping
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.1.0.M2

__Mar 9th 2015__ : _Version 4.1 Milestone 2_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1275'>NUCCORE-1275</a>] -         Add method DataNucleusEnhancer.addPersistenceUnit(PersistenceUnitMetaData) for dynamically created persistence units
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-290'>NUCJPA-290</a>] -         Provide access to other value generators not in scope of JPA spec
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1278'>NUCCORE-1278</a>] -         Persistence property &quot;datanucleus.findObject.typeConversion&quot; should be overrideable on PM/EM basis
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1279'>NUCCORE-1279</a>] -         Support specification of &quot;comparator-name&quot; via extensions on the field rather than just on collection metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1280'>NUCCORE-1280</a>] -         Move all class/member level metadata extensions to &quot;public static final String&quot; fields in org.datanucleus.metadata.MetaData
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-84'>NUCAPIJDO-84</a>] -         Make use of ConcurrentHashMap for pm cache now that we support JDK1.7+ only
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-293'>NUCJPA-293</a>] -         Make use of ConcurrentHashMap for persistence unit metadata now that we support JDK1.7+ only
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-153'>NUCMONGODB-153</a>] -         Support query of 1-1/N-1 reference compared to relation object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-158'>NUCMONGODB-158</a>] -         Cater for query structure like &quot;field == param&quot; or &quot;field == literal&quot; and the field uses a TypeConverter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-160'>NUCMONGODB-160</a>] -         java.sql.Time, java.sql.Date are being stored as String when could use &quot;date&quot; Mongo type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-161'>NUCMONGODB-161</a>] -         Support retrieval of interface fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-852'>NUCRDBMS-852</a>] -         Support query fetch of Collection/Map/Array fields when serialised (i,e stored in single column of owner table).
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-858'>NUCRDBMS-858</a>] -         Support NUCCORE-1280
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-14'>NUCJODATIME-14</a>] -         Extend Joda time support for LocalDateTime
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1271'>NUCCORE-1271</a>] -         Drop targetClass from org.datanucleus.identity.SingleFieldId since duplicates targetClassName
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1272'>NUCCORE-1272</a>] -         Rename options for &quot;datanucleus.valuegeneration.transactionAttribute&quot; to be NEW and EXISTING
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1274'>NUCCORE-1274</a>] -         Support CASE / IF/ELSE &quot;when&quot; conditions that are not completely defined (i.e depend on previous when conditions)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1276'>NUCCORE-1276</a>] -         Remove refs to javax.jdo properties/methods
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1281'>NUCCORE-1281</a>] -         Provide handling for Enum &quot;value getter method&quot; so it can be used by all store plugins (currently in RDBMS only)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-82'>NUCAPIJDO-82</a>] -         Implement JDK1.7 JDOConnectionJDBCImpl methods since using JDK1.7+ now
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-83'>NUCAPIJDO-83</a>] -         Support NUCCORE-1271
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-291'>NUCJPA-291</a>] -         Allow direct access to java.sql.Connection via EM.unwrap when using RDBMS
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-292'>NUCJPA-292</a>] -         Remove use of javax.jdo.option.transactiontype : only need internal DataNucleus property with JPA
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-294'>NUCJPA-294</a>] -         Implement Criteria FetchImpl.fetch methods so we can chain fetches
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-850'>NUCRDBMS-850</a>] -         Change &quot;datanucleus.multivaluedFetch&quot; to be RDBMS specific and specifiable globally
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-851'>NUCRDBMS-851</a>] -         Add check on CASE &quot;action&quot; expression types for consistency
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-853'>NUCRDBMS-853</a>] -         HikariCP : Make leakThreshold, maxLifetime configurable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-854'>NUCRDBMS-854</a>] -         Support NUCCORE-1274
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-855'>NUCRDBMS-855</a>] -         Drop support for &quot;adapter-column-name&quot; for overriding join table order column name. Just use &lt;order&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-860'>NUCRDBMS-860</a>] -         Push Enum &quot;value getter method&quot; handling down into datanucleus-core so we can make it available for other store plugins
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1277'>NUCCORE-1277</a>] -         DeleteFieldManager &quot;nullBidirIfNotDependent&quot; handling incomplete when dealing with N-1 relationships
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-80'>NUCEXCEL-80</a>] -         Make sure StoreData is populated before using fetchObject(...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-81'>NUCEXCEL-81</a>] -         Numeric object wrapper fields can fail on retrieval due to falling back to TypeConverter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-82'>NUCEXCEL-82</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-84'>NUCEXCEL-84</a>] -         Persist of object with composite PK results in blank row in worksheet before the next inserted object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-85'>NUCEXCEL-85</a>] -         Classes without table (abstract) can cause NPE if you try to do query over them
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-86'>NUCEXCEL-86</a>] -         Fetch of relation fields doesn't cater for the related object being deleted elsewhere. Copy Cassandra plugin handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-60'>NUCODF-60</a>] -         Make sure StoreData is populated before using fetchObject(...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-61'>NUCODF-61</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-62'>NUCODF-62</a>] -         Classes without table (abstract) can cause NPE if you try to do query over them
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-63'>NUCODF-63</a>] -         Fetch of relation fields doesn't cater for the related object being deleted elsewhere. Copy Cassandra plugin handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-154'>NUCMONGODB-154</a>] -         MongoUtils.getClassNameForIdentity should use StoreManager to get subclasses so they get registered
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-156'>NUCMONGODB-156</a>] -         Persisting array of char, byte etc can fail on retrieval since stored as List&lt;String&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-157'>NUCMONGODB-157</a>] -         Query of class with field using multiple-column TypeConverter only selects the first column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-163'>NUCMONGODB-163</a>] -         Creattion of index/unique is incorrect. Should set name if not set, and should use class name in generated name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-54'>NUCJSON-54</a>] -         Classes without table (abstract) can cause NPE if you try to do query over them
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-55'>NUCJSON-55</a>] -         Fetch of relation fields doesn't cater for the related object being deleted elsewhere. Copy Cassandra plugin handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-848'>NUCRDBMS-848</a>] -         &quot;max&quot; value generator provides wrong id if 2 objects are persisted in one transaction  
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-856'>NUCRDBMS-856</a>] -         ViewImpl seems to have regression in validate() method
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-857'>NUCRDBMS-857</a>] -         Typo from NUCRDBMS-838
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.1.0.M1

__Jan 19th 2015__ : _Version 4.1 Milestone 1_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-253'>NUCRDBMS-253</a>] -         DB2 : SerializeRead/useUpdateLock &quot;for update&quot; shouldn't have been appended to all selects
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1269'>NUCCORE-1269</a>] -         Map wrapper SCOs have inefficient initialise method when updating (setXXXField). Create efficient logic for working out changed elements
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1270'>NUCCORE-1270</a>] -         Add ExecutionContext.getLevel1Cache for symmetry with NucleusContext and Level2Cache
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-81'>NUCAPIJDO-81</a>] -         JDO class load listener : catch any exceptions loading the class and log rather than rethrowing
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-845'>NUCRDBMS-845</a>] -         Handling of case expression should check for non-Boolean conditional expression, and convert to CaseNumericExpression if possible
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1229'>NUCCORE-1229</a>] -         Add ExecutionContextReference interface, and use it in bytecode enhancement contract
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1238'>NUCCORE-1238</a>] -         Set of container field of a persistable doesn't make use of the old value when updating the field; should use the old value to decide what to do
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1260'>NUCCORE-1260</a>] -         Standard collection/map wrappers remove() does cascade delete direct, yet should check if queued operations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1263'>NUCCORE-1263</a>] -         Add OperationQueue operations for persists, removes and updates
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1265'>NUCCORE-1265</a>] -         Move StateManagerImpl.getEmbeddedOwners to ExecutionContext
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1266'>NUCCORE-1266</a>] -         Separate embedded owner field setting code from StateManagerImpl.wrapSCOField
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1267'>NUCCORE-1267</a>] -         SCOCollection/SCOMap updateEmbeddedXXX should take in makeDirty flag
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-844'>NUCRDBMS-844</a>] -         JDOQL/JPQL : Allow &quot;expr = {param}&quot; to have flexibility when the param is null so that can map to &quot;IS NULL&quot; or &quot;= null&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-846'>NUCRDBMS-846</a>] -         Support boolean Case expressions (just like we do numeric Case expressions)
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1264'>NUCCORE-1264</a>] -         Loss of all collection elements on add+remove when playing around with SCO wrapper of an object that was subsequently made HOLLOW
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-843'>NUCRDBMS-843</a>] -         MapMapping.postUpdate when setting to null doesn't clear the backing store but should
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-847'>NUCRDBMS-847</a>] -         JDOQL statement with multi-tenant PersistenceManager
</li>
</ul>

