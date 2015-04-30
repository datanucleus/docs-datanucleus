<head><title>AccessPlatform 4.1.0.M4</title></head>

# DataNucleus AccessPlatform 4.1.0.M4

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.0.M3 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_0_m3.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__1st May 2015__ - DataNucleus AccessPlatform 4.1.0.M4 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1292'>NUCCORE-1292</a>] -         Allow subquery in SELECT clause (JDOQL/JPQL)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-304'>NUCJPA-304</a>] -         Support @Convert with attributeName of &quot;key&quot; or &quot;value&quot; to apply to the key or value of a Map field
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-305'>NUCJPA-305</a>] -         Support @Convert when specified on Collection to convert the element
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-17'>NUCRDBMS-17</a>] -         Classes with collection/map fields should be allowed to have &quot;subclass-table&quot; inheritance strategy, and the elements/keys/values should be allowed to have &quot;subclass-table&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-18'>NUCRDBMS-18</a>] -         1-1 undirectional relation needs the flexibility of allowing &quot;subclass-table&quot; at the other end
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-19'>NUCRDBMS-19</a>] -         Support for 1-N bidir relation between impl of interface with collection of elements
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-719'>NUCRDBMS-719</a>] -         Provide the ability to override a builtin method mapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-882'>NUCRDBMS-882</a>] -         Support for DEGREES/RADIANS functions and JDOQL Math.toDegrees/Math.toRadians
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1300'>NUCCORE-1300</a>] -         Call to PM.refreshObject/retrieveObject/evictObject gives unclear exception message when transient object passed 
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1306'>NUCCORE-1306</a>] -         TypeManager should use ConcurrentHashMap since multithreaded
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-89'>NUCAPIJDO-89</a>] -         Allow PM.getFetchGroup/PMF.getFetchGroup to include members of existing named/static query when available
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-878'>NUCRDBMS-878</a>] -         Query attempting to select a 1-1/N-1 field which uses subclass-table (hence no FK) throws exception on form of statement but should just select FK only
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-884'>NUCRDBMS-884</a>] -         When a JDBC driver provides multiple sql-type for a jdbc-type should be possible to have default matching plugin.xml
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-54'>NUCSPATIAL-54</a>] -         Support NUCRDBMS-884
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1293'>NUCCORE-1293</a>] -         Prevent SCOOperation's being added to OperationQueue when owner object is not yet flushed to datastore
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1294'>NUCCORE-1294</a>] -         ManagedRelations : backed Set wrappers initialise(Collection, Collection) register changes twice
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1296'>NUCCORE-1296</a>] -         In-memory evaluation of assorted Math.xxx functions
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1298'>NUCCORE-1298</a>] -         Move &quot;implementation-classes&quot; handling to be with CollectionMetaData, MapMetaData etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1301'>NUCCORE-1301</a>] -         Metadata load often resulted in attempt to find metadata for single-field identity classes when obviously not persistent
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1302'>NUCCORE-1302</a>] -         Clean up ExecutionContext.close to merge methods only used once, so we improve logging
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-90'>NUCAPIJDO-90</a>] -         Change JDOAdapter.isXXX to use Persistable direct rather than routing through JDOHelper.isXXX and then through JDOImplHelper.nonBinaryCompatibleIs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-302'>NUCJPA-302</a>] -         Support query hints on @NamedQuery, @NamedNativeQuery etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-877'>NUCRDBMS-877</a>] -         1-N FK Set of interface object doesn't allow update of FK reliably
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-883'>NUCRDBMS-883</a>] -         JPQL should allow ORDER BY using result alias
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1295'>NUCCORE-1295</a>] -         Generic compiler can fail to correctly detect class names in PrimaryExpression and result in invalid compilation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1299'>NUCCORE-1299</a>] -         Make sure that close of ExecutionContext completes, checking for null objects
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1303'>NUCCORE-1303</a>] -         Joining over map value not working when wanting to chain the join to sub-objects of the value
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1304'>NUCCORE-1304</a>] -         Generic compile of filter &quot;field NOT IN (:param)&quot; doesn't include the NOT in the resultant compile
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1305'>NUCCORE-1305</a>] -         Generic compile of filter something like &quot;field.method().field.method()&quot; is not compiled correctly
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1307'>NUCCORE-1307</a>] -         List wrapper SCOs have error in initialise method when updating (setXXXField); should log with operation queue in more situations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-303'>NUCJPA-303</a>] -         Metamodel returns ONE_TO_ONE instead of MANY_TO_ONE
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-876'>NUCRDBMS-876</a>] -         When we try to fetch a N-1 &quot;owner&quot; field (with join table) where the owner has an interface, it doesn't get the implementation and fails
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-879'>NUCRDBMS-879</a>] -         Backing store of Collection with multiple root elements doesn't give correct info for size()
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-880'>NUCRDBMS-880</a>] -         When storing java.sql.Timestamp as String it calls ps.setObject(Timestamp) and relies on JDBC driver
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-881'>NUCRDBMS-881</a>] -         RuntimeException caused by readl lock during preDelete is ignored
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-885'>NUCRDBMS-885</a>] -         Selecting a map value not working when the value has a Map field in it
</li>
</ul>

