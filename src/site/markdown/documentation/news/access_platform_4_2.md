<head><title>AccessPlatform 4.2</title></head>

#Release Notes for DataNucleus AccessPlatform v4.2

The 4.2 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 4.2_ includes the following over 4.1

<ul>
<li>Remove support for DataNucleus "JDO Typesafe Query" API.</li>
<li>Add support for JDO 3.2 JDOQLTypedQuery API.</li>
<li>Add support for JDO 3.2 AttributeConverter</li>
<li>Add support for JDO 3.2 Query API enhancements</li>
<li>Add support for JDO 3.2 JDOQL bitwise operations</li>
<li>Remove support for methods that were dropped in JDO 3.2</li>
</ul>

<br/>

# DataNucleus AccessPlatform 4.2.7

__Aug 2nd 2016__ : _Version 4.2.7_ includes the following changes

## Enhancements

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/25'>datanucleus-api-jdo-25</a>] - JDOPersistenceManager.close should null the pmf</li>
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


# DataNucleus AccessPlatform 4.2.6

__Jun 6th 2016__ : _Version 4.2.6_ includes the following changes

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
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/16'>datanucleus-api-jdo-16</a>] - Bean Validation : don't fire off validation on prePersist and preStore, just on one</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/23'>datanucleus-api-jpa-23</a>] - Criteria in(...).not() is ignoring the NOT in the generic compilation (and generated SQL)</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/20'>datanucleus-api-jpa-20</a>] - Bean Validation : don't fire off validation on prePersist and preStore, just on one</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/49'>datanucleus-rdbms-49</a>] - Bulk fetch has bug when trying to handle array case, assumes it is a Collection resulting in NPE</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.2.5

__Apr 7th 2016__ : _Version 4.2.5_ includes the following changes

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


# DataNucleus AccessPlatform 4.2.4

__Feb 20th 2016__ : _Version 4.2.4_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-23'>NUCJAVAEIGHT-23</a>] -         Backport of NUCCORE-1377
</li>
</ul>

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
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-22'>NUCJAVAEIGHT-22</a>] -         Backport of NUCCORE-1376
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1009'>NUCRDBMS-1009</a>] -         Parameters in group by expressions are not set on the JDBC statement
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 4.2.3

__Jan 13th 2016__ : _Version 4.2.3_ includes the following changes

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

# DataNucleus AccessPlatform 4.2.2

__Nov 27th 2015__ : _Version 4.2.2_ includes the following changes

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



# DataNucleus AccessPlatform 4.2.1

__Nov 6th 2015__ : _Version 4.2.1_ includes the following changes

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
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-112'>NUCAPIJDO-112</a>] -         @Convert specified on field doesn't always get processed. Works fine when using @Persistent(converter=...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-974'>NUCRDBMS-974</a>] -         Oracle, Firebird require that when using GROUP BY, all non-aggregate SELECT components are in the GROUP BY clause
</li>
</ul>

<br/>



# DataNucleus AccessPlatform 4.2.0.RELEASE

__Oct 9th 2015__ : _Version 4.2 RELEASE_ includes the following changes

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
<li>[<a href='http://issues.datanucleus.org/browse/NUCJDOQUERY-21'>NUCJDOQUERY-21</a>] -         Support persistable classes that are static inline
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



# DataNucleus AccessPlatform 4.2.0.M3

__Sept 15th 2015__ : _Version 4.2 Milestone 3_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1344'>NUCCORE-1344</a>] -         JPQL Compilation : support limited polymorphic join
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-108'>NUCAPIJDO-108</a>] -         Support StringExpression.matches(String)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-932'>NUCRDBMS-932</a>] -         Support polymorphic joins for entities
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-939'>NUCRDBMS-939</a>] -         Support parameters in SELECT clause, particularly when as part of subqueries
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-18'>NUCJAVAEIGHT-18</a>] -         Support java.time types in JDO Typesafe
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-111'>NUCAPIJDO-111</a>] -         ExpressionImpl has package variables, should be protected to allow extension in other packages
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-935'>NUCRDBMS-935</a>] -         SQLStatement : change handling of selects to retain SQLText until statement generation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJDOQUERY-20'>NUCJDOQUERY-20</a>] -         Support for java.time LocalXXX types using java8 plugin
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1346'>NUCCORE-1346</a>] -         JDO 3.2 requires change to behaviour at close of EC with active transaction. Make it configurable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1348'>NUCCORE-1348</a>] -         Extend NUCCORE-1338 to EmbeddedMetaData
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-109'>NUCAPIJDO-109</a>] -         JDO 3.2 : Close of PM with active tx should rollback the transaction rather than throw exception (JDO &lt;= 3.1 behaviour)
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1345'>NUCCORE-1345</a>] -         Unable to use version tag on ORM file without having to define the strategy again
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1349'>NUCCORE-1349</a>] -         JDOQL/JPQL parse of BigInteger value is parsed internally to be Long and loses precision
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-110'>NUCAPIJDO-110</a>] -         Query.saveAsNamedQuery should save under candidate+name if we have one, otherwise just name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-936'>NUCRDBMS-936</a>] -         Addendum to NUCRDBMS-917. Dont create indexes when not indexable column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-938'>NUCRDBMS-938</a>] -         Column creation for overridden field can try to create as IDENTITY when no value strategy defined!
</li>
</ul>

