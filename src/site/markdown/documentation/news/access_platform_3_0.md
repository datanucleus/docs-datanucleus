<head><title>AccessPlatform 3.0</title></head>

#Release Notes for DataNucleus AccessPlatform v3.0

The 3.0 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 3.0_ includes the following over 2.2

<ul>
<li>JDO, JPA, REST APIs split out into separate plugins with JPA no longer piggybacking on JDO.</li>
<li>Major restructring to provide initial support for Data Federation</li>
<li>Ability to specify classes as "read-only"</li>
<li>Major changes with non-transactional operations, providing atomic persistence/delete</li>
<li>SchemaTool : added support for ODF, Excel, MongoDB, HBase</li>
<li>MongoDB : New plugin for MongoDB document store, providing quite complete feature set</li>
<li>HBase : Much enhanced support for HBase map store</li>
<li>RDBMS : Added support for SQLite</li>
<li>ODF : support added for embedded fields, maps, value generation, query of interfaces</li>
<li>Excel : support added for maps, value generation, query of interfaces</li>
<li>NeoDatis : support for unique constraints</li>
<li>Cache : added support for Xmemcached, and enhanced support for EHCache</li>
<li>JDO : Support for "complete-table"</li>
<li>JDO : Support for bulk update/delete via typesafe API</li>
<li>JPA : support for singleton EMF pattern</li>
<li>JPA : support for merge of transient object when it has identity fields mapping to persistent object</li>
<li>Now works with JBoss 6+</li>
<li>Many bug fixes, and minor feature additions.</li>
</ul>



# DataNucleus AccessPlatform 3.0.10

__Jun 15h 2012__ : _Version 3.0.10_ includes the following changes

<ul>
<li>JPA : Fix bug with EMF creation when overriding properties are null.</li>
<li>JPA : Fix bug in Criteria FromImpl causing NPE</li>
<li>Fix bug preventing objects created using "identity" strategy from being L2 cached</li>
<li>Fix bug in string conversion of JDOQL Typesafe into String when including equals clause</li>
<li>Add support for detachment of N-1 join table relations.</li>
<li>RDBMS : Fix bug in concurrent access with classes with date types persisted as String</li>
</ul>


# DataNucleus AccessPlatform 3.0.9

__Mar 28th 2012__ : _Version 3.0.9_ includes the following changes

<ul>
<li>Change Set proxy to not do clear+addAll on an update</li>
<li>Fix bug in removeAll() method of Set proxies</li>
<li>Add support for bulk loading of objects when calling pm.getObjectsById()</li>
<li>Fix to non-referential flush process to detect new objects correctly</li>
<li>Fix to persist of 1-N uni FK Lists to not to update the FK even though already set (less SQL calls)</li>
<li>Fix to delete of N side of a 1-N bidir catering for relation not loaded</li>
<li>Improved error reporting when detach fails</li>
<li>JPA : fix to javax.persistence.XXXDataSource persistence properties</li>
</ul>


# DataNucleus AccessPlatform 3.0.8

__Feb 28th 2012__ : _Version 3.0.8_ includes the following changes

<ul>
<li>Fix to cascade-attach of arrays of persistable types</li>
<li>Fix to classloader usage for "persistence.xml" to work with OSGi</li>
<li>Minor change to OSGi metadata load (Danny van Leiden)</li>
<li>JPA : Fix to "findTypeConversion" extension</li>
<li>RDBMS : Support for sequences with Derby 10.6+ (Michael Bouschen)</li>
<li>RDBMS : Fix to BLOB/CLOB with non-standard Oracle JDBC driver (Ludovic Galibert)</li>
</ul>


# DataNucleus AccessPlatform 3.0.7

__Feb 10th 2012__ : _Version 3.0.7_ includes the following changes

<ul>
<li>Fix to use of persistence property "datanucleus.storeManagerType"</li>
<li>JPA : Support for JPA2.1 Type Convertors</li>
<li>JPA : Fix to EM.find to also work for datastore-identity</li>
<li>JPA : Update to detection of 1-N UNI FK relations to avoid the need for JPA 'level' persistence property</li>
<li>JPA : Add numeric conversion capabilities to EM.find key argument.</li>
<li>JDO : Fix to duplicate close of query results when using Extent on non-RDBMS datastores</li>
<li>Fix to load of metadata for persistence unit when persistable inner classes present</li>
<li>Fix to instantiation of object from identity when root class is abstract and using single-field id</li>
<li>RDBMS : Fix to JPQL "INDEX" SQL generation for join table case</li>
<li>MongoDB : fix to query with no filter</li>
<li>JSON, HBase, MongoDB, Excel, ODF, RDBMS : fix to version of core usable to prohibit v3.1</li>
</ul>


