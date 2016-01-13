<head><title>AccessPlatform 4.2.3</title></head>

# DataNucleus AccessPlatform 4.2.3

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.2.3 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_2_3.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__13th January 2016__ - DataNucleus AccessPlatform 4.2.3 ("Planck") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-991'>NUCRDBMS-991</a>] -         Support for fetch of ReferenceMapping field when there is a single implementation and using FK
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1366'>NUCCORE-1366</a>] -         AbstractMemberMetaData.getClassName(false) can return fully qualified name in some situations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-329'>NUCJPA-329</a>] -         JPA MetaModel doesn't cater correctly for List&lt;nonPC&gt;, and sets to CollectionAttributeImpl instead of ListAttributeImpl
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-990'>NUCRDBMS-990</a>] -         Loading of interface field with single implementation with version field is not loading the version
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-992'>NUCRDBMS-992</a>] -         Name of candidate key (unique) on join table is not respected
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-995'>NUCRDBMS-995</a>] -         TypeConverterMapping.getJavaType is incorrect when roleForMember is set
</li>
</ul>

