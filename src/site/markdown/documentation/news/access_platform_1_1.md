<head><title>AccessPlatform 1.1</title></head>

#Release Notes for DataNucleus AccessPlatform v1.1

The 1.1 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 1.1_ includes the following over 1.0

<ul>
<li>Requires JDK1.5+</li>
<li>Support for in-memory evaluation of JDOQL/JPQL subqueries</li>
<li>Support for JDO2 PersistenceManager proxy</li>
<li>Support for JDO2.3 Metadata API</li>
<li>Support for JDO2.3 Enhancer API</li>
<li>Support for JDO2.3 query timeout/cancel API</li>
<li>Support for JDO2.2 transaction isolation control</li>
<li>JPA2 preview support for datastore cache, @OrderColumn, standardised properties, and various
    new query methods</li>
<li>RDBMS : rewrite of locate, fetch and some select SQL using a new SQL API</li>
<li>RDBMS : start of an alternative JDOQL implementation using a new SQL API</li>
<li>RDBMS : Support for persistence of interface fields into a single column</li>
<li>ODF : Support for persistence/querying of OpenDocument format spreadsheets</li>
<li>XML : Added support for 1-1, 1-N, M-N relations</li>
<li>XML : Added many improvements in configurability</li>
<li>LDAP : Support for various new mapping configurations.</li>
<li>LDAP : Support for native querying</li>
<li>Support for enhancement as part of the compilation process (JDK1.6+)</li>
<li>Dropped support for NucleusSQL query language</li>
<li>Dropped support for BCEL enhancer</li>
</ul>


# DataNucleus AccessPlatform 1.1.6

__Oct 11th 2009__ : _Version 1.1.6_ includes the following changes

<ul>
<li>Bug fix to PersistenceManager proxy in multithreaded environments</li>
<li>Bug fix to interface mapping strategy "xcalia"</li>
<li>LDAP : Add support for enums</li>
<li>RDBMS : Bug fix to instanceof when handling possible subclasses</li>
<li>RDBMS : Bug fix to detection of discriminator when handling superclasses</li>
</ul>


# DataNucleus AccessPlatform 1.1.5

__Jul 15th 2009__ : _Version 1.1.5_ includes the following changes

<ul>
<li>Support minor changes to JDO2.3 API post 2.3-early-access</li>
<li>Bug fix to generic compilation of invoke expressions</li>
<li>Bug fix to use of "persistence.xml" in a path with spaces in it</li>
<li>Bug fix to JPA query repeated setting of the first postion</li>
<li>RDBMS : Bug fix to SchemaTool, broken in 1.1.4</li>
<li>RDBMS : Bug fix to querying when enum is null</li>
<li>RDBMS : Add support for persisting all date types as a String in a consistent way</li>
<li>RDBMS : Revision to nullability handling and joins</li>
<li>RDBMS : updates to very minor corner-case possibilities of connection leaks</li>
</ul>


# DataNucleus AccessPlatform 1.1.4

__Jun 17th 2009__ : _Version 1.1.4_ includes the following changes

<ul>
<li>Make the query cache pluggable, allowing use of external caching products</li>
<li>Add support for use of Memcache, javax.cache, and EHCache for the query cache</li>
<li>Addition of upfront checks on whether the datastore supports particular features
    so allowing quick fail</li>
<li>Bug fix to datastores which don't provide non-transactional connections</li>
<li>Simplification of specification of L2 caching, for consistency with L1 cache and
    Query cache.</li>
<li>Improvement to classloading for RDBMS "requests" for use in OSGi containers</li>
<li>Change JPA default for discriminator value to use "class name" when no value specified.</li>
<li>Improvements to fallback process for persisting a type as a String</li>
<li>Add control over cascade delete of map keys, and minor change in default</li>
<li>Bug fix to JPQL "LOWER"/"UPPER" compilation</li>
<li>Bug fix to List.set() methods when using cascade delete</li>
<li>Respect JPA "fetch" setting on 1-1 relations</li>
<li>Support JPA "columnDefinition" in a minimalistic way</li>
<li>RDBMS : Change fetch process to allow fetching of related (1-1, N-1) objects in same SQL</li>
<li>RDBSM : Change to Oracle BLOB/CLOB handling to use new SQL API instead of legacy code.</li>
<li>XML : Bug fix to addition of elements to collection of persistent object</li>
<li>LDAP : Bug fix to JNDI connection pooling</li>
<li>LDAP : Support for persisting embedded elements as child entries</li>
<li>LDAP : Support for inheritance in relationships</li>
</ul>


# DataNucleus AccessPlatform 1.1.3