# DataNucleus AccessPlatform 3.0.6

__Jan 29th 2012__ : _Version 3.0.6_ includes the following changes

<ul>
<li>Fix to clear/removeAll methods of backed SCOs for non-RDBMS datastores (e.g GAE)</li>
<li>Fix to embedded inheritance mapping treatment of members</li>
<li>Add code for generic type converter, compatible with JPA2.1 converters</li>
<li>Fix to JPA @EmbeddedId when used in a relation</li>
<li>Add validation of "jdbc-type" to only accept valid values</li>
<li>Allow for custom scanning for annotated classes (Ales Justin)</li>
<li>JDO3.1 : add check for invalid javax.jdo persistence properties</li>
<li>JDO3.1 : add security check on PMF.getManagedClasses calls</li>
<li>JPA extension : add annotation to support specification of column "position"</li>
<li>JPA2.1 : support stored procedure API</li>
<li>RDBMS : add support for serialisation of query results</li>
<li>RDBMS : fix use of JDOQL cast/instanceof for embedded inherited fields</li>
<li>MongoDB : support nondurable identity</li>
<li>Excel : support nondurable identity</li>
<li>Excel : support embedded PK fields</li>
<li>Excel : drop support for extension "sheet" and use standard only now</li>
<li>ODF : support embedded PK fields</li>
<li>ODF : drop support for extension "sheet" and use standard only now</li>
<li>HBase : fix reuse of HTable so we can use HBase 0.90.1+</li>
<li>HBase : dont allow table creation/validation if persistence properties not set</li>
</ul>


# DataNucleus AccessPlatform 3.0.5

__Jan 11th 2012__ : _Version 3.0.5_ includes the following changes

<ul>
<li>Make use of bulk load from L2 cache on use of PM.getObjectsById</li>
<li>Support for override of metadata for inherited fields/properties in embedded objects</li>
<li>Fix to in-memory query evaluation when an order clause is null</li>
<li>Some clean ups for logging</li>
<li>Fix to default value of "datanucleus.identifier.case" which was incorrect in 3.0.4</li>
<li>RDBMS : dont load all query results when running non-tx when we retain the connection</li>
<li>RDBMS : Support for use of sql-type when there are multiple possible for a jdbc-type</li>
<li>RDBMS : Support various MySQL sql types such as LONGTEXT, MEDIUMBLOB etc</li>
<li>RDBMS : Some improved error messages</li>
<li>JSON : Support for enum fields</li>
<li>JSON : Support datastore identity</li>
<li>JSON : Support 1-1/1-N/M-N relations</li>
<li>JSON : Support field types that have long/String converters</li>
<li>JSON : Support versioning of objects</li>
<li>DB4O : Remove invalid import from OSGi info</li>
</ul>


# DataNucleus AccessPlatform 3.0.4

__Dec 10th 2011__ : _Version 3.0.4_ includes the following changes

<ul>
<li>AccessPlatform : drop support for ZIP distributions for db4o and NeoDatis datastores</li>
<li>AccessPlatform : add Maven POM artifacts for main AccessPlatform combinations (JDO-RDBMS, JPA-RDBMS, etc)</li>
<li>Add ability to turn off Metadata support for XML or annotations, for performance</li>
<li>Parameterise all persistence property names for easy referencing</li>
<li>Split support for java.awt geometry types into a separate plugin, and complete support for persisting in String form</li>
<li>Improve startup process so that NucleusContext, PluginManager are more modular, and so that
    JPA doesn't create multiple working contexts</li>
<li>SchemaTool : improvement to class resolution process when not forking the JVM process</li>
<li>Support for Atomikos transaction manager (Matthew Adams)</li>
<li>Support batching of L2 cache updates</li>
<li>Support L2 cache "mode" to determine which classes are cacheable (JPA "sharedCache.Mode")</li>
<li>RDBMS : Improvement to handling of result classes when single column selected</li>
<li>RDBMS : Support for embedded inherited objects (likely part of JDO3.1/3.2)</li>
<li>MongoDB : fix to handling of bidirectional relations when using IDENTITY strategy</li>
<li>HBase : fix problem in table management</li>
<li>Cache : support for javax.cache v0.3+ (in datanucleus-cache v3.1.0, while support for the earlier
    version is in datanucleus-cache v3.0)</li>
