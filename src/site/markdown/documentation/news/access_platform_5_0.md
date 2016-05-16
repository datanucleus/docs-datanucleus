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


# DataNucleus AccessPlatform 5.0.0.M4

__May 17th 2016__ : _Version 5.0 Milestone 4_ includes the following changes

## Enhancements

<ul>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/74">datanucleus-core-74</a>] - In-memory evaluation : if result fails, throw exception</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/72">datanucleus-core-72</a>] - CompleteClassTable : cater for columnMetaData on collection element when intended for field</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/69">datanucleus-core-69</a>] - Federation : cater for simple use-cases of identity</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/66">datanucleus-core-66</a>] - SchemaTool : Support "ignoreMetaDataForMissingClasses"</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/55">datanucleus-core-55</a>] - Support method MONTH_JAVA in-memory</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/54">datanucleus-core-54</a>] - Add in-memory evaluation support for Optional.orElse</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-cassandra/issues/16">datanucleus-cassandra-16</a>] - Add ability to check for existence of records when inserting</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-cassandra/issues/15">datanucleus-cassandra-15</a>] - Support JPA @OrderBy</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-cassandra/issues/2">datanucleus-cassandra-2</a>] - Support JPA @EmbeddedId</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-excel/issues/8">datanucleus-excel-8</a>] - Support JPA @OrderBy</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-hbase/issues/19">datanucleus-hbase-19</a>] - Support CompoundIdentity</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-hbase/issues/18">datanucleus-hbase-18</a>] - Support JPA @OrderBy</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-hbase/issues/17">datanucleus-hbase-17</a>] - Support JPA @EmbeddedId</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-json/issues/5">datanucleus-json-5</a>] - Support JPA @OrderBy</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-mongodb/issues/17">datanucleus-mongodb-17</a>] - Support JPA @OrderBy</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-odf/issues/6">datanucleus-odf-6</a>] - Support JPA @OrderBy</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-rdbms/issues/48">datanucleus-rdbms-48</a>] - Rename of backing store variables so clearer the intent</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-rdbms/issues/47">datanucleus-rdbms-47</a>] - Oracle supports specifying the PRIMARY KEY in the CREATE TABLE statement</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-rdbms/issues/46">datanucleus-rdbms-46</a>] - jdbc timeouts are not propagated for SQL queries</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-rdbms/issues/37">datanucleus-rdbms-37</a>] - Add support for java.util.Optional JDOQL "orElse" method</li>
</ul>

## Bugs

<ul>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/77">datanucleus-core-77</a>] - NamingFactory do not cater for unique index name for DISCRIMINATOR_COLUMN</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/75">datanucleus-core-75</a>] - CompleteClassTable : mark embedded PK columns as being part of PK</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-core/issues/67">datanucleus-core-67</a>] - OperationQueue : performAll for backing store should only process for the specified ObjectProvider</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-api-jdo/issues/14">datanucleus-api-jdo-14</a>] - Bean Validation : don't fire off validation on prePersist and preStore, just on one</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-api-jpa/issues/19">datanucleus-api-jpa-19</a>] - Bean Validation : don't fire off validation on prePersist and preStore, just on one</li>
<li>[<a href="https://github.com/datanucleus/datanucleus-rdbms/issues/50">datanucleus-rdbms-50</a>] - Bulk fetch has bug when trying to handle array case, assumes it is a Collection resulting in NPE</li>
</ul>

<br/>


# DataNucleus AccessPlatform 5.0.0.M3

__Apr 8th 2016__ : _Version 5.0 Milestone 3_ includes the following changes

