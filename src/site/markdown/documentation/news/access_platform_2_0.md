<head><title>AccessPlatform 2.0</title></head>

#Release Notes for DataNucleus AccessPlatform v2.0

The 2.0 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 2.0_ includes the following over 1.1

<ul>
<li>Addition of plugin for persistence to HBase (HADOOP) datastores</li>
<li>Support for persistence to Amazon S3 datastores</li>
<li>Support for persistence to Oracle Timesten datastores</li>
<li>Addition of plugin for persistence of JodaTime types</li>
<li>Change default for non-transactional read/write to true for JDO</li>
<li>Support atomic non-transactional write persist/delete operations</li>
<li>Level 2 Cache is now enabled by default (soft)</li>
<li>Cache : Support for pinning/unpinning of query results with Memcache/javax.cache</li>
<li>Split query cache into 3 components : generic compilation, datastore compilation
    and query results. Added API for managing caching of query results (using JDO or JPA).</li>
<li>Enhancer : add ability to generate PK classes (including composite)</li>
<li>JDO : Support for JDO 2.3 Query cancel, and datastore read/write timeout</li>
<li>JPA : Support for extended persistence context</li>
<li>JPA2 : Support for metamodel API</li>
<li>JPA2 : Support for bean validation API</li>
<li>JPA2 : Support for various JPQL keywords</li>
<li>JPA2 : Support for 1-N FK bidirectional relations</li>
<li>JPA2 : Support for 1-N collection/map of non-persistable objects.</li>
<li>JPA2 : Support for TypedQuery</li>
<li>RDBMS : Support for update/delete-by-query for JPQL</li>
<li>RDBMS : Rewritten JPQL implementation building on generic query compiler. 
    This is now the default JPQL implementation for RDBMS, and can be used with the query caching mechanism.</li>
<li>RDBMS : Rewritten JDOQL implementation building on generic query compiler.
    This is not currently the default JDOQL implementation but is available to be used, and can be used with the query caching mechanism.</li>
<li>LDAP : Support for persistence of recursive object graph to hierarchical structure</li>
<li>Add support for PMF/EMF singleton pattern, via persistence property</li>
<li>Spatial : Many fixes to handling of JTS types.</li>
<li>Many bug fixes, and minor feature additions.</li>
</ul>



# DataNucleus AccessPlatform 2.0.5

__Jul 1st 2010__ : _Version 2.0.5_ includes the following changes

<ul>
<li>Fix to persistence of BLOBs/CLOBs on Oracle for some corner-case relationships</li>
</ul>


# DataNucleus AccessPlatform 2.0.4

__Apr 22nd 2010__ : _Version 2.0.4_ includes the following changes

<ul>
<li>Fix to support non-standard SQL statements (stored procs, statements not starting with SELECT/INSERT/UPDATE/MERGE/DELETE)</li>
<li>Fix to the query in-memory evaluator to support aggregate names in upper or lower case</li>
<li>Fix to a couple of situations where a versioned object can be returned to the user without the version set</li>
<li>Fix to reset the version of an object on rollback()</li>
<li>Fix to SCOListIterator</li>
<li>RDBMS : Fix to generation of indexes for reference fields when having a FK per implementation
    so that the index is created for the implementations FK only</li>
<li>JDOQL2 : Fix to use of input parameters with multiple columns</li>
<li>Enhancer : when using JDK1.6 and having the enhancer in the CLASSPATH default to not enabling
    the annotation processor to enhance the class(es) being compiled</li>
</ul>


# DataNucleus AccessPlatform 2.0.3

__Apr 1st 2010__ : _Version 2.0.3_ includes the following changes