__May 15th 2009__ : _Version 1.1.3_ includes the following changes

<ul>
<li>Add support for REST API</li>
<li>Add support for Memcache and javax.cache (JSR107) L2 caches</li>
<li>Add support for choosing which JDOQL/JPQL implementation to use.</li>
<li>Generic compilation of bulk update statements</li>
<li>Support for generic compilation of JPQL "KEY", "VALUE", "ENTRY", "SIZE", "LIKE",
    "SUBSTRING", "LENGTH", "CONCAT", "TRIM", "LOWER", "UPPER", "LOCATE" keywords
    as well as fixes to compilation of "NOT BETWEEN", "JOIN FETCH" keywords</li>
<li>Fixes to generic compilation of JPQL "Object(a)", from clause</li>
<li>Fixes to input parameter handling for generic JPQL/JDOQL queries, including much improved
    type checking</li>
<li>Add support for allowing multiple JPA inheritance strategies in an inheritance tree
    (JPA extension).</li>
<li>Bug fix to replication for embedded-only classes</li>
<li>Bug fix to allow handling of multi-level generic annotations</li>
<li>Fix to detachAllOnCommit to mean we don't have DN wrappers in detached objects
    so objects are ready for use in clients.</li>
<li>Fix to JPAReplicationManager for multiple objects</li>
<li>Fix to use of jtaDataSource for RESOURCE_LOCAL contexts</li>
<li>Support for JDO2.3 transaction locking semantics</li>
<li>Support for JPA2 @Cacheable</li>
<li>Bug fix for specification of generation strategy in orm.xml</li>
<li>Bug fix for PK join columns in orm.xml</li>
<li>JDOQL2 : Support for Oracle-specific mappings</li>
<li>Provision of alternative JPQL implementation for RDBMS "JPQL2"</li>
<li>JPQL2 : Support FROM clause join syntaxis</li>
<li>JPQL2 : Support case-insensitive identifiers</li>
<li>JPQL2 : Support for CURRENT_DATE, CURRENT_TIME, CURRENT_TIMESTAMP</li>
<li>JPQL2/JDOQL2 : Cater for input parameters with multiple PK fields</li>
<li>Support for dynamic schema updates for interface implementation in 1-N collections</li>
<li>Minor bug fixes to SchemaTool</li>
<li>Bug fix to the enhancer to close any file that was opened</li>
<li>Bug fix to the enhancer for classes with custom PKs using long fields</li>
<li>Upgrade to NeoDatis 1.9 final</li>
<li>Upgrade to Apache JDO 2.3 "early access" jar</li>
<li>Move to use of Geronimo "JPA1" jar for more flexible license</li>
</ul>


# DataNucleus AccessPlatform 1.1.2

__Apr 15th 2009__ : _Version 1.1.2_ includes the following changes

<ul>
<li>Improvements to fix issues in beforeCompletion/afterCompletion for JTA</li>
<li>Support for null values in HashMap</li>
<li>Generic query compiler support for implicit variables, method invocation on parameters</li>
<li>Generic query compiler support for JPQL "MEMBER OF", EXISTS, ALL, ANY, SUM, as well
    as resolution of entity names.</li>
<li>Generic query compiler support for JDOQL "ascending"/"descending" has been fixed</li>
<li>Bug fix to caching of generic query compilations to make thread safe.</li>
<li>JDO2.3 : Support for future ability to specify read object locking on transaction
    and on query</li>
<li>Level 2 cache : fixes to caching of Object[], Collection&lt;Object&gt;, as well
    as to ordered lists and the state of returned objects from the L2 cache</li>
<li>Managed Relations : support for delete of an object that is present in a collection</li>
<li>Support for backwards compatibility with column identifiers consistent with JPOX</li>
<li>Support for load of all classes below the root of a persistence-unit, and support for
    "exclude-unlisted-classes".</li>
<li>Fixes to allow correct enhancement of Scala classes</li>
<li>Fix support for JPA @Temporal, and complete support for TemporalType on Query API</li>
<li>Fix to JPA XML "generated-value" to handle case-sensitivity correctly</li>
<li>ODF : Support use of ORM files</li>
<li>LDAP : Support use of ORM files</li>
<li>Excel : Support use of ORM files</li>
<li>RDBMS : JDOQL2 - support for Collection.contains, Map.containsKey, Map.containsValue,
    Map.get, Map.containsEntry</li>
<li>RDBMS : JDOQL2 - support for cast, range, grouping, resultClass, new XXX()</li>
<li>RDBMS : JDOQL2 - ArrayLiteral/CollectionLiteral size, contains methods</li>
<li>RDBMS : JDOQL2 - support for String.equals(...)</li>
<li>RDBMS : JDOQL2 - fixes to aggregate types, case and whether to use UNIONs</li>
<li>RDBMS : JDOQL2 - detection of whether a query can be precompiled, and mechanism to
    convert a parameter into its literal form when not precompilable</li>