## New Feature

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/57'>datanucleus-core-57</a>] -         Add support for JPQL FROM join to a new &quot;root&quot; with ON condition
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/58'>datanucleus-core-58</a>] -         CompleteClassTable and MemberColumnMapping do not support collection element or map key/value conversion. Need to add
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/56'>datanucleus-core-56</a>] -         Add mechanism whereby if there is metadata for a class that is not in the classpath we can just ignore it
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/5'>datanucleud-api-jdo-5</a>] -         Add support for javax.jdo.query.OptionalExpression
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/7'>datanucleus-api-jpa-7</a>] -         Support NonDurable Identity as vendor extension
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-cassandra/issues/9'>datanucleus-cassandra-9</a>] -         Support for java.util.Optional
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-cassandra/issues/10'>datanucleus-cassandra-10</a>] -         Support persistence of serialised PC fields
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-cassandra/issues/11'>datanucleus-cassandra-11</a>] -         Support use of TypeConverter on Collection element, Map key and Map value
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/9'>datanucleus-hbase-9</a>] -         Support for java.util.Optional
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/10'>datanucleus-hbase-10</a>] -         Support use of TypeConverter on Collection element, Map key and Map value
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/7'>datanucleus-hbase-7</a>] -         Persist relation fields as &quot;persistableId&quot; like with MongoDB, Excel, ODF, Cassandra, Neo4j, JSON etc
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-excel/issues/5'>datanucleus-excel-5</a>] -         Support for java.util.Optional
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-json/issues/3'>datanucleus-json-3</a>] -         Support for java.util.Optional
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-mongodb/issues/14'>datanucleus-mongodb-14</a>] -         Support inherited embedded Map keys/values
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-mongodb/issues/15'>datanucleus-mongodb-15</a>] -         Support for java.util.Optional
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-mongodb/issues/13'>datanucleus-mongodb-13</a>] -         Support use of TypeConverter on Collection element, Map key and Map value
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-neo4j/issues/13'>datanucleus-neo4j-13</a>] -         Support for java.util.Optional
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-odf/issues/5'>datanucleus-odf-4</a>] -         Support for java.util.Optional
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/38'>datanucleus-rdbms-38</a>] -         Add support for JPQL FROM join to a new &quot;root&quot; with ON condition
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-jdo-query/issues/2'>datanucleus-jdo-query-2</a>] -         Add support for javax.jdo.query.OptionalExpression
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMAVEN-52'>NUCMAVEN-52</a>] -         Support &quot;datanucleus.metadata.ignoreMetaDataForMissingClasses&quot; via enhancer
</li>
</ul>

## Improvement

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/6'>datanucleus-hbase-6</a>] -         If attempt to use HBase with IDENTITY value generator it throws an exception. Better to switch to INCREMENT and log warning
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/39'>datanucleus-rdbms-39</a>] -         Collection.contains allows control over variable join/subquery - should allow the same for Map.containsKey, Map.containsValue
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/42'>datanucleus-rdbms-42</a>] -         Collection.contains, Map.containsKey, Map.containsValue can define how a variable is &quot;joined&quot; (subquery or innerjoin) but ought to allow &quot;leftouterjoin&quot; also
</li>
</ul>

## Task

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/59'>datanucleus-core-59</a>] -         Marking a member as &quot;serializable&quot; conflicts with the use of a converter
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/62'>datanucleus-core-62</a>] -         Clean up code around ClassLoaderResolverImpl for JRE classes so matches those in ClassNameConstants
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/60'>datanucleus-core-60</a>] -         Add StoreManager supportedOption for serialized collection element, array element, map key, map value
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/61'>datanucleus-core-61</a>] -         Add converter for conversion from BufferedImage to ByteBuffer
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-cassandra/issues/13'>datanucleus-cassandra-13</a>] -         Support for persisting fields of type BufferedImage
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-cassandra/issues/12'>datanucleus-cassandra-12</a>] -         Complete support for retrieval of byte[] field
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/4'>datanucleus-hbase-4</a>] -         HBaseSchemaHandler hasn't been properly upgraded to HBase 1.x
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/3'>datanucleus-hbase-3</a>] -         HBase fetch of fields doesn't cater for non-persistent fields (transient, transactional)
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/43'>datanucleus-rdbms-43</a>] -         Support for NUCCORE-1395 options
</li>
</ul>

