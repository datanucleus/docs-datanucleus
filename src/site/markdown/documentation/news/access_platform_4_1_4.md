<head><title>AccessPlatform 4.1.4</title></head>

# DataNucleus AccessPlatform 4.1.4

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.4 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_4.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__15th September 2015__ - DataNucleus AccessPlatform 4.1.4 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


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

