<head><title>AccessPlatform 3.3.8</title></head>

# DataNucleus AccessPlatform 3.3.8

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 3.3.8 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/news/access_platform_3_3_8.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__15th March 2014__ - DataNucleus AccessPlatform 3.3.8 ("Galileo") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-757'>NUCRDBMS-757</a>] -         getClassNameForObjectID should check on number of concrete candidates, and return if just 1
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1111'>NUCCORE-1111</a>] -         Mark any class using &quot;DatastoreUniqueOID&quot; as not being L2 cacheable to avoid problems
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1115'>NUCCORE-1115</a>] -         TypeManager extraction of datastore type for a TypeConverter can fail when we are using an interface as the member type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1138'>NUCCORE-1138</a>] -         L2 cache configuration not reset when getting ExecutionContext from pool
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-758'>NUCRDBMS-758</a>] -         Wrong SQL generated for bulk fetch for queries with order by
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCXML-55'>NUCXML-55</a>] -         Setting the 'indent-number' attribute is incompatible with some external XSLT libraries.
</li>
</ul>

