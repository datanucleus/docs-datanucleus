<head><title>AccessPlatform 4.1.0.RELEASE</title></head>

# DataNucleus AccessPlatform 4.1.0.RELEASE

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.0.RELEASE Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_0_release.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__19th May 2015__ - DataNucleus AccessPlatform 4.1.0.RELEASE ("Chadwick") is released.
DataNucleus AccessPlatform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, Cassandra, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


DataNucleus AccessPlatform 4.1 includes the following features relative to version 4.0

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


This release includes the following changes over the previous release (4.1.0.M4)

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