<li>Eclipse : update to the plugin to move API to general preferences and drop the enhancer "type"
    since it was not being used</li>
</ul>


# DataNucleus AccessPlatform 3.0.3

__Nov 5th 2011__ : _Version 3.0.3_ includes the following changes

<ul>
<li>Rewrite of significant parts of the L2 cache to now store a map of field values rather than a
    detached persistable object. This means no locking is needed.</li>
<li>Fix to metadata identification of some Object and interface field relation types</li>
<li>Fix to query result cache evict-by-class process</li>
<li>Fix to generic compilation of implicit query parameters when repeated in the query</li>
<li>Change ObjectStringConverter/ObjectLongConverter to use generics for type safety</li>
<li>OSGi : Add export version to many MANIFEST entries</li>
<li>JDO : Add support for use of javax.validation</li>
<li>JDO : Respect persistence-unit "validation-mode" setting</li>
<li>JPA : Respect persistence-unit "validation-mode" setting</li>
<li>JPA : Add DataNucleus variant of orm.xsd so we can add on vendor specifics</li>
<li>Cache : Fix to use of Memcached caches so they can handle all "identity" types</li>
<li>Cache : Support Cacheonix as a query result cache</li>
<li>RDBMS : Fix to PostgreSQL ESCAPE syntax support</li>
<li>RDBMS : Fix to JDOQL "equalsIgnoreCase" handling</li>
<li>RDBMS : Fix to query serializeRead to only apply it when in a transaction</li>
<li>MongoDB : Support multitenancy via discriminator</li>
<li>MongoDB : Only evaluate query filter in-memory if not done completely in-datastore</li>
</ul>


# DataNucleus AccessPlatform 3.0.2

__Oct 1st 2011__ : _Version 3.0.2_ includes the following changes

<ul>
<li>Fix to L2 caching of fields of types Map&lt;PC, NonPC&gt;, Map&lt;NonPC, PC&gt;</li>
<li>Fix to allow plugin registry to load plugins from "https"</li>
<li>Fix to allow recursion in flushing</li>
<li>JDO : Fix to @Embedded processing</li>
<li>JPA : Allow specification of jdbc type for a field (extension)</li>
<li>RDBMS : Fixes to SQL generation for collections of interfaces where FK per implementation</li>
<li>RDBMS : Fix to clear/remove in maps where formed using foreign key</li>
<li>RDBMS : Support for in-datastore handling of query range for Oracle, DB2</li>
<li>RDBMS : Support for MultiTenancy using a discriminator</li>
<li>RDBMS : Support for specification of JDBC driver properties with connection pools</li>
<li>RDBMS : Fix to boolean usage in some queries</li>
<li>HBase : Fix to not serialise the PK by default</li>
<li>HBase : Support for "schema evolution : addition of new fields"</li>
<li>HBase : Fix to query handling of "!="</li>
<li>MongoDB : Support for multiple "AND" clauses on the same field when querying</li>
<li>MongoDB : Support for "schema evolution : addition of new fields"</li>
<li>Cache : Support for use of Cacheonix as an L2 cache</li>
</ul>


# DataNucleus AccessPlatform 3.0.1

__Aug 27th 2011__ : _Version 3.0.1_ includes the following changes

<ul>
<li>Improved support for DataNucleus in non-Eclipse OSGi environments (Alexey Sushko)</li>
<li>Separate synchronisation of PM/EM access into separate class so not used for majority of use-cases</li>
<li>Support for embedded "null-indicator" column/value for JPA (extension)</li>
<li>Fix bug in detach() of newly-persistent object that was causing NPE on commit (JPA)</li>
<li>Change access to StoreManager to better facilitate data federation</li>
<li>JSON : minor change to URL processing</li>
<li>RDBMS : Support for JDOQL "JDOHelper.getVersion()"</li>
<li>RDBMS : Support SQLServer with table names having spaces</li>
<li>RDBMS : Improve support for indexes under SQLServer</li>
<li>ODF : Support retrieval of interface field</li>
<li>Excel : Support retrieval of interface field</li>
<li>MongoDB : Support retrieval of interface field</li>
<li>JDO JCA : Better support for JBoss 7</li>
</ul>


