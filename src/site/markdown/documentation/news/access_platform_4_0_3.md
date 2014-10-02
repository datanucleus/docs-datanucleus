<head><title>AccessPlatform 4.0.3</title></head>

# DataNucleus AccessPlatform 4.0.3

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.3 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_3.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__2nd October 2014__ - DataNucleus AccessPlatform 4.0.3 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-283'>NUCJPA-283</a>] -         Expose access to the underlying connection, so people can perform native operations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-285'>NUCJPA-285</a>] -         Allow EntityManager.createNativeQuery to create a query using a non-SQL query language
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-21'>NUCCASSANDRA-21</a>] -         Support native Cassandra CQL queries
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1256'>NUCCORE-1256</a>] -         Extend NUCCORE-1233 support for JDOQL &quot;IF ... ELSE IF ... ELSE ...&quot; to require final ELSE or throw exception
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-730'>NUCRDBMS-730</a>] -         Persist of M-N relation can be inefficient; currently always does SELECT to see if present then INSERT.
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1248'>NUCCORE-1248</a>] -         NamingFactory.getConstraintName for member should also pass in the class name so we can name indexes when part of table for subclasses
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1249'>NUCCORE-1249</a>] -         Drop SCOMtoN since we can just check if it is M-N relation or if collection
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1250'>NUCCORE-1250</a>] -         Add method to MetaDataManager that returns the enhanced method name prefix (i.e &quot;dn&quot;)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1253'>NUCCORE-1253</a>] -         Move identity conversion handling into core from api.jdo/api.jpa
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1255'>NUCCORE-1255</a>] -         Add method for what query language is considered &quot;native&quot; for a store
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-79'>NUCAPIJDO-79</a>] -         Add Transaction set/getNontransactionalWriteAutoCommit
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-282'>NUCJPA-282</a>] -         Support @ConstructorResult
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-58'>NUCCASSANDRA-58</a>] -         Support NUCCORE-1248
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-59'>NUCCASSANDRA-59</a>] -         Support NUCCORE-1255
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-150'>NUCMONGODB-150</a>] -         Support NUCCORE-1248
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-827'>NUCRDBMS-827</a>] -         Support constructor mappings in SQL query results
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-833'>NUCRDBMS-833</a>] -         Support NUCCORE-1255
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1252'>NUCCORE-1252</a>] -         ByteArrayByteBufferConverter toMemberType ByteBuffer to byte[] conversion fails
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1254'>NUCCORE-1254</a>] -         Backed SCO wrappers should not add operations to queue when the owner object is not yet inserted
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-281'>NUCJPA-281</a>] -         CriteriaQuery needs to respect any distinct specified on &quot;select&quot; but currently ignores it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-57'>NUCCASSANDRA-57</a>] -         JPQLQuery should have latest candidate class code (copy from HBase for example)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-829'>NUCRDBMS-829</a>] -         Embedded object causes: IllegalArgumentException: out of field index
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-830'>NUCRDBMS-830</a>] -         ResultClassROF can throw exception if it finds an enhancement method in the result class of a query
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-831'>NUCRDBMS-831</a>] -         RDBMSStoreManager generates comments which are bad syntax in Mysql
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-832'>NUCRDBMS-832</a>] -         Persist of object with Collection (via join table) containing some new and some detached elements doesn't create the join table entries
</li>
</ul>