## Bug

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/64'>datanucleus-core-64</a>] -         In-memory evaluation of Optional.get doesn't check for isPresent but should
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/65'>datanucleus-core-65</a>] -         SerializableByteBufferConverter should use wrap/remaining to convert to bytes but doesn't
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-core/issues/63'>datanucleus-core-63</a>] -         In-memory evaluation of MonthDay.getMonthValue and YearMonth.getMonthValue are returning Month object!
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-cassandra/issues/14'>datanucleus-cassandra-14</a>] -         When using converter on field it should SCO wrap the result on retrieval but currently doesn't
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-excel/issues/6'>datanucleus-excel-6</a>] -         Look up of object doesn't cater for PK field being Date stored as String (i.e use of converter)
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-excel/issues/4'>datanucleus-excel-4</a>] -         ExcelCandidateList (query results) should respect FetchPlan of query
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/13'>datanucleus-hbase-13</a>] -         Use of TypeConverter fails on persist since doesn't use the converted value
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/8'>datanucleus-hbase-8</a>] -         Query of NonDurable identity fails, due to unknown type info even though the class is input
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/11'>datanucleus-hbase-11</a>] -         HBase query comparing Enum field with ordinal value (or name) doesn't evaluate
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/5'>datanucleus-hbase-5</a>] -         Hbase plugin doesn't cope with fetch of relation field pointing to object that is no longer present. Should just set relation to null
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/12'>datanucleus-hbase-12</a>] -         Lookup of object when using TypeConverter on PK field fails to find the object
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-mongodb/issues/16'>datanucleus-mongodb-16</a>] -         MongoDB v3.x removes support for using java.sql.* so need to pass in java.util.Date
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-odf/issues/2'>datanucleus-odf-2</a>] -         Look up of object doesn't cater for PK field being Date stored as String (i.e use of converter)
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-odf/issues/3'>datanucleus-odf-3</a>] -         ODFCandidateList (query results) should respect FetchPlan of query
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/41'>datanucleus-rdbms-41</a>] -         NUCRDBMS-1012 updates to join table PK creation were incomplete. Need further improvement
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-rdbms/issues/40'>datanucleus-rdbms-40</a>] -         Insert of array of persistable objects fails to insert join table when cascade not enabled
</li>
</ul>

<br/>


# DataNucleus AccessPlatform 5.0.0.M2

__Mar 15th 2016__ : _Version 5.0 Milestone 2_ includes the following changes

## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1369'>NUCCORE-1369</a>] -         Add in-memory evaluation support for YearMonth.getYear, YearMonth.getMonthValue, MonthDay.getDayOfMonth, MonthDay.getMonthValue, Period.getMonths, Period.getDays, Period.getYears etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1370'>NUCCORE-1370</a>] -         Support conversion from MonthDay to java.sql.Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1371'>NUCCORE-1371</a>] -         Support conversion from YearMonth to java.sql.Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1374'>NUCCORE-1374</a>] -         Provide ability for a store plugin to set the default TypeConverter to use for a java field type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1377'>NUCCORE-1377</a>] -         Support conversion of java.time.Instant to java.util.Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1380'>NUCCORE-1380</a>] -         Support conversion from Duration to Double (secs.nanos)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1383'>NUCCORE-1383</a>] -         JPQL : Support YEAR, MONTH, DAY, HOUR, MINUTE, SECOND with java.time types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1387'>NUCCORE-1387</a>] -         Add in-memory evaluation support for Optional.get, Optional.isPresent
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1388'>NUCCORE-1388</a>] -         Support persistence of java.time.ZonedDateTime as Timestamp / String
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/10'>datanucleus-api-jpa-10</a>] -         Allow shared relation to be specified using single annotation rather than 3 extension annotations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1000'>NUCRDBMS-1000</a>] -         Add support for YearMonth.getYear, YearMonth.getMonthValue, MonthDay.getDayOfMonth, MonthDay.getMonthValue, Period.getMonths, Period.getDays, Period.getYears etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1003'>NUCRDBMS-1003</a>] -         JDOQL : Support Optional.get(), Optional.isPresent() rather than current automatic referral to underlying type
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-jdo-query/issues/3'>datanucleus-jdo-query-3</a>] -         Use LocalDateExpression/LocalTimeExpression/LocalDateTimeExpression from javax.jdo (3.2.0.m4+)
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/7'>datanucleus-api-jdo-7</a>] -         Allow use of jta-data-source/non-jta-data-source from persistence.xml as alternative to standard JDO properties
</li>
</ul>

## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1368'>NUCCORE-1368</a>] -         List of &quot;simple&quot; result classes is very restrictive. Extend to include other commonly used &quot;simple&quot; classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1385'>NUCCORE-1385</a>] -         Query parsing can be improved to better cater for quoting and end of line characters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1389'>NUCCORE-1389</a>] -         java.awt.Color should be in DFG
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-rest/issues/6'>datanucleus-api-rest-6</a>] -         Remove use of NucleusException
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-rest/issues/4'>datanucleus-api-rest-4</a>] -         Change &quot;jdoql&quot; / &quot;jpql&quot; modes so that they take parameter &quot;query&quot; with the encoded query
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-rest/issues/5'>datanucleus-api-rest-5</a>] -         Extract Google AppEngine code into separate classes so we can make user types pluggable
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-rest/issues/7'>datanucleus-api-rest-7</a>] -         Split out code for Google "User" and "Key" classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1001'>NUCRDBMS-1001</a>] -         Oracle supports NVARCHAR but JDBC driver doesn't acknowledge it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1004'>NUCRDBMS-1004</a>] -         Temporal query methods contain significant duplication and need rationalising
</li>
</ul>

## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1353'>NUCCORE-1353</a>] -         org.datanucleus.store.query.Query has short &quot;type&quot; but ought to be enum. Will need all store plugins updating to match
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1372'>NUCCORE-1372</a>] -         Nondurable classes should not be L2 cached, ever.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1373'>NUCCORE-1373</a>] -         CalendarStringConverter/DateStringConverter should implement ColumnLengthDefiningTypeConverter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1376'>NUCCORE-1376</a>] -         Update LocalDateDateConverter, LocalDateTimeDateConverter and LocalTimeDateConverter to use Instant and ZoneId for reliability
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1379'>NUCCORE-1379</a>] -         Dont log about AutoStartMechanism if set to None
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1382'>NUCCORE-1382</a>] -         Change JPQL &quot;MONTH&quot; to evaluate to the month between 1 and 12 (rather than 0 and 11 like now)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1384'>NUCCORE-1384</a>] -         JPQL : Support YEAR, MONTH, DAY, HOUR, MINUTE, SECOND as in-memory evaluation
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/12'>datanucleus-api-jpa-12</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/8'>datanucleus-api-jdo-8</a>] -         Move LocalDateExpression/LocalTimeExpression/LocalDateTimeExpression to javax.jdo
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/6'>datanucleus-api-jdo-6</a>] -         Allow lifecycle state change from HOLLOW to P_NONTRANS when no tx and field is already loaded
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/9'>datanucleus-api-jdo-9</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1005'>NUCRDBMS-1005</a>] -         Merge VersionStringMapping, VersionTimestampMapping into VersionMapping. Same for DiscriminatorMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1006'>NUCRDBMS-1006</a>] -         ClassMapping is no longer needed; use type converter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1007'>NUCRDBMS-1007</a>] -         Apparently need a call to ConnectionFactory.setPool() to avoid log message with DBCP2
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1010'>NUCRDBMS-1010</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-cassandra/issues/8'>datanucleus-cassandra-8</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-excel/issues/7'>datanucleus-excel-7</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/14'>datanucleus-hbase-14</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-json/issues/4'>datanucleus-json-4</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-ldap/issues/10'>datanucleus-ldap-10</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-mongodb/issues/16'>datanucleus-mongodb-12</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-neodatis/issues/1'>datanucleus-neodatis-1</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-neo4j/issues/12'>datanucleus-neo4j-12</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-odf/issues/5'>datanucleus-odf-5</a>] -         Support NUCCORE-1353
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-xml/issues/4'>datanucleus-xml-4</a>] -         Support NUCCORE-1353
</li>
</ul>

