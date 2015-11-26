<head><title>AccessPlatform 4.1.7</title></head>

# DataNucleus AccessPlatform 4.1.7

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.7 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_7.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__27th November 2015__ - DataNucleus AccessPlatform 4.1.7 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 

This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1358'>NUCCORE-1358</a>] -         Allow JPQL to exclude subclasses of the candidate
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-983'>NUCRDBMS-983</a>] -         Support SAP &quot;SQLAnywhere&quot;
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
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1360'>NUCCORE-1360</a>] -         Support PK field conversions for types Currency, TimeZone, UUID
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-20'>NUCJAVAEIGHT-20</a>] -         InstantTimestampConverter : use convenience methods to do the conversion
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-165'>NUCMONGODB-165</a>] -         Make sure &quot;ownerMmd&quot; is set for FetchFieldManager when embedded, add TODO to resolve
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJDOQUERY-22'>NUCJDOQUERY-22</a>] -         Add support for TypeVariables
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1362'>NUCCORE-1362</a>] -         Persistable elements contained in Collection/Map that is serialised (whole field) are not detached/attached correctly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-981'>NUCRDBMS-981</a>] -         Support NUCCORE-1362
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-985'>NUCRDBMS-985</a>] -         SELECT statement generation handling of ordering when multiple cols per order expression should apply quoting as final step but doesnt
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-986'>NUCRDBMS-986</a>] -         Creation of mapping in some cases misses the MultiColumnConverter case and doesnt use TypeConverterMultiMapping
</li>
</ul>