# DataNucleus AccessPlatform 3.0.0.RELEASE

__Aug 1st 2011__ : _Version 3.0 RELEASE_ includes the following changes

<ul>
<li>JDO : Add ability to hook into transaction events via listener</li>
<li>JPA : Fix problem with DetachAllOnRollback not being set</li>
<li>JPA : Fix fetch flag observance when read from XML</li>
<li>JPA : Fix problem with singleton EMF pattern</li>
<li>Major changes to java type management to support specification of generics by configuration, and
    to give major speed up in type information access</li>
<li>Move SCO container backing store implementations into RDBMS plugin</li>
<li>Fix use of version metadata with respect to inheritance of classes, affecting various store plugins</li>
<li>Fix problems with non-transactional "commit" and pm/em close process to discard objects that
    don't need any processing</li>
<li>Fix all operations that involve schema updates to respect the "autoCreate" flags (so they now
    can correctly prevent any schema changes)</li>
<li>Fix to queries using result class, to prevent NPE when selecting candidate and defining result class
    as candidate</li>
<li>MongoDB : fix to use of IDENTITY for datastore id</li>
<li>MongoDB : fix to querying with inheritance</li>
<li>MongoDB : added extra handling of MongoDB numeric types</li>
<li>Maven : fix to setting of the CLASSPATH in some situations</li>
</ul>


# DataNucleus AccessPlatform 3.0.0.M6

__Jul 10th 2011__ : _Version 3.0 Milestone 6_ includes the following changes

<ul>
<li>Added the ability to persist transient objects as a way of updating existing persistent objects (application identity only).</li>
<li>Added persistence property for control over what is detached (for APIs without fetch groups)</li>
<li>Fix to delete of a detached object</li>
<li>Fix to SortedSet use of comparator in detaching</li>
<li>Evict entries from the query cache when objects of the candidate type are updated/deleted/persisted</li>
<li>Fix to use of Collection.add so that it checks on contains() before performing any action</li>
<li>Change to make non-transactional operations as not "queued"</li>
<li>Allow "detach-on-close" to be run non-transactional</li>
<li>Add support for object identity translators for the key value</li>
<li>Enhancer : add support for custom detach field access behaviour</li>
<li>JPA : Add support for JPA2.1 EMF.unwrap, Cache.unwrap</li>
<li>JPA : Set "RetainValues" to default to true for cleaner user feedback</li>
<li>JPA : Various fixes around metamodel methods, and exception handling</li>
<li>REST : Fix to respect "persistence-unit" definition like it did in v2</li>
<li>RDBMS : Initial support for SQLite</li>
<li>RDBMS : Fully implements JDOQL String.startsWith(str, int) for Derby, MSSQL</li>
<li>RDBMS : Fix Derby handling of composite indexes</li>
<li>RDBMS : Fix to make use of connection pool properties</li>
<li>MongoDB : Fix to use of IDENTITY fields</li>
<li>MongoDB : Fix to authentication handling</li>
<li>Many other bug fixes and clean ups</li>
</ul>


# DataNucleus AccessPlatform 3.0.0.M5

__Jun 14th 2011__ : _Version 3.0 Milestone 5_ includes the following changes

