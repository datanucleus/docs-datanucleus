<head><title>AccessPlatform 5.0</title></head>

#Release Notes for DataNucleus AccessPlatform v5.0

The 5.0 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 5.0_ includes the following over 4.2

<ul>
<li>Minimum java requirement increased to Java8.</li>
<li>Support added for Java8 Optional</li>
<li>Support added for HBase v1.1 (hbase-client)</li>
<li>Support added for Neo4j v2.3</li>
<li>Support added for MongoDB java driver v3.0</li>
<li>PostgreSQL : support for persisting collection/array of strings/ints into "array" column type</li>
</ul>

<br/>



# DataNucleus AccessPlatform 5.0.0.M1

__Jan 18th 2016__ : _Version 5.0 Milestone 1_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1339'>NUCCORE-1339</a>] -         Support for non-JDK containers
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1342'>NUCCORE-1342</a>] -         Support for single element collections (java.util.Optional)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1343'>NUCCORE-1343</a>] -         Allow to specify default nullability for fields using a configuration property.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1350'>NUCCORE-1350</a>] -         Extend NUCCORE-1344 to allow LEFT JOIN FETCH
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1354'>NUCCORE-1354</a>] -         Add support for JPQL &quot;INSERT&quot; queries (vendor extension)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1358'>NUCCORE-1358</a>] -         Allow JPQL to exclude subclasses of the candidate
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-115'>NUCAPIJDO-115</a>] -         Support java.time types in JDO Typesafe
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-326'>NUCJPA-326</a>] -         Support JPA 2.1 Tuple/TupleElement
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-328'>NUCJPA-328</a>] -         Make EntityManagerFactory, EntityManager implement AutoCloseable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-939'>NUCRDBMS-939</a>] -         Support parameters in SELECT clause, particularly when as part of subqueries
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-944'>NUCRDBMS-944</a>] -         Support polymorphic joins when using UNION, so only apply to particular UNIONs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-954'>NUCRDBMS-954</a>] -         MySQL : allow setting the COLLATION and CHARACTER SET of any tables that are created
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-958'>NUCRDBMS-958</a>] -         Firebird supports date functions using EXTRACT(...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-970'>NUCRDBMS-970</a>] -         SQLStatement needs a way of generation where we don't use table aliases, and just use table names
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-976'>NUCRDBMS-976</a>] -         JPQL : BULK INSERT query support
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-977'>NUCRDBMS-977</a>] -         Support persisting a Collection/Map using a TypeConverter for the whole field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-983'>NUCRDBMS-983</a>] -         Support SAP &quot;SQLAnywhere&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-988'>NUCRDBMS-988</a>] -         PostgreSQL : Support JDBC type of ARRAY allowing array and Collection fields to be persisted to it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-989'>NUCRDBMS-989</a>] -         Support embedded object with field stored in join table
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-996'>NUCRDBMS-996</a>] -         JDOQL : when invoking a method on a type that uses a converter, if the method doesn't exist on the type, try on the converted-to type
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
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-111'>NUCAPIJDO-111</a>] -         ExpressionImpl has package variables, should be protected to allow extension in other packages
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-935'>NUCRDBMS-935</a>] -         SQLStatement : change handling of selects to retain SQLText until statement generation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-945'>NUCRDBMS-945</a>] -         SQLStatement needs more flexibility with joins; apply to just one union, pass in join type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-951'>NUCRDBMS-951</a>] -         Index auto creation : detect reuse of fields so we don't try to duplicate indexes
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
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-971'>NUCRDBMS-971</a>] -         SQLite doesn't provide explicit support for putting nulls last, but can use &quot;{col} IS NULL, {col}&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-972'>NUCRDBMS-972</a>] -         View creation : skip any token that is a &quot;comment&quot; since some RDBMS don't handle that
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-973'>NUCRDBMS-973</a>] -         Delete tables processing : goes off and calls DatabaseMetaData.getColumns for detection of table existence but could just get table type (quicker!)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-978'>NUCRDBMS-978</a>] -         Subclass SQLStatement for DeleteStatement, UpdateStatement
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-980'>NUCRDBMS-980</a>] -         Improve method to determine type of ValueGenerator to use reflection and getActualTypeArguments
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-984'>NUCRDBMS-984</a>] -         Query generation can add order clauses to SELECT but doesn't check if they are already present; should do
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-991'>NUCRDBMS-991</a>] -         Support for fetch of ReferenceMapping field when there is a single implementation and using FK
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-994'>NUCRDBMS-994</a>] -         JPQL : &quot;elem IN collectionField&quot; is invalid syntax but we could map internally as &quot;elem MEMBER OF collectionField&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-99'>NUCHBASE-99</a>] -         Lack of current HBase support (newest supported version is 0.94)
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1346'>NUCCORE-1346</a>] -         JDO 3.2 requires change to behaviour at close of EC with active transaction. Make it configurable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1348'>NUCCORE-1348</a>] -         Extend NUCCORE-1338 to EmbeddedMetaData
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1360'>NUCCORE-1360</a>] -         Support PK field conversions for types Currency, TimeZone, UUID
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1361'>NUCCORE-1361</a>] -         Provide ValueGenerator that generates UUID objects rather than String
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1365'>NUCCORE-1365</a>] -         NucleusLogger : provide access to the underlying Logger for a NucleusLogger
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1367'>NUCCORE-1367</a>] -         Add method to ObjectProvider to return if the version is loaded
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-113'>NUCAPIJDO-113</a>] -         Allow addInstanceLifecycleListener/removeInstanceLifecycleListener usage until first PM is obtained
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-322'>NUCJPA-322</a>] -         Support AttributeConverter on a collection field to be for the whole field not just the element
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-930'>NUCRDBMS-930</a>] -         Extract &quot;lock-for-update&quot; extension of SQLStatement into &quot;public static final&quot; variable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-937'>NUCRDBMS-937</a>] -         Abstract out ComponentInfo for improved handling of backing store with reference components
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-946'>NUCRDBMS-946</a>] -         Add RIGHT_OUTER_JOIN as option in DatastoreAdapter that can be unsupported (SQLite)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-949'>NUCRDBMS-949</a>] -         Support date/time methods on SQLite
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-957'>NUCRDBMS-957</a>] -         Firebird v2 requires use of SUBSTRING for substring of VARCHAR fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-960'>NUCRDBMS-960</a>] -         Disable value generator &quot;uuid-string&quot; for PostgreSQL since main charsets don't handle it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-967'>NUCRDBMS-967</a>] -         SQLite doesn't support &quot;ALL|ANY|SOME {subquery}&quot; keyword constructs, so throw exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-968'>NUCRDBMS-968</a>] -         SQLite LOCATE / String.indexOf should use INSTR(x,y) rather than LOCATE
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-969'>NUCRDBMS-969</a>] -         SQLite DELETE / UPDATE JPQL should not use alias since these are not supported with SQLite
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-975'>NUCRDBMS-975</a>] -         Provide access to RDBMSQueryCompilation, and to the SQLStatement(s) that the compilation is made up of.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-998'>NUCRDBMS-998</a>] -         Prevent SortedSet (and subclasses) be allocated a ListXXXStore since needs unsorted
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-999'>NUCRDBMS-999</a>] -         Support date/time methods on SQLite
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-164'>NUCMONGODB-164</a>] -         Upgrade to MongoDB v3.x
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-165'>NUCMONGODB-165</a>] -         Make sure &quot;ownerMmd&quot; is set for FetchFieldManager when embedded, add TODO to resolve
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-56'>NUCNEOFORJ-56</a>] -         Upgrade to Neo4j v2.3
</li>
</ul>

## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1349'>NUCCORE-1349</a>] -         JDOQL/JPQL parse of BigInteger value is parsed internally to be Long and loses precision
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1351'>NUCCORE-1351</a>] -         IN predicate unexpectedly gets transformed to EQ predicate
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1355'>NUCCORE-1355</a>] -         JPQLSingleStringParser has missing trimRight handling (typo in trimLeft)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1356'>NUCCORE-1356</a>] -         Metadata processing moves ColumnMetaData to ElementMetaData is not embedded/serialised but should also allow for full field type converter case
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1362'>NUCCORE-1362</a>] -         Persistable elements contained in Collection/Map that is serialised (whole field) are not detached/attached correctly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1364'>NUCCORE-1364</a>] -         L2 cache of persistable arrays creates incorrect array type for caching
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1366'>NUCCORE-1366</a>] -         AbstractMemberMetaData.getClassName(false) can return fully qualified name in some situations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-112'>NUCAPIJDO-112</a>] -         @Convert specified on field doesn't always get processed. Works fine when using @Persistent(converter=...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-319'>NUCJPA-319</a>] -         JPA 2.1 has bug in EntityGraph method signatures for Attribute generic type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-327'>NUCJPA-327</a>] -         Handling of UniqueConstraint/Index &quot;name&quot; is incorrect
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-329'>NUCJPA-329</a>] -         JPA MetaModel doesn't cater correctly for List&lt;nonPC&gt;, and sets to CollectionAttributeImpl instead of ListAttributeImpl
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-325'>NUCRDBMS-325</a>] -         JDOQL : &quot;instanceof&quot; with inheritance generates incorrect query when using union, in query FILTER
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-933'>NUCRDBMS-933</a>] -         Wrong sql query generated when using type function with joined inheritance without discriminators
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-934'>NUCRDBMS-934</a>] -         Exception about missing field when using (TYPE function with) TABLE_PER_CLASS strategy
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-938'>NUCRDBMS-938</a>] -         Column creation for overridden field can try to create as IDENTITY when no value strategy defined!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-941'>NUCRDBMS-941</a>] -         Selecting attribute from element collection map value produces wrong sql
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
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-965'>NUCRDBMS-965</a>] -         Use of COMPLETE_TABLE doesn't seem to allow override of PK field column names
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-974'>NUCRDBMS-974</a>] -         Oracle, Firebird require that when using GROUP BY, all non-aggregate SELECT components are in the GROUP BY clause
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-979'>NUCRDBMS-979</a>] -         Query returning result of COMPLETE_TABLE strategy where root class has no table causes exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-981'>NUCRDBMS-981</a>] -         Support NUCCORE-1362
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-985'>NUCRDBMS-985</a>] -         SELECT statement generation handling of ordering when multiple cols per order expression should apply quoting as final step but doesnt
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-986'>NUCRDBMS-986</a>] -         Creation of mapping in some cases misses the MultiColumnConverter case and doesnt use TypeConverterMultiMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-987'>NUCRDBMS-987</a>] -         UpdateRequest : only add the version field if it is not present in the passed list of modified fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-992'>NUCRDBMS-992</a>] -         Name of candidate key (unique) on join table is not respected
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-995'>NUCRDBMS-995</a>] -         TypeConverterMapping.getJavaType is incorrect when roleForMember is set
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-98'>NUCHBASE-98</a>] -         Cannot auto-create tables without deactivating sanity checks
</li>
</ul>

