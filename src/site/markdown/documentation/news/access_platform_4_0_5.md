<head><title>AccessPlatform 4.0.5</title></head>

# DataNucleus AccessPlatform 4.0.5

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.5 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_5.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__2nd February 2015__ - DataNucleus AccessPlatform 4.0.5 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-845'>NUCRDBMS-845</a>] -         Handling of case expression should check for non-Boolean conditional expression, and convert to CaseNumericExpression if possible
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-852'>NUCRDBMS-852</a>] -         Support query fetch of Collection/Map/Array fields when serialised (i,e stored in single column of owner table).
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-851'>NUCRDBMS-851</a>] -         Add check on CASE &quot;action&quot; expression types for consistency
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-847'>NUCRDBMS-847</a>] -         JDOQL statement with multi-tenant PersistenceManager
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-151'>NUCMONGODB-151</a>] -         JDOQL COUNT query fails for unknown classes
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCLDAP-66'>NUCLDAP-66</a>] -         AttributeStrategy : When reassigning N-1 owner, allow for new owner not yet being persistent
</li>
</ul>