<ul>
<li>Fix to a typo in the use of ConnectionFactory when defining the datastore as a DataSource</li>
<li>Cleanup to process of creation of L1/L2/Query caches</li>
<li>Fix to use of Extent to close all iterators correctly</li>
<li>Fix to generic compilation of cast expressions</li>
<li>Added checks on invalid use of keywords during generic compialtion</li>
<li>Fix to generic compilation of {array}.length</li>
<li>Fix to getParent() of class/package metadata of JDO Metadata API</li>
<li>Fix to use of set() on ListIterator obtained from list wrapper</li>
<li>Fix to persistence of object with reference to the same object</li>
<li>RDBMS : having expression that are not boolean should throw XXXUserException in JDOQL2</li>
<li>RDBMS : fix to use of parameters for range and passed in as unnamed to API</li>
<li>RDBMS : fix to caching of JDOQL2 queries when using String.matches with input parameter</li>
<li>RDBMS : fix to not create indexes for serialised field (problem on MySQL)</li>
</ul>


# DataNucleus AccessPlatform 2.0.2

__Mar 6th 2010__ : _Version 2.0.2_ includes the following changes

<ul>
<li>Fix to the auto-generation of PK classes by the enhancer for some field types.</li>
<li>Fixes to generic compilation of collection.contains when using variables</li>
<li>Support for in-memory query evaluation of Enum.toString() and Enum.ordinal()</li>
<li>Fixes to in-memory query evaluation of boolean predicates, and loading of fields</li>
<li>Fix to use of result class with constructor with arguments when one argument is null</li>
<li>Support for use of encrypted passwords in persistence properties</li>
<li>RDBMS : Fix to handling of FKs when specified on fields</li>
<li>Support for persisting java.awt.Color/Point/Rectangle and java.util.BitSet field types as String</li>
<li>RDBMS : JDOQL2 - Fixes to use of Extent for no concrete classes, subclass-table inheritance,
    and persistence interface cases</li>
<li>RDBMS : JDOQL2 - Support for use of variables</li>
<li>RDBMS : JDOQL2 - Support for Collection.contains on embedded fields</li>
<li>RDBMS : JDOQL2 - Support for binding parameter type via Collection.contains, Map.containsXXX methods</li>
<li>RDBMS : JDOQL2 - Detect result clauses that are multi-valued and throw exception</li>
<li>RDBMS : JDOQL2 - Fixes to allow many complex queries that failed with "JDOQL" to work
    with this new implementation.</li>
<li>RDBMS : JDOQL2 - Fix to String.matches escape clause</li>
<li>JPA : Support for CONCAT methods with Criteria Query</li>
<li>JPA : Support for COALESCE methods with Criteria Query</li>
<li>JPA : Support for function() method with Criteria Query</li>
<li>JPA : Support for joins specified using string name with Criteria Query</li>
<li>JPA : Support for negated predicates with Criteria Query</li>
<li>JPA : Support for subqueries with Criteria Query</li>
<li>Excel : Support persistence of Enum fields</li>
<li>Excel : Support for persistence of relation fields (as per ODF plugin)</li>
<li>Excel : Fixes to persistence of Date/Calendar types</li>
<li>Excel : Fixes to handling of SCO fields so they are wrapped correctly</li>
<li>Excel : Upgrade Apache POI requirement to 3.6+</li>
<li>ODF : Fixes to handling of SCO fields so they are wrapped correctly</li>
<li>ODF : Fixes to persistence of Date/Calendar types</li>
<li>ODF : Support persistence of Enum fields</li>
<li>XML : Fix to persistence of Enum fields</li>
</ul>


# DataNucleus AccessPlatform 2.0.1

__Feb 6th 2010__ : _Version 2.0.1_ includes the following changes

<ul>
<li>Support for JPA2 Criteria query API (doesn't yet support subqueries, and some less useful
   query builder methods)</li>
<li>Change all primitive wrapper constructor usage to use class valueOf() for efficiency</li>
<li>Fix to annotation processing to ignore all unsupported class annotations, and to correctly
    handle methods called get(), is()</li>