<li>RDBMS : Fix DB2 schema generation NPE</li>
<li>RDBMS : Use of SERIAL8 in Informix for sequence</li>
<li>RDBMS : Ability to generate schema with multiple PMFs at the same time</li>
<li>RDBMS : Improvement to locking with Derby</li>
<li>RDBMS : Fix to indexed="true" for discriminator and version columns</li>
<li>XML : Fix to the retrieval of objects when the candidate has no "xpath" specified</li>
</ul>


# DataNucleus AccessPlatform 1.1.1

__Mar 17th 2009__ : _Version 1.1.1_ includes the following changes

<ul>
<li>Added support for generic compilation of long form of Math.XXX, JDOHelper.XXX</li>
<li>Added support for parameter.method, parameter.field syntaxis in generic queries</li>
<li>Improved in-memory evaluation of queries to skip candidates that fail sub-expressions
    due to impossible conditions (unimplemented features, or casts etc)</li>
<li>Bug fix to always put objects in the L2 cache after a query</li>
<li>Bug fix to class loading when user has supplied their own loader</li>
<li>Bug fix to JTA with JCA in afterCompletion (Guido Anzuoni)</li>
<li>Bug fix to execution of generically compiled queries with parameters so that subsequent
    invocations use the new parameter values</li>
<li>Bug fix to runtime enhancement and use of @Extension with JPA to avoid ClassCastException</li>
<li>Improvements to ordered lists to handle some operations that require indexed positions</li>
<li>Improvement to object-value-generator to cache the generators</li>
<li>Bug fix to JPA @Basic annotation allowing for tagging of custom type fields as persistent</li>
<li>RDBMS "JDOQL2" : Improved support for various String methods</li>
<li>RDBMS "JDOQL2" : Add support for Math.XXX, JDOHelper.XXX</li>
<li>RDBMS "JDOQL2" : Support for static class fields</li>
<li>RDBMS "JDOQL2" : Support chained method invocations</li>
<li>RDBMS "JDOQL2" : Bug fix to use of parameters when the statement involves unions</li>
<li>RDBMS "JDOQL2" : Support for input Extent</li>
<li>RDBMS "JDOQL2" : Support for enums</li>
<li>RDBMS : Rewrite all backing store "iterator" statements to use new SQL API</li>
<li>RDBMS : Separate all native (SQL) statements into their own log category</li>
</ul>


# DataNucleus AccessPlatform 1.1.0.RELEASE

__Feb 23rd 2009__ : _Version 1.1 RELEASE_ includes the following changes

<ul>
<li>Add support for JDK1.6+ enhancement during the compilation.</li>
<li>Add support for persistence to Open Document Format (ODF) spreadsheets.</li>
</ul>


# DataNucleus AccessPlatform 1.1.0.M4

__Feb 1st 2009__ : _Version 1.1 Milestone 4_ includes the following changes

<ul>
<li>Upgrade to NeoDatis 1.9RC1</li>
<li>Upgrade to latest JDO 2.3 snapshot including Metadata API</li>
<li>Add accessor for available query extensions</li>
<li>Support for in-memory evaluation of JDOQL/JPQL subqueries</li>
<li>Support for JDO2.3 Metadata API</li>
<li>Bug fix to allow registration of persistent classes when loaded by ClassLoader</li>
<li>Support for QueryResult toArray/subList</li>
<li>RDBMS : Make "request" operations pluggable allowing override of INSERT/UPDATE/DELETE etc</li>
<li>RDBMS : Replacement of field fetch process using new SQL API</li>
<li>RDBMS : Replacement of object locate process using new SQL API</li>
<li>RDBMS : Provision of potential replacement JDOQL implementation, using new SQL API</li>
<li>XML : Fix for fields marked transient to not be persisted</li>
<li>XML : Provide default XmlID/XmlIDREF based on relation metadata information</li>
<li>XML : Fix to implement fetch of fields</li>
<li>XML : Support for use of schema/table/column</li>
<li>XML : Bug fix for XmlIDREF for collection fields</li>
<li>LDAP : Support for hierarchical mapping of relations</li>
<li>LDAP : Support for wrappers of primitives</li>
<li>LDAP : Support for map/array/collection of Strings/primitives to multivalued LDAP components</li>
<li>Dropped support for BCEL enhancer</li>
</ul>


# DataNucleus AccessPlatform 1.1.0.M3