<ul>
<li>Add support for custom class-level and field-level annotations.</li>
<li>Add support for "native" value generator when field of different type to expected (String &lt;-&gt; long)</li>
<li>Fix to in-memory query evaluation of String.substring to cater for IndexOutOfBounds</li>
<li>Support for typing of variables in JDO Typesafe queries</li>
<li>Fix to not call "fetch" when persisting a new object under some situations</li>
<li>Support for persistence of Calendar as a String (where required by the datastore)</li>
<li>Provision of query extensions static final Strings for easier refactoring</li>
<li>Support for query extensions that are boolean to be specified as that type rather than String</li>
<li>Enhancer : allow user plugin bundles</li>
<li>JPA : Support for dynamic generation of "persistence-unit"</li>
<li>JPA : fix for use of Enum without jdbcType</li>
<li>RDBMS : fix to possible lockup due to internal map usage for schema</li>
<li>RDBMS : Enable BINARY/VARBINARY support for MySQL</li>
<li>RDBMS : Support for max/min of temporal expressions in queries</li>
<li>RDBMS : fix to case of subquery that was not precompilable so mark the outer query as not precompilable too</li>
<li>RDBMS : fix to Oracle when using DISTINCT to not select BLOB/CLOB columns</li>
<li>RDBMS : Migrate to BoneCP 0.7+</li>
<li>RDBMS : Support detection of timeout exceptions in JDOQL</li>
<li>RDBMS : Fix to some situations of "complete-table" inheritance strategy usage</li>
<li>ODF : Support persist of byte[] fields</li>
<li>ODF : Support for "increment"/"table" value generator</li>
<li>ODF : fix to retrieval of map field</li>
<li>Excel : fix to ordering of inserts so we don't overwrite rows/columns</li>
<li>Excel : fix to retrieve of map field</li>
<li>Excel : Support for "increment"/"table" value generator</li>
<li>Excel : Support persist of byte[] fields</li>
<li>HBase : Cache datastore-query compilation</li>
<li>HBase : Fix to "hbase" dependency maven groupId</li>
<li>HBase : Support for persistence of non-serialised map fields</li>
<li>HBase : Support use of embedded field references in queries in-datastore</li>
<li>HBase : Support for simple parameter values in queries in-datastore</li>
<li>MongoDB : fix to "increment" value generator</li>
<li>MongoDB : fix to exceptions thrown on MongoDB problems to match JDO/JPA specs</li>
<li>MongoDB : Fix to use of specified datastore name</li>
<li>MongoDB : Support for schema validation with SchemaTool</li>
<li>MongoDB : Support for persistence of Date/Calendar as Date (rather than String)</li>
<li>MongoDB : Support for persistence of maps with Enums keys/values</li>
<li>MongoDB : Fix to persist of array field</li>
<li>MongoDB : Cache datastore-query compilation</li>
<li>IDEA : inclusion of plugin for IDEA, previously developed as separate project (downloadable from Intellij also)</li>
</ul>


# DataNucleus AccessPlatform 3.0.0.M4

__May 9th 2011__ : _Version 3.0 Milestone 4_ includes the following changes

<ul>
<li>Fix to embedded field handling for RDBMS where an embedded object has a relation to a
    non-embedded object.</li>
<li>Allow property methods (getter/setter) to be final and still handle persistence</li>
<li>Fix to single-string parse for JDOQL/JPQL when using multiple subqueries</li>
<li>Fix to JDOQL parse for typesafe query to allow for null literal</li>
<li>Fix to persistence of Date as String for those datastores that need it</li>
<li>Fix to corner case on retrieval by identity to check inheritance via discriminator</li>
<li>Provide mechanism for allowing persistence properties to be specifiable on the EM/PM</li>
<li>SchemaTool : support additional properties on delete/validate, and allow DDL for RDBMS on delete</li>
<li>Support use with JBoss 6.0</li>
<li>OSGi : Fix to handle invalid MANIFEST.MF in external bundles</li>
<li>Enhancer : fix to javaagent enhancer to use the same class-loader for all enhancement</li>
<li>Enhancer : fix minor FindBugs issues in enhanced code</li>
<li>JPA : Fix to caseof mapped-superclass with first child entity using SINGLE_TABLE</li>
<li>JPA : Fix to not cache query results with any query since JPA has no mechanism to free them</li>
<li>JPA : Fixes to ManagedType.getXXXAttributes</li>
<li>JPA : Improvement to Validator exceptions</li>
<li>JPA : Fix to selection of aggregate and use of query.getResultList()</li>
<li>JDO : Fix to annotation reader for ArrayIndexOutOfBounds</li>
<li>MongoDB : Support persistence of Enum fields</li>
<li>MongoDB : Fix persistence of Date fields</li>
<li>MongoDB : Fix to make sure all SCO fields are wrapped</li>
<li>HBase : Change JDOQL/JPQL to evaluate simple filters in the datastore</li>
<li>HBase : Support persistence of Enum fields</li>
<li>HBase : Fix persistence of Date fields</li>
<li>HBase : Fix to make sure all SCO fields are wrapped</li>
<li>Excel : Support persistence of Map fields</li>
<li>ODF : Support persistence of Map fields</li>
<li>ODF : Support SchemaTool creation</li>
<li>RDBMS : Fix to use of range in caching of queries</li>
<li>RDBMS : Support JDOQL String.equalsIgnoreCase()</li>
<li>RDBMS : Fix to when query results are read-in (i.e at commit, rather than at flush) matching
    when any connection is closing</li>