<li>Complete generic compile of JPQL TRIM and LIKE keywords, and support COALESCE, NULLIF keywords</li>
<li>Add support for in-memory query evaluation of COALESCE/NULLIF keywords</li>
<li>Update in-memory query evaluator to load fields where needed</li>
<li>Minor fixes to JDO getObjectById to pass new tests in JDO2.3 TCK</li>
<li>Minor changes to JDO timeout setter methods to pass new tests in JDO2.3 TCK</li>
<li>Fix to L2 cache retrieval of relation field to use the value</li>
<li>Fix to use of @Persistent and @Extension on a field, so that the settings are respected</li>
<li>Clean up of generic query compilation expressions to not use SymbolTable before bind()</li>
<li>XML : Fix to handling of empty XML file when searching for an object</li>
<li>RDBMS : respect "indexed" value of false when creating indexes</li>
<li>RDBMS : fix to SQL embed extension so we have SQL_boolean, SQL_numeric static functions</li>
<li>RDBMS : support for JPQL COALESCE, NULLIF functions</li>
<li>RDBMS : fix to JPQL to not add dup joins when defined in FROM clause and also from result</li>
<li>RDBMS : JPQL - support for ESCAPE on LIKE, and support for all TRIM options</li>
<li>Add support for persisting some java types as Long where no native handling</li>
<li>HBase : better handling of update to not delete records</li>
<li>DB4O : upgrade to 7.12 and above</li>
</ul>


# DataNucleus AccessPlatform 2.0.0.RELEASE

__Jan 9th 2010__ : _Version 2.0 RELEASE_ includes the following changes

<ul>
<li>Align to recent changes in JDO2.3 timeout API</li>
<li>Fix to Spatial handling of JTS types</li>
<li>Support for many spatial methods with the rewritten RDBMS JDOQL/JPQL query mechanism</li>
</ul>


# DataNucleus AccessPlatform 2.0.0.M4

__Dec 7th 2009__ : _Version 2.0 Milestone 4_ includes the following changes

<ul>
<li>Require use of a JPA2 jar when used for JPA persistence</li>
<li>Change handling of JDO @PrimaryKey to not require @Persistent for non-default persistent fields</li>
<li>Change generic compilation of subqueries, particularly for JPQL, to allow for multi-level
    primary expression</li>
<li>Change generic compilation of JPQL "LOCATE" to handle multi-level primary expressions</li>
<li>Fix to JDO PersistenceManagerProxy for named queries (typo)</li>
<li>Provide framework for bulk object retrieval (available to datastore-specific plugins)</li>
<li>Fix handling of query parameters to allow for use of parameters in subqueries</li>
<li>Respect "RetainValues" setting for objects that are deleted (so field values can be retained
    after the transaction commits, and the object is deleted).</li>
<li>Add support for PMF/EMF singleton pattern, via persistence property</li>
<li>Add support for case-insensitive persistence properties (previously all were case sensitive)</li>
<li>JPA2 : Support for "Metamodel" API</li>
<li>JPA2 : Support for TypedQuery</li>
<li>JPA2 : Support for Bean Validation</li>
<li>JPA : Fix to runtime enhancer</li>
<li>Enhancer : add ability to turn on/off capabilities</li>
<li>Enhancer : add ability to generate PK classes (including composite)</li>
<li>Enhancer : add ability to turn off generation of default constructor</li>
<li>Enhancer : add short form of "persistenceUnit" argument</li>
<li>RDBMS : Change to use "JPQL2" implementation by default since it passes the JPA1 TCK</li>
<li>RDBMS : Fix to JDOQL2/JPQL2 for case where multiple classes share a table and use a discriminator</li>
<li>RDBMS : Support for embedded fields in JDOQL2/JPQL2</li>
<li>RDBMS : Query range not working for Oracle now fixed</li>
<li>RDBMS : Fix to FROM join in JPQL2 for second and subsequent joins</li>
<li>RDBMS : Add support to JPQL2 for subquery FROM clauses with multiple joins</li>
<li>RDBMS : Fix support in JPQL2 for "COUNT (DISTINCT ...)"</li>
<li>RDBMS : Support for JPA2 "TYPE" in JPQL2 implementation</li>
<li>RDBMS : Support for "StringExpression == EnumLiteral" in JDOQL2/JPQL2</li>
<li>RDBMS : Change to "persistenceUnit" option of SchemaTool to allow short form</li>
<li>RDBMS : Fix for read of null BLOB with Oracle</li>
<li>Spatial : fix to M2 dependencies to make some optional</li>
<li>HBase : add security handling to cater for issues in HBase itself</li>
<li>Maven2 plugin : Support for enhancement generating PKs, and turn on/off default constructor</li>
</ul>


