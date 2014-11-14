<head><title>AccessPlatform 4.0.4</title></head>

# DataNucleus AccessPlatform 4.0.4

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.4 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_4.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__15th November 2014__ - DataNucleus AccessPlatform 4.0.4 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


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

