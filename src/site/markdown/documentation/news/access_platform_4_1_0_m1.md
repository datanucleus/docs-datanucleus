<head><title>AccessPlatform 4.1.0.M1</title></head>

# DataNucleus AccessPlatform 4.1.0.M1

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.1.0.M1 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_1_0_m1.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__19th January 2015__ - DataNucleus AccessPlatform 4.1.0.M1 ("Chadwick") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-253'>NUCRDBMS-253</a>] -         DB2 : SerializeRead/useUpdateLock &quot;for update&quot; shouldn't have been appended to all selects
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1269'>NUCCORE-1269</a>] -         Map wrapper SCOs have inefficient initialise method when updating (setXXXField). Create efficient logic for working out changed elements
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1270'>NUCCORE-1270</a>] -         Add ExecutionContext.getLevel1Cache for symmetry with NucleusContext and Level2Cache
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-81'>NUCAPIJDO-81</a>] -         JDO class load listener : catch any exceptions loading the class and log rather than rethrowing
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-845'>NUCRDBMS-845</a>] -         Handling of case expression should check for non-Boolean conditional expression, and convert to CaseNumericExpression if possible
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1229'>NUCCORE-1229</a>] -         Add ExecutionContextReference interface, and use it in bytecode enhancement contract
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1238'>NUCCORE-1238</a>] -         Set of container field of a persistable doesn't make use of the old value when updating the field; should use the old value to decide what to do
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1260'>NUCCORE-1260</a>] -         Standard collection/map wrappers remove() does cascade delete direct, yet should check if queued operations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1263'>NUCCORE-1263</a>] -         Add OperationQueue operations for persists, removes and updates
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1265'>NUCCORE-1265</a>] -         Move StateManagerImpl.getEmbeddedOwners to ExecutionContext
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1266'>NUCCORE-1266</a>] -         Separate embedded owner field setting code from StateManagerImpl.wrapSCOField
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1267'>NUCCORE-1267</a>] -         SCOCollection/SCOMap updateEmbeddedXXX should take in makeDirty flag
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-844'>NUCRDBMS-844</a>] -         JDOQL/JPQL : Allow &quot;expr = {param}&quot; to have flexibility when the param is null so that can map to &quot;IS NULL&quot; or &quot;= null&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-846'>NUCRDBMS-846</a>] -         Support boolean Case expressions (just like we do numeric Case expressions)
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1264'>NUCCORE-1264</a>] -         Loss of all collection elements on add+remove when playing around with SCO wrapper of an object that was subsequently made HOLLOW
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-843'>NUCRDBMS-843</a>] -         MapMapping.postUpdate when setting to null doesn't clear the backing store but should
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-847'>NUCRDBMS-847</a>] -         JDOQL statement with multi-tenant PersistenceManager
</li>
</ul>

