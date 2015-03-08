<head><title>AccessPlatform 4.1.0.M2</title></head>

# DataNucleus AccessPlatform 4.1.0.M2

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.0.M2 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_0_m2.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__9th March 2015__ - DataNucleus AccessPlatform 4.1.0.M2 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1275'>NUCCORE-1275</a>] -         Add method DataNucleusEnhancer.addPersistenceUnit(PersistenceUnitMetaData) for dynamically created persistence units
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-290'>NUCJPA-290</a>] -         Provide access to other value generators not in scope of JPA spec
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1278'>NUCCORE-1278</a>] -         Persistence property &quot;datanucleus.findObject.typeConversion&quot; should be overrideable on PM/EM basis
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1279'>NUCCORE-1279</a>] -         Support specification of &quot;comparator-name&quot; via extensions on the field rather than just on collection metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1280'>NUCCORE-1280</a>] -         Move all class/member level metadata extensions to &quot;public static final String&quot; fields in org.datanucleus.metadata.MetaData
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-84'>NUCAPIJDO-84</a>] -         Make use of ConcurrentHashMap for pm cache now that we support JDK1.7+ only
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-293'>NUCJPA-293</a>] -         Make use of ConcurrentHashMap for persistence unit metadata now that we support JDK1.7+ only
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-153'>NUCMONGODB-153</a>] -         Support query of 1-1/N-1 reference compared to relation object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-158'>NUCMONGODB-158</a>] -         Cater for query structure like &quot;field == param&quot; or &quot;field == literal&quot; and the field uses a TypeConverter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-160'>NUCMONGODB-160</a>] -         java.sql.Time, java.sql.Date are being stored as String when could use &quot;date&quot; Mongo type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-161'>NUCMONGODB-161</a>] -         Support retrieval of interface fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-852'>NUCRDBMS-852</a>] -         Support query fetch of Collection/Map/Array fields when serialised (i,e stored in single column of owner table).
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-858'>NUCRDBMS-858</a>] -         Support NUCCORE-1280
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-14'>NUCJODATIME-14</a>] -         Extend Joda time support for LocalDateTime
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1271'>NUCCORE-1271</a>] -         Drop targetClass from org.datanucleus.identity.SingleFieldId since duplicates targetClassName
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1272'>NUCCORE-1272</a>] -         Rename options for &quot;datanucleus.valuegeneration.transactionAttribute&quot; to be NEW and EXISTING
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1274'>NUCCORE-1274</a>] -         Support CASE / IF/ELSE &quot;when&quot; conditions that are not completely defined (i.e depend on previous when conditions)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1276'>NUCCORE-1276</a>] -         Remove refs to javax.jdo properties/methods
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1281'>NUCCORE-1281</a>] -         Provide handling for Enum &quot;value getter method&quot; so it can be used by all store plugins (currently in RDBMS only)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-82'>NUCAPIJDO-82</a>] -         Implement JDK1.7 JDOConnectionJDBCImpl methods since using JDK1.7+ now
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-83'>NUCAPIJDO-83</a>] -         Support NUCCORE-1271
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-291'>NUCJPA-291</a>] -         Allow direct access to java.sql.Connection via EM.unwrap when using RDBMS
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-292'>NUCJPA-292</a>] -         Remove use of javax.jdo.option.transactiontype : only need internal DataNucleus property with JPA
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-294'>NUCJPA-294</a>] -         Implement Criteria FetchImpl.fetch methods so we can chain fetches
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-850'>NUCRDBMS-850</a>] -         Change &quot;datanucleus.multivaluedFetch&quot; to be RDBMS specific and specifiable globally
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-851'>NUCRDBMS-851</a>] -         Add check on CASE &quot;action&quot; expression types for consistency
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-853'>NUCRDBMS-853</a>] -         HikariCP : Make leakThreshold, maxLifetime configurable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-854'>NUCRDBMS-854</a>] -         Support NUCCORE-1274
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-855'>NUCRDBMS-855</a>] -         Drop support for &quot;adapter-column-name&quot; for overriding join table order column name. Just use &lt;order&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-860'>NUCRDBMS-860</a>] -         Push Enum &quot;value getter method&quot; handling down into datanucleus-core so we can make it available for other store plugins
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1277'>NUCCORE-1277</a>] -         DeleteFieldManager &quot;nullBidirIfNotDependent&quot; handling incomplete when dealing with N-1 relationships
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-80'>NUCEXCEL-80</a>] -         Make sure StoreData is populated before using fetchObject(...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-81'>NUCEXCEL-81</a>] -         Numeric object wrapper fields can fail on retrieval due to falling back to TypeConverter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-82'>NUCEXCEL-82</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-84'>NUCEXCEL-84</a>] -         Persist of object with composite PK results in blank row in worksheet before the next inserted object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-85'>NUCEXCEL-85</a>] -         Classes without table (abstract) can cause NPE if you try to do query over them
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-86'>NUCEXCEL-86</a>] -         Fetch of relation fields doesn't cater for the related object being deleted elsewhere. Copy Cassandra plugin handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-60'>NUCODF-60</a>] -         Make sure StoreData is populated before using fetchObject(...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-61'>NUCODF-61</a>] -         StoreEmbeddedFieldManager has incorrect logic in detection of embedded sub field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-62'>NUCODF-62</a>] -         Classes without table (abstract) can cause NPE if you try to do query over them
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-63'>NUCODF-63</a>] -         Fetch of relation fields doesn't cater for the related object being deleted elsewhere. Copy Cassandra plugin handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-154'>NUCMONGODB-154</a>] -         MongoUtils.getClassNameForIdentity should use StoreManager to get subclasses so they get registered
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-156'>NUCMONGODB-156</a>] -         Persisting array of char, byte etc can fail on retrieval since stored as List&lt;String&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-157'>NUCMONGODB-157</a>] -         Query of class with field using multiple-column TypeConverter only selects the first column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-163'>NUCMONGODB-163</a>] -         Creattion of index/unique is incorrect. Should set name if not set, and should use class name in generated name
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-54'>NUCJSON-54</a>] -         Classes without table (abstract) can cause NPE if you try to do query over them
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-55'>NUCJSON-55</a>] -         Fetch of relation fields doesn't cater for the related object being deleted elsewhere. Copy Cassandra plugin handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-848'>NUCRDBMS-848</a>] -         &quot;max&quot; value generator provides wrong id if 2 objects are persisted in one transaction  
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-856'>NUCRDBMS-856</a>] -         ViewImpl seems to have regression in validate() method
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-857'>NUCRDBMS-857</a>] -         Typo from NUCRDBMS-838
</li>
</ul>

