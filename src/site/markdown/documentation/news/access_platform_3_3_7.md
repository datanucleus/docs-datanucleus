<head><title>AccessPlatform 3.3.7</title></head>

# DataNucleus AccessPlatform 3.3.7

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 3.3.6 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/news/access_platform_3_3_6.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__28th January 2014__ - DataNucleus AccessPlatform 3.3.7 ("Galileo") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1104'>NUCCORE-1104</a>] -         Provide API to allow a class' ClassMetaData to be removed from the MetaDataManager.</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-66'>NUCAPIJDO-66</a>] -         Allow type conversion on key input to pm.getObjectById(Class cls, Object key)</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-262'>NUCJPA-262</a>] -         Add extension annotation @Index to allow index specification on fields/methods</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCREST-13'>NUCREST-13</a>] -         Provide way of specifying the FetchPlan for a query, such as pass in a fetch group name</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-710'>NUCRDBMS-710</a>] -         Support NuoDB</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-741'>NUCRDBMS-741</a>] -         NuoDB : support SEQUENCE, and FETCH/OFFSET</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-742'>NUCRDBMS-742</a>] -         NuoDB : support IDENTITY columns</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-743'>NUCRDBMS-743</a>] -         NuoDB : generate PK in CREATE TABLE statement</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-744'>NUCRDBMS-744</a>] -         NuoDB : support SELECT ... FOR UPDATE</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1106'>NUCCORE-1106</a>] -         NamingFactory : support naming of indexes</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-740'>NUCRDBMS-740</a>] -         SQL : cater for CREATE, DROP, etc statements and provide for correct execution of them</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1077'>NUCCORE-1077</a>] -         L2 Cache : cater for caching of TreeSet/TreeMap when using composite id - need CachedId to be Comparable, or store in HashMap</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1101'>NUCCORE-1101</a>] -         Provide findObject type conversion persistence property to be used by JDO/JPA APIs</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-67'>NUCAPIJDO-67</a>] -         Support presence of extensions on @Index, @ForeignKey, @Unique, @PrimaryKey</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-261'>NUCJPA-261</a>] -         Drop datanucleus.jpa.findTypeConversion and use datanucleus.findObject.typeConversion</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-737'>NUCRDBMS-737</a>] -         Firebird : support NULLS specification in order by clause</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-739'>NUCRDBMS-739</a>] -         Firebird : change CREATE TABLE to define PRIMARY KEY also</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-745'>NUCRDBMS-745</a>] -         NuoDB : set transaction isolation levels that are supported to match NuoDB docs</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-746'>NUCRDBMS-746</a>] -         Allow a DatastoreAdapter to only support some types of ResultSet</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-752'>NUCRDBMS-752</a>] -         Move JDBC types lookup into DatastoreAdapter since different for each JDBC driver / adapter</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1100'>NUCCORE-1100</a>] -         Backing store Map.values returns Set when not caching values meaning it doesn't (currently) support duplicated values. Should support it</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1102'>NUCCORE-1102</a>] -         Query processing of &quot;NULLS LAST&quot; is being compiled to &quot;NULLS FIRST&quot;, cut and paste error</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1103'>NUCCORE-1103</a>] -         Eager loading of multi-valued fields fails for collections of type java.util.SortedSet.  This would seem to be due to a bug in SCOUtils.</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1107'>NUCCORE-1107</a>] -         SchemaTool : should call StoreManager.close to give any datastore connections the opportunity to be closed cleanly</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-735'>NUCRDBMS-735</a>] -         Map.values should return CollectionStore as per NUCCORE-1100 update to MapStore API</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-736'>NUCRDBMS-736</a>] -         DN generated Invalid query syntax is generated for DB2 LUW in Hive 12</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-738'>NUCRDBMS-738</a>] -         Firebird : query range from of 0 is incorrectly handled</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-747'>NUCRDBMS-747</a>] -         Null Pointer exception when running executeWithArray together with addGroup</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-749'>NUCRDBMS-749</a>] -         Select of identity field(s) on candidate with new-table inheritance and PK in superclass/table can cause error in SQL generation</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-751'>NUCRDBMS-751</a>] -         Query UPDATE statement with object reference with multiple PK fields to NULL generates incorrect SQL</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-137'>NUCMONGODB-137</a>] -         Calling hasNext() on empty query result iterator returns true</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-86'>NUCHBASE-86</a>] -         Read of enum when stored as int (ordinal) causes ClassCastException</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-34'>NUCSPATIAL-34</a>] -         Use of postgis-jdbc 2.1.0 causes problems with MySQL</li>
</ul>