<li>RDBMS : Fix JDOQL/JPQL to check for reference to non-persistent field</li>
<li>RDBMS : Support for subqueries in result and order clauses of JDOQL/JPQL queries</li>
</ul>


# DataNucleus AccessPlatform 3.0.0.M3

__Apr 2nd 2011__ : _Version 3.0 Milestone 3_ includes the following changes

<ul>
<li>JDO : Support for JDO 3.1 PersistenceManager property methods.</li>
<li>JDO : Support bulk update/delete via typesafe API (extension)</li>
<li>JPA : Support &lt;association-override&gt;</li>
<li>JPA : Support &lt;discriminator-column&gt; "length"</li>
<li>JPA : Support EMF singleton pattern</li>
<li>JPA : Bug fixes to @CollectionTable, &lt;inheritance&gt;, and user specification of
    detachXXX persistence properties</li>
<li>OSGi : add optional import of log4j</li>
<li>Bug fix so that calls to PC.setXXX for SCO field immediately wraps the field and so can detect
    subsequent changes</li>
<li>Various changes to default values for persistence properties to better suit all supported
    datastores</li>
<li>Fixes to 300+ possible errors shown up by "FindBugs"</li>
<li>Improvements to nontransactional persistence process</li>
<li>Fixes for JDOQL/JPQL querying with subqueries to correctly cache the compilation, and to cater
    for nested subqueries</li>
<li>Fixes to persistence of nested embedded fields to be independent of ordering</li>
<li>Support for "optimised flush" process, particularly for datastores that don't support
    referential integrity (so we can do bulk inserts, bulk deletes etc)</li>
<li>Support for detachAllOnCommit, pbrAtCommit, serializeRead to be specifiable during
    the lifecycle of a PM/EM</li>
<li>Rewrite Query execution process to not use a separate thread</li>
<li>SchemaTool : ability to just generate tables, or just generate constraints</li>
<li>Cache : support for xmemcached</li>
<li>Cache : support for latest versions of EHCache</li>
<li>ODF : Upgrade to ODFDOM 0.8.7</li>
<li>RDBMS : Enable prepared statement caching, and fix related issue for C3P0</li>
<li>RDBMS : Updates to JPQL to support joins relative to joined tables</li>
<li>RDBMS : Checks for List.set when using ordered list</li>
<li>RDBMS : Fix to table generator to use the initial-value</li>
<li>RDBMS : Fix to use of parameters in query ORDER BY clause</li>
<li>HBase : support optimised delete of obejcts</li>
<li>HBase : support persistence of primitives as raw bytes</li>
<li>MongoDB : support optimised insert of objects</li>
<li>Enhancer : ability to turn off all System.out</li>
</ul>


# DataNucleus AccessPlatform 3.0.0.M2

__Mar 1st 2011__ : _Version 3.0 Milestone 2_ includes the following changes

<ul>
<li>Change plugin startup process to use DataNucleus plugins only (by default), to ignore
    any plugins that have invalid MANIFESTs, and by default to omit the validation of
    bundle dependencies.</li>
