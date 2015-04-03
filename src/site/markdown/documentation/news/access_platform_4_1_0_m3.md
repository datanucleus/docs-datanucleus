<head><title>AccessPlatform 4.1.0.M3</title></head>

# DataNucleus AccessPlatform 4.1.0.M3

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.0.M3 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_0_m3.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__3rd April 2015__ - DataNucleus AccessPlatform 4.1.0.M3 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


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

