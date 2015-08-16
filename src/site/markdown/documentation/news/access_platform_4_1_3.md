<head><title>AccessPlatform 4.1.3</title></head>

# DataNucleus AccessPlatform 4.1.3

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.3 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_3.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__16th August 2015__ - DataNucleus AccessPlatform 4.1.3 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1335'>NUCCORE-1335</a>] -         Add ability to set JDOQL/JPQL strictness on query compilation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1336'>NUCCORE-1336</a>] -         JPQL : support CURRENT_TIMESTAMP(), CURRENT_DATE(), CURRENT_TIME()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1337'>NUCCORE-1337</a>] -         JPQL : support COUNT(*)
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