<li>Add associated value logic to FK maps, to potentially reduce SQL invoked</li>
<li>Reduced memory utilisation by dropping ObjectProviderImpl, ExecutionContextImpl</li>
<li>Fix to use of embedded objects which was creating too many objects</li>
<li>Support marking some classes as "read-only"</li>
<li>JDO : Official support for "complete-table" (now part of JDO3.1)</li>
<li>JPA : Fix to compilation of JPQL "NOT IN (subquery)" syntax</li>
<li>JPA : Support for @MapKeyEnumerated</li>
<li>JPA : Fix to Query.setLockMode when "SELECT" - throw exception</li>
<li>JPA : EntityManager.close throws IllegalStateException if container managed</li>
<li>JPA : Fix metamodel to handle recursion and static fields</li>
<li>JPA : Fix processing of &lt;column&gt; within unique-constraints in <i>orm.xml</i></li>
<li>JPA : Add support for setting properties on EntityManager</li>
<li>JPA : Fix to &lt;embeddable&gt; trailing tag processing</li>
<li>JPA : Fix to use of listeners when specified via annotations and <i>orm.xml</i></li>
<li>RDBMS : Support for JDOQL "interfaceField = :implValue"</li>
<li>RDBMS : Fix to race condition in statement batching (Gerd Behrmann)</li>
<li>RDBMS : Fix to "count" result size method to allow for ranges</li>
<li>RDBMS : Support for PostgreSQL "SIMILAR TO" method in JDOQL ("String.similarTo")</li>
<li>Excel : Support for querying interfaces</li>
<li>Excel : Support access to native connection</li>
<li>ODF : Support for querying interfaces</li>
<li>ODF : Support access to native connection</li>
<li>XML : Support for querying interfaces</li>
<li>HBase : Support for querying interfaces</li>
<li>HBase : Support for cascade delete with pessimistic txns</li>
<li>HBase : Support discriminators</li>
<li>HBase : Support fetch plan on retrieve of objects</li>
<li>HBase : Support optimistic checks</li>
<li>HBase : Support polymorphic queries</li>
<li>HBase : Fix to use of server URL</li>
<li>MongoDB : Support for querying interfaces</li>
<li>MongoDB : Support access to native connection</li>
<li>MongoDB : Support polymorphic queries</li>
<li>MongoDB : Support optimistic checks</li>
<li>MongoDB : Support for SchemaTool</li>
<li>MongoDB : Support "increment"/"table" value generator</li>
<li>MongoDB : Support nested embedded persistable fields</li>
<li>MongoDB : Support authentication of connections</li>
<li>MongoDB : Support cascade delete for pessimistic txns</li>
<li>MongoDB : Support embedded 1-1/N-1 as embedded document</li>
<li>MongoDB : Support embedded 1-N/M-N as embedded array</li>
<li>MongoDB : Support fetch plan on retrieve of objects</li>
<li>MongoDB : Support persistence of maps</li>
<li>MongoDB : Support embedded maps as embedded array</li>
<li>MongoDB : Support versions</li>
<li>MongoDB : Support "identity" value generator using MongoDB "_id" field</li>
<li>LDAP : Support for "native"/"auto" value generation strategy (to use uuid-hex)</li>
</ul>


# DataNucleus AccessPlatform 3.0.0.M1

__Feb 2nd 2011__ : _Version 3.0 Milestone 1_ includes the following changes

<ul>
<li>Split JDO API into separate "api.jdo" plugin</li>
<li>Repackage JPA API into "api.jpa" plugin</li>
<li>Repackage Rest API into "api.rest" plugin</li>
<li>Basic JSON API added ("api.json") - not yet documented</li>
<li>Much refactoring to allow for Data Federation</li>
<li>Data Federation : Basic mechanism to specify secondary datastores on PMF/EMF</li>
<li>Data Federation : Basic mechanism to specify persistence of class to secondary datastore</li>
<li>JDO : Change @Serialized handling to imply @Persistent</li>
<li>Support persistence of fields of type Class</li>
<li>Change handling of embedded fields so that defaults to column definition of embedded type when
    embedded details not specified</li>
<li>Excel : Support for use with SchemaTool to create/delete worksheets</li>
<li>NeoDatis : Support for unique key creation</li>
<li>NeoDatis : Build against latest version (1.9.30)</li>
<li>HBase : Build against latest version (0.90.0)</li>
<li>HBase : Support for relationships</li>
<li>HBase : Support for (nested) embedded persistable fields</li>
<li>HBase : Support for use with SchemaTool to create/delete tables/families</li>
<li>HBase : Support for datastore identity</li>
<li>HBase : Support for surrogate versions</li>
<li>HBase : Addition of new increment value generator (Peter Rainer)</li>
<li>MongoDB : Addition of plugin for basic persistence</li>
<li>MongoDB : Support for datastore identity</li>
<li>RDBMS : Fix to corner case where version was not being set on a queried object</li>
<li>RDBMS : Fix for Derby 10.6 handling of boolean/integer comparisons</li>
<li>RDBMS : Fix to collection.contains when using primitive</li>
<li>RDBMS : Fix to index creation for PostgreSQL to not prefix the schema name</li>
<li>RDBMS : Fix to HSQLDB 1.7 and earlier handling of transaction isolation</li>
<li>RDBMS : Fix to iterator handling for datastores that don't evaluate range in the datastore</li>
</ul>