__Dec 11th 2008__ : _Version 1.1 Milestone 3_ includes the following changes

<ul>
<li>Upgrade to Apache POI 3.2</li>
<li>Upgrade to JDO 2.3 (snapshot)</li>
<li>New autostarter taking in metadata filenames</li>
<li>Support for pm.getObjectById(String) mimicking custom behaviour of Xcalia 
    (for people migrating from Xcalia)</li>
<li>Support for JDO2 PersistenceManager proxy</li>
<li>Support for JPA2 @OrderColumn</li>
<li>RDBMS : Support for persisting interface/object fields using a single column.
    (for compatibility with Kodo/Xcalia, for people migrating from those implementations)</li>
<li>Support for JDO2.3 Enhancer API</li>
<li>LDAP : Support for native queries rather than performing all in-memory.</li>
<li>LDAP : Improvements to distinguishedName handling</li>
<li>Support for String.startsWith/endsWith/indexOf with parameter/primary expressions</li>
<li>Catch leading/trailing blanks in persistence properties</li>
<li>Support for OpenJPA/Kodo style datastore identity (for people migrating from Kodo)</li>
<li>Support for Xcalia style datastore identity (for people migrating from Xcalia)</li>
<li>Fix for unary minus in generic query mechanism</li>
<li>Remove enhancer "verify" mode since no longer used</li>
<li>Provide access to class bytes after enhancement via enhancer API</li>
<li>Fix to replication in some cases where object didnt exist in datastore 2</li>
<li>Fix to RDBMS large result "count" method to ignore ordering</li>
</ul>


# DataNucleus AccessPlatform 1.1.0.M2

__Oct 31st 2008__ : _Version 1.1 Milestone 2_ includes the following changes

<ul>
<li>Upgrade to ASM 3.1</li>
<li>Upgrade to db4o 7.4 java5</li>
<li>Upgrade to JDO2.2 final</li>
<li>Provide an API for datastore replication for JDO and JPA</li>
<li>Improvements to L2 caching to fix problems with objects being garbage collected and returning
    old version of objects</li>
<li>Fixes to how fields are marked as loaded</li>
<li>Fix to handling of collections with non-RDBMS datastores so they aren't treated as serialised</li>
<li>Improvement to detach flag DETACH_UNLOAD_FIELDS to also remove the values from the object</li>
<li>Fix SQL syntax for non-ANSI joins (e.g Oracle 8i)</li>
<li>Remove support for NucleusSQL for RDBMS datastores</li>
<li>Support for sequences with H2 datastore</li>
<li>Extend RDBMS "update lock" to also apply to object existence check</li>
<li>Fix to handling of URLs with DB4O plugin</li>
<li>Fix to JPA handling of PostLoad callbacks</li>
<li>Fix to LDAP plugin so that the existence check doesnt retrieve any attributes</li>
<li>Fix to handling of XMLIdRef annotation with XML plugin</li>
</ul>


# DataNucleus AccessPlatform 1.1.0.M1

__Sept 23rd 2008__ : _Version 1.1 Milestone 1_ includes the following changes

<ul>
<li>Moved to JDK1.5+ requirement</li>
<li>Removal of Java5 plugin, and addition of JPA plugin</li>
<li>Support for JDO2.2 transaction isolation specification mechanism</li>
<li>Support for JPQL "&lt;&gt;" added to generic query compilation</li>
<li>Support for JDOQL "(cast)" added to generic query compilation</li>
<li>Support for JPQL bulk delete for db4o, NeoDatis, Excel, XML, LDAP and JSON datastores</li>
<li>Support db4o 7.0 or later only</li>
<li>Log any invalid/unsupported persistence properties</li>
<li>Remove support for NucleusSQL for RDBMS datastores</li>
<li>Performance improvement to Excel and XML datastores to not repeatedly open/close the datastore</li>
<li>When checking for RDBMS table existence use DatabaseMetaData.getTables for performance</li>
<li>Fix logging of initialisation of Derby datastores to remove logged exception</li>
<li>Fix logging of initialisation of RDBMS SEQUENCE_TABLE to remove logged exception</li>
<li>Fix bug in loading of unloaded fields to cater for corner case</li>
<li>Fix bug in persistence of 1-N bidir List using cascade delete</li>
<li>Fix available transaction isolation levels for HSQL, H2 datastores</li>
<li>Fix bug in DB4O and NeoDatis JDOQL handling of "{alias}.b" syntax</li>
<li>Fix bug in Extents with subclasses for Excel, XML, LDAP and JSON datastores</li>
<li>Fix bug in LDAP persistence of boolean fields</li>
</ul>
