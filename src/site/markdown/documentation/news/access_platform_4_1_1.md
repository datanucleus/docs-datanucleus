<head><title>AccessPlatform 4.1.1</title></head>

# DataNucleus AccessPlatform 4.1.1

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.1 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_1.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__13th June 2015__ - DataNucleus AccessPlatform 4.1.1 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release



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

