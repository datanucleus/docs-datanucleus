<head><title>AccessPlatform 4.0.2</title></head>

# DataNucleus AccessPlatform 4.0.2

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.2 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_2.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__29th August 2014__ - DataNucleus AccessPlatform 4.0.2 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


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