## Bug

<ul>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/11'>datanucleus-api-jpa-11</a>] -         If metadata specified using orm.xml only, the entity name is not defaulted
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/9'>datanucleus-api-jpa-9</a>] -         Criteria multiple join with no join alias results in exception
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/8'>datanucleus-api-jpa-8</a>] -         Criteria join to a multiple valued path doesn't work.
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1009'>NUCRDBMS-1009</a>] -         Parameters in group by expressions are not set on the JDBC statement
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1012'>NUCRDBMS-1012</a>] -         Using JPA with a OneToMany field that is a Set with join table doesn't create the PK for the join table, but should
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-1013'>NUCRDBMS-1013</a>] -         JPQL : join to embedded object generates incorrect SQL
</li>
</ul>


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
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/12'>datanucleus-api-jdo-12</a>] -         Support java.time types in JDO Typesafe
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/15'>datanucleus-api-jpa-15</a>] -         Support JPA 2.1 Tuple/TupleElement
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/18'>datanucleus-api-jpa-18</a>] -         Make EntityManagerFactory, EntityManager implement AutoCloseable
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
<li>[<a href='https://github.com/datanucleus/datanucleus-scala/issues/2'>datanucleus-scala-2</a>] -         Support for &quot;Option&quot;
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-scala/issues/1'>datanucleus-scala-1</a>] -         Support for &quot;case&quot; classes as SCOs
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
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/13'>datanucleus-api-jdo-13</a>] -         ExpressionImpl has package variables, should be protected to allow extension in other packages
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
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/16'>datanucleus-hbase-16</a>] -         Lack of current HBase support (newest supported version is 0.94)
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
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/11'>datanucleus-api-jdo-11</a>] -         Allow addInstanceLifecycleListener/removeInstanceLifecycleListener usage until first PM is obtained
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/17'>datanucleus-api-jpa-17</a>] -         Support AttributeConverter on a collection field to be for the whole field not just the element
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
<li>[<a href='https://github.com/datanucleus/datanucleus-mongodb/issues/10'>datanucleus-mongodb-10</a>] -         Upgrade to MongoDB v3.x
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-mongodb/issues/11'>datanucleus-mongodb-11</a>] -         Make sure &quot;ownerMmd&quot; is set for FetchFieldManager when embedded, add TODO to resolve
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-neo4j/issues/11'>datanucleus-neo4j-11</a>] -         Upgrade to Neo4j v2.3
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
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jdo/issues/10'>datanucleus-api-jdo-10</a>] -         @Convert specified on field doesn't always get processed. Works fine when using @Persistent(converter=...)
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/14'>datanucleus-api-jpa-14</a>] -         JPA 2.1 has bug in EntityGraph method signatures for Attribute generic type
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/13'>datanucleus-api-jpa-13</a>] -         Handling of UniqueConstraint/Index &quot;name&quot; is incorrect
</li>
<li>[<a href='https://github.com/datanucleus/datanucleus-api-jpa/issues/16'>datanucleus-api-jpa-16</a>] -         JPA MetaModel doesn't cater correctly for List&lt;nonPC&gt;, and sets to CollectionAttributeImpl instead of ListAttributeImpl
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
<li>[<a href='https://github.com/datanucleus/datanucleus-hbase/issues/15'>datanucleus-hbase-15</a>] -         Cannot auto-create tables without deactivating sanity checks
</li>
</ul>