# DataNucleus AccessPlatform 2.0.0.M3

__Oct 24th 2009__ : _Version 2.0 Milestone 3_ includes the following changes

<ul>
<li>Allow override of basic settings of DFG, default persistent for java types</li>
<li>Fix to L2 cache handling to evict deleted object</li>
<li>Level 2 Cache is now enabled by default (soft)</li>
<li>Level 1 Cache default is now changed to soft</li>
<li>Support for max size on weak/soft Level 2 caches</li>
<li>Generic compile updated for JPQL "EMPTY"/"LIKE"/"SIZE" to allow for multi-level primaries</li>
<li>Generic compile updated for JPQL "FROM" to chain nodes correctly</li>
<li>Generic compile updated for JPQL Object/Sum/Avg/Min/Max/Count to allow for case-insensitive</li>
<li>Generic compile updated for JPQL to allow for case-insensitive aliases</li>
<li>Generic compile updated for JPQL to fix escape sequence</li>
<li>Generic compile of JPQL subqueries to correctly allow for ALL/ANY/SOME/EXISTS forms</li>
<li>Generic compile support for AS aliases in result clause</li>
<li>Generic compile support for "new XXX().method" constructs</li>
<li>Generic compile support for JPQL "IN" taking multi-value parameters (JPA2)</li>
<li>Generic compile fix for JPQL "MOD"</li>
<li>Generic compile fix for JPQL "NOT" being applied incorrectly</li>
<li>Generic compile support for JPQL "TYPE" syntax (JPA2)</li>
<li>Generic compile fix for specification of result class in single-string form not being respected</li>
<li>Ignore all unsupported annotations</li>
<li>Rewrite of query in-memory method invocations handler to match the RDBMS style type-method</li>
<li>Fix to handling of non-transactional objects at pm close to move through lifecycle correctly</li>
<li>Support for JDO Query.cancel(Thread)</li>
<li>JPA : fix to mark transaction for rollback only on error</li>
<li>JPA : Support @Column length correctly</li>
<li>RDBMS : JDOQL2 support for String concatenation, and support for parameter defined
    as supertype but passed in as subtype</li>
<li>RDBMS : JDOQL2/JPQL2 support for Oracle NLS sorting</li>
<li>RDBMS : JDOQL2/JPQL2 support for result of type DyadicExpression</li>
<li>RDBMS : JDOQL2/JPQL2 support for result expression aliases</li>
<li>RDBMS : JDOQL2/JPQL2 fix handling of result new object to handle objects with composite PKs</li>
<li>RDBMS : JDOQL2/JPQL2 fix to handling of boolean expressions in ==/!=</li>
<li>RDBMS : JDOQL2/JPQL2 fix to handling of mappings using non-default datastore mapping (e.g Date persisted as VARCHAR)</li>
<li>RDBMS : JPQL2 fix to handling of ANY/ALL/SOME/EXISTS</li>
<li>RDBMS : JPQL2 fix to bulk update to allow DyadicExpression/PrimaryExpression in SET clause</li>
<li>RDBMS : Fix to Schematool to remove possible dups with bidirectional relations</li>
<li>RDBMS : Support for user-defined primary key constraints on join tables</li>
<li>RDBMS : Fix to support persisting Boolean as SMALLINT/TINYINT</li>
<li>JSON : support for Amazon S3 datastores</li>
<li>HBase : upgrade to HBase 0.20</li>
<li>HBase : performance improvements, including connection pooling and create schema only once</li>
<li>HBase : support for column families</li>
<li>Excel : Use lazy loading when retrieving candidate instances</li>
<li>ODF : Fix to delete of an object</li>
<li>ODF : Use lazy loading when retrieving candidate instances</li>
<li>ODF : Support for persistence of null fields and retrieval as null</li>
<li>ODF : Support for persistence/retrieval of Date fields</li>
<li>XML : Use lazy loading when retrieving candidate instances</li>
</ul>


# DataNucleus AccessPlatform 2.0.0.M2

__Sept 11th 2009__ : _Version 2.0 Milestone 2_ includes the following changes

