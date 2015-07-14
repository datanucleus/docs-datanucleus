<head><title>AccessPlatform 4.2.0.M1</title></head>

# DataNucleus AccessPlatform 4.2.0.M1

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.2.0.M1 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_2_0_m1.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__14th July 2015__ - DataNucleus AccessPlatform 4.1.0.M2 ("Planck") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1325'>NUCCORE-1325</a>] -         Support Java generic TypeVariable where declared by class generic type bounds
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-93'>NUCAPIJDO-93</a>] -         Support specification of &quot;default&quot; TypeConverter via PMF properties
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-95'>NUCAPIJDO-95</a>] -         Support JDO 3.2 AttributeConverter specification via annotations/XML/API
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-314'>NUCJPA-314</a>] -         Support specification of datastore identity using XML metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-316'>NUCJPA-316</a>] -         Support specification of surrogate version using XML metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-317'>NUCJPA-317</a>] -         Provide access to &quot;datastore-id&quot; and &quot;surrogate-version&quot; via helper methods
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-901'>NUCRDBMS-901</a>] -         MariaDB support storing millisecs in time columns, needs recognising in adapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-911'>NUCRDBMS-911</a>] -         When RDBMS supports &quot;FOR UPDATE NOWAIT&quot; provide extension for specifying &quot;NOWAIT&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-912'>NUCRDBMS-912</a>] -         Ability to register an SQLMethod at runtime when not registered via the plugin mechanism
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-913'>NUCRDBMS-913</a>] -         Add COUNTSTAR function to equate to SQL &quot;COUNT(*)&quot; since not present in JDOQL/JPQL directly
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-99'>NUCAPIJDO-99</a>] -         JDOQLTypedQuery : change toString to include any subquery in the string
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1323'>NUCCORE-1323</a>] -         Add generics for element, key, value to all wrappers and backing stores
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1324'>NUCCORE-1324</a>] -         Bump repackaged ASM to v5.0.4 from 5.0.3
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-33'>NUCAPIJDO-33</a>] -         JDO3.2 : use javax.jdo.query interfaces when typesafe adopted by JDO
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-94'>NUCAPIJDO-94</a>] -         Build against groupId=org.datanucleus artifactId=javax.jdo version=3.2.0-m1-SNAPSHOT
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-97'>NUCAPIJDO-97</a>] -         PMF.addFetchGroups, PMF.removeFetchGroups, PMF.registerMetadata, Query.saveAsNamedQuery should check for permission &quot;getMetadata&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-98'>NUCAPIJDO-98</a>] -         Support XML XSD/DTD specifications of xmlns.jcp.org and use local copy for those
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-315'>NUCJPA-315</a>] -         Rename @DatastoreIdentity to be @DatastoreId for consistency
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-899'>NUCRDBMS-899</a>] -         Add generics for element, key, value to backing stores (see NUCCORE-1323)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-904'>NUCRDBMS-904</a>] -         PostgreSQL doesn't support &quot;read uncommitted&quot; so disable in adapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-905'>NUCRDBMS-905</a>] -         PostgreSQL doesn't support stored procedures so disable in adapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-11'>NUCGUAVA-11</a>] -         Support NUCCORE-1323
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-313'>NUCJPA-313</a>] -         JPQL generated for Criteria can have too many blanks in FROM clause when no alias
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-318'>NUCJPA-318</a>] -         Metamodel Type getJavaType returns wrong classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-900'>NUCRDBMS-900</a>] -         Schema generation fails if using a FK Map, and a separate unique constraint on a class, and not specifying constraint name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-902'>NUCRDBMS-902</a>] -         PostgreSQL function &quot;SUBSTRING&quot; needs explicit CAST of FROM/FOR args to INTEGER otherwise fails
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-903'>NUCRDBMS-903</a>] -         StringExpression.add creates CONCAT (||) of two expressions but should always be in parentheses, and in one case isn't
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-906'>NUCRDBMS-906</a>] -         Change entity after persist causes insert to fail
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-908'>NUCRDBMS-908</a>] -         DN4 does not seem to automatically create the DB schema (as in @PersistenceCapable(schema=...) for any entities annotated as such
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-909'>NUCRDBMS-909</a>] -         User specified catalog/schema should be translated into adapter case as required
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-910'>NUCRDBMS-910</a>] -         H2 adapter CREATE SCHEMA should use schema rather than catalog
</li>
</ul>

