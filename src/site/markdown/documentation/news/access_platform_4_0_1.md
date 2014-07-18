<head><title>AccessPlatform 4.0.1</title></head>

# DataNucleus AccessPlatform 4.0.1

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.1 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_1.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__19th July 2014__ - DataNucleus AccessPlatform 4.0.1 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1233'>NUCCORE-1233</a>] -         Support JDOQL compilation of &quot;IF (expr) expr ELSE IF (expr) expr ELSE expr&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-56'>NUCCASSANDRA-56</a>] -         Adding support for uuid datastoreType of Cassandra
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-96'>NUCHBASE-96</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-78'>NUCEXCEL-78</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-59'>NUCODF-59</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-53'>NUCJSON-53</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-148'>NUCMONGODB-148</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-807'>NUCRDBMS-807</a>] -         Support mapping java.util.UUID to PostgreSQL native &quot;uuid&quot; column type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-810'>NUCRDBMS-810</a>] -         Support for TIME and DATE JDBC data types for MS SQL Server 2008 and newer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-51'>NUCNEOFORJ-51</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-59'>NUCODF-59</a>] -         Support cascade-persist/cascade-update on 1-1/1-N fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-14'>NUCJAVAEIGHT-14</a>] -         Provide Java8 variants of Collection/Map wrappers so that any new methods can be supported.
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1237'>NUCCORE-1237</a>] -         CompleteClassTable should check for columns with same name in the table and throw an exception
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1230'>NUCCORE-1230</a>] -         Upgrade ASM to 5.0.3
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1231'>NUCCORE-1231</a>] -         Add basic support for temporal literals as Strings
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1236'>NUCCORE-1236</a>] -         Support update of L2 cache when refresh() is called
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-805'>NUCRDBMS-805</a>] -         Add simple handling of temporal literal as String
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-806'>NUCRDBMS-806</a>] -         Mappings for Oracle should be merged into org.datanucleus.store.rdbms.mapping.[java|datastore]
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1235'>NUCCORE-1235</a>] -         RDBMSStoreManager.addSchemaCallback does not populate the schemaCallbacks correctly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1239'>NUCCORE-1239</a>] -         1-1 Birdirecional relation management fails when using optimistic tx
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-78'>NUCAPIJDO-78</a>] -         Creation of implementation of persistent abstract class / interface creates metadata with full name (including package)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-274'>NUCJPA-274</a>] -         NamedStoredProcedureQueries doesn't set procedure name on processed stored procs metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-55'>NUCCASSANDRA-55</a>] -         Could not serialize byte[] @Serialized member on Cassandra store
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-79'>NUCEXCEL-79</a>] -         SchemaTool doesn't make full use of generalised Table; should create CompleteClassTable when not present
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-149'>NUCMONGODB-149</a>] -         SchemaTool doesn't make full use of generalised Table; should create CompleteClassTable when not present
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-808'>NUCRDBMS-808</a>] -         Datanucleus can't find sequence in PostrgreSQL when persistence property 'datanucleus.identifier.case' is set
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-809'>NUCRDBMS-809</a>] -         Inconsistent behavior in enum value conversion to/from numeric value in RDBMS using 'enum-value-getter' extension
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-811'>NUCRDBMS-811</a>] -         Enum extension &quot;enum-check-constraint&quot; is incorrectly handled if also using extension &quot;enum-value-getter&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-812'>NUCRDBMS-812</a>] -         When executing StoredProcedure with multiple result sets, the close of the first results will close the statement!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-813'>NUCRDBMS-813</a>] -         1-N FK bidir relationship management failing when using optimistic tx
</li>
</ul>