<ul>
<li>Addition of control over the Locale used for logging messages</li>
<li>Add support for "embedded='true'" to mean embed the field - so the user doesn't have to
    specify the 'embedded' element also</li>
<li>Bug fix to handling of embedded collections</li>
<li>Fix to generic query compilation for words starting "new"</li>
<li>Fix to JDOQL compilation of subquery FROM clause</li>
<li>Fix to the attach of nested embedded objects</li>
<li>Improvements to the query results cache to allow pinning/unpinning and to not validate</li>
<li>Fix to JTA handling introduced in M1 release</li>
<li>Add support for "detachAllOnRollback"</li>
<li>Removal of unnecessary flush on 1-1 relation</li>
<li>Bug fix to usage when invoked path has "+" symbol</li>
<li>Addition of plugin for persistence of primary JodaTime types, and simple querying for RDBMS</li>
<li>Cache : Support for pinning/unpinning of query results with Memcache/javax.cache</li>
<li>Enhancer : Bug fix to return code from enhancer when run from command line</li>
<li>JPA : Support for JPA "extended persistence context"</li>
<li>JPA : Fix to use of @EmbeddedId in extended persistence context</li>
<li>JPA : Support for optional attribute of @ManyToOne</li>
<li>LDAP : Support for persistence of recursive object graph to hierarchical structure</li>
<li>RDBMS : Addition of support for persistence to Oracle TimesTen datastore (Anton Troshin)</li>
<li>RDBMS : JDOQL2 support for "SELECT this" queries, and DISTINCT</li>
<li>RDBMS : JDOQL2 support for temporal queries</li>
<li>RDBMS : JDOQL2 support for subqueries</li>
<li>RDBMS : JPQL2 support for subqueries</li>
<li>RDBMS : JPQL2 support for bulk update/delete by query</li>
<li>RDBMS : SQL API fixes to cater for composite PKs and ordering of expressions</li>
<li>RDBMS : Improvements to choice of whether to use UNION or discriminator for inheritance detection</li>
<li>RDBMS : Some fixes to handling of temporal types to add more flexibility</li>
</ul>


# DataNucleus AccessPlatform 2.0.0.M1

__Jul 30th 2009__ : _Version 2.0 Milestone 1_ includes the following changes

<ul>
<li>Addition of plugin for persistence to HBase (HADOOP) datastores</li>
<li>Allow query execution in separate thread to allow for cancel/timeout hooks</li>
<li>Change default for non-transactional read/write to true for JDO</li>
<li>Support atomic non-transactional write persist/delete operations</li>
<li>Support for in-memory evaluation of queries with variables</li>
<li>Support for in-memory evaluation of queries with List.get(), and ranges using parameters</li>
<li>Drop support for various extensions that were standardised during version 1.1 timeframe</li>
<li>Split query cache into 3 components : generic compilation, datastore compilation
    and query results. Added API for managing caching of query results (using JDO or JPA).</li>
<li>Internal changes to implementation of StoreManager making it even easier to provide
    support for new datastores</li>
<li>Bug fix for annotation of unmapped columns in JDO</li>
<li>Refactor all legacy query classes into own package for removal during 2.0 timeline</li>
<li>Bug fix to JDO Metadata "index" when unique flag not defined</li>
<li>RDBMS : Fix to COMPLETE_TABLE inheritance when used with JDOQL2</li>
<li>RDBMS : Change default auto-start mechanism to "None"</li>
<li>RDBMS : JDOQL2 support for input params with multiple columns</li>
<li>RDBMS : JDOQL2 support for List.get()</li>
<li>RDBMS : JDOQL2 support for range defined with input parameters</li>
<li>RDBMS : JDOQL2/JPQL2 support for views</li>
<li>RDBMS : Revised handling of nullability on joins</li>
<li>RDBMS : Support for table creation with columns having default of NULL</li>
<li>RDBMS : Support for specifying the order of columns in DDL</li>
<li>Much internal refactoring has also been performed to remove unneeded components
    or to simplify the API's for things needed in the 2.0 timeline. Any use of internal
    API's by applications will likely need changes.</li>
</ul>