<br/>




# DataNucleus AccessPlatform 4.2.0.M2

__Aug 16th 2015__ : _Version 4.2 Milestone 2_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1335'>NUCCORE-1335</a>] -         Add ability to set JDOQL/JPQL strictness on query compilation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1336'>NUCCORE-1336</a>] -         JPQL : support CURRENT_TIMESTAMP(), CURRENT_DATE(), CURRENT_TIME()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1337'>NUCCORE-1337</a>] -         JPQL : support COUNT(*)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-101'>NUCAPIJDO-101</a>] -         Add support for JDOQLTypedQuery NumericExpression.neg()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-102'>NUCAPIJDO-102</a>] -         Add support for JDOQLTypedQuery NumericExpression.com()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-103'>NUCAPIJDO-103</a>] -         Add support for JDOQLTypedQuery BooleanExpression.neg()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-104'>NUCAPIJDO-104</a>] -         Add support for JDOQLTypedQuery CharacterExpression.neg() and com()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-107'>NUCAPIJDO-107</a>] -         Add support for JDOQLTypedQuery NumericExpression.bAnd, bOr, bXor
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
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-100'>NUCAPIJDO-100</a>] -         Some NumericExpression atan, sqrt methods have copy-paste errors for the method to invoke
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



# DataNucleus AccessPlatform 4.2.0.M1

__Jul 14th 2015__ : _Version 4.2 Milestone 1_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1325'>NUCCORE-1325</a>] -         Support Java generic TypeVariable where declared by class generic type bounds
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-93'>NUCAPIJDO-93</a>] -         Support specification of &quot;default&quot; TypeConverter via PMF properties
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-95'>NUCAPIJDO-95</a>] -         Support JDO 3.2 AttributeConverter specification via annotations/XML/API
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

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-99'>NUCAPIJDO-99</a>] -         JDOQLTypedQuery : change toString to include any subquery in the string
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1323'>NUCCORE-1323</a>] -         Add generics for element, key, value to all wrappers and backing stores
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1324'>NUCCORE-1324</a>] -         Bump repackaged ASM to v5.0.4 from 5.0.3
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-33'>NUCAPIJDO-33</a>] -         JDO3.2 : use javax.jdo.query interfaces when typesafe adopted by JDO
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-94'>NUCAPIJDO-94</a>] -         Build against groupId=org.datanucleus artifactId=javax.jdo version=3.2.0-m1-SNAPSHOT
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-97'>NUCAPIJDO-97</a>] -         PMF.addFetchGroups, PMF.removeFetchGroups, PMF.registerMetadata, Query.saveAsNamedQuery should check for permission &quot;getMetadata&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-98'>NUCAPIJDO-98</a>] -         Support XML XSD/DTD specifications of xmlns.jcp.org and use local copy for those
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

