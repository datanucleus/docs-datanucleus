<head><title>AccessPlatform 4.0.6</title></head>

# DataNucleus AccessPlatform 4.0.6

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.6 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_6.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__1st March 2015__ - DataNucleus AccessPlatform 4.0.6 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release



## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1273'>NUCCORE-1273</a>] -         Support for NUCRDBMS-848 for DN 4.0
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1274'>NUCCORE-1274</a>] -         Support CASE / IF/ELSE &quot;when&quot; conditions that are not completely defined (i.e depend on previous when conditions)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-854'>NUCRDBMS-854</a>] -         Support NUCCORE-1274
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-848'>NUCRDBMS-848</a>] -         &quot;max&quot; value generator provides wrong id if 2 objects are persisted in one transaction  
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-856'>NUCRDBMS-856</a>] -         ViewImpl seems to have regression in validate() method
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-81'>NUCEXCEL-81</a>] -         Numeric object wrapper fields can fail on retrieval due to falling back to TypeConverter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-82'>NUCEXCEL-82</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-84'>NUCEXCEL-84</a>] -         Persist of object with composite PK results in blank row in worksheet before the next inserted object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-61'>NUCODF-61</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
</ul>

