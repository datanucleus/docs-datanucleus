<head><title>AccessPlatform 4.1.5</title></head>

# DataNucleus AccessPlatform 4.1.5

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.5 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_5.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__8th Octember 2015__ - DataNucleus AccessPlatform 4.1.5 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


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

