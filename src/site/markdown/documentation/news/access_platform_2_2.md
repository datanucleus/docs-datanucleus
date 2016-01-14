<head><title>AccessPlatform 2.2</title></head>

#Release Notes for DataNucleus AccessPlatform v2.2

The 2.2 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 2.2_ includes the following over 2.1

<ul>
<li>Many improvements to L2 caching</li>
<li>Various improvements to connection handling for performance</li>
<li>Improved support for persisting containers with null elements</li>
<li>JDO : Support for column position specification</li>
<li>JDO : Support for a typesafe query API</li>
<li>JPA : More complete JPA2 implementation, providing remaining methods</li>
<li>RDBMS : Drop legacy JDOQL implementation</li>
<li>RDBMS : Provide bundled repackaged connection pool (DBCP)</li>
<li>RDBMS : Support for N-1 uni join table relation</li>
<li>Other datastores : Support for cascade delete</li>
<li>Many bug fixes, and minor feature additions.</li>
</ul>



# DataNucleus AccessPlatform 2.2.3

__May 8th 2011__ : _Version 2.2.3_ includes the following changes

<ul>
<li>Fix to use of embedded fields where having a relation to a non-embedded.</li>
<li>Allow property methods (getter/setter) to be final</li>
<li>OSGi : add optional import of log4j</li>
<li>Fix to log messages so we don't call cache.size() since some don't support it</li>
<li>Mark SortedSet/SortedMap wrappers as Serializable</li>
<li>Add check for null literal in JDOQL parser</li>
<li>JPA : Fix to use of @CollectionTable</li>
<li>JPA : Improvements to XML metadata handling</li>
<li>RDBMS : fix to String.matches type handling</li>
<li>Other minor cleanups</li>
</ul>


# DataNucleus AccessPlatform 2.2.2

__Feb 24th 2011__ : _Version 2.2.2_ includes the following changes

<ul>
<li>Add support for associated value mechanism for 1-N maps to reduce the number of SQL statements
    used (been supported for 1-N lists/sets for 2 yrs)</li>
<li>Bug fix to metadata handling for embedded fields, when embedded field definition not provided</li>
<li>JPA : Bug fix to query compilation of JPQL "NOT IN (subquery)"</li>
<li>JPA : Support for @MapKeyEnumerated to define the type of column</li>
<li>JPA : Bug fix to processing of &lt;column&gt; within unique-constraint in XML metadata</li>
<li>JPA : Support for multiple inherited @MappedSuperclass</li>
<li>RDBMS : Bug fix to race condition in statement batching (Gerd Behrmann)</li>
<li>RDBMS : Support for use of "count()" size method when range specified on query</li>
<li>RDBMS : Fix to Derby 10.6 change in handling of boolean/integer comparisons</li>
<li>RDBMS : Bug fix to Postgresql handling of index generation, now omitting the schema name</li>
<li>Other minor cleanups</li>
</ul>


# DataNucleus AccessPlatform 2.2.1

__Jan 17th 2011__ : _Version 2.2.1_ includes the following changes

<ul>
<li>Support for JPQL extension functions "MONTH", "DAY", "YEAR", "HOUR", "MINUTE", "SECOND"</li>
<li>When embedding a persistable field, default to the metadata of the embedded class</li>
<li>JDO : fix to return type for AVG() in JDOQL to match JDO spec change</li>
<li>JPA : Support attribute override for nested embedded members</li>
<li>JPA : Support XML "embedded" tag</li>
<li>RDBMS : Fix to retrieval of version on object in certain circumstances</li>
<li>RDBMS : Fix to Collection.contains check when containing a primitive</li>
<li>RDBMS : Add OSGi importPackage of principal JDBC drivers</li>
<li>RDBMS : Better treatment of unmapped columns with null values</li>
<li>HBase : fix to retrieval when non-persistent fields present</li>
<li>HBase : support "native"(JDO)/"auto"(JPA) value generation strategies</li>
<li>Enhancer : set default API (JDO) when using annotation processor</li>
</ul>


# DataNucleus AccessPlatform 2.2.0.RELEASE

__Dec 10th 2010__ : _Version 2.2 RELEASE_ includes the following changes

<ul>
<li>Fix to threading of transaction manager calls</li>
<li>Fix to threading of startup of services</li>
<li>Fix to not L2 cache fields marked as transactional</li>
<li>Fix to support cascade delete when using "simple" SCO container classes (all datastores except RDBMS)</li>
<li>Fix to detection of inheritance level of application identity object</li>
<li>Minor improvement to class loading for querying</li>
<li>Fix to non-transactional connection retention to clean out connections when closing the PM/EM</li>
<li>Support for bulk update/delete with JDOQL (DataNucleus extension)</li>
<li>Fix to deadlock around enlisting of an object in the transaction when updating a field</li>
<li>Add the ability to define in metadata which classes are pinned in the L2 cache</li>
<li>Several fixes to L2 caching to make use of relation field information</li>
<li>JPA : Support for locking</li>
<li>JPA : Support for fetch groups (DataNucleus extension)</li>
<li>RDBMS : Merge "datanucleus-connectionpool" into RDBMS plugin</li>
<li>RDBMS : Provide bundled repackaged DBCP as fallback connection pool</li>
<li>RDBMS : Support for N-1 uni join table relations</li>
<li>RDBMS : Fix to nontransactional batched inserts so that all statements are flushed</li>
<li>RDBMS : Various minor improvements to JDOQL statement generation</li>
</ul>


# DataNucleus AccessPlatform 2.2.0.M3

__Nov 13th 2010__ : _Version 2.2 Milestone 3_ includes the following changes

<ul>
<li>Fix various SCO container classes with respect to adding a null element.</li>
<li>Set default for "allow-nulls" on SCO containers based on the Java type behaviour</li>
<li>Drop "attachPolicy" and provide complete attachment in default scenario</li>
<li>Providing mechanism for per-object locking</li>
<li>Couple of fixes to result handling in in-memory query evaluator</li>
<li>JDO : Support JDO3.1 PMF.getManagedClasses()</li>
<li>JDO : Support for 
    <a href="http://www.datanucleus.org/products/accessplatform_2_2/jdo/jdoql_typesafe.html">typesafe queries for JDO</a> 
    using a QueryDSL-like fluent API</li>
<li>JDO : More improvements to helpers on NucleusJDOHelper</li>
<li>JPA : Outline implementation of JPA2 lock methods</li>
<li>JPA : Support use of @PrimaryKeyJoinColumn for 1-1s</li>
<li>RDBMS : Allow column reuse for multiple fields of a class</li>
<li>RDBMS : Fix to use of subclass-table with 1-1 bidirectional relations</li>
<li>RDBMS : Fix to use of lengths with BLOB/CLOB on MySQL</li>
<li>RDBMS : Support for querying of (persistent) interfaces</li>
<li>RDBMS : Fixes to handling of "allow-nulls" on arrays with join table</li>
<li>RDBMS : Add support for LONGVARCHAR with HSQLDB 2.0</li>
<li>RDBMS : Add query extension for controlling the join type of variable in JDOQL (1-1 only)</li>
<li>RDBMS : Add support for persisting maps with null values</li>
<li>RDBMS : Fix to JDOQL Collection.contains() on candidate collection when invalid element type</li>
<li>RDBMS : Fix to index/FK creation on Derby to avoid warning messages</li>
</ul>


# DataNucleus AccessPlatform 2.2.0.M2

__Oct 20th 2010__ : _Version 2.2 Milestone 2_ includes the following changes

<ul>
<li>Complete support for JDO3.1 column positioning</li>
<li>Improved merge of metadata information when sequence or cascade info specified in annotations</li>
<li>Ability to retain the datastore connection for non-transactional operations</li>
<li>Fix to a few concurrency bugs around commit/rollback and read/write of objects fields</li>
<li>Ability to specify a separate connection pool for non-transactional connections</li>
<li>JDOQL : Allow use of method invocation in grouping statements</li>
<li>Upgrade to NucleusJDOHelper dirty/loaded methods</li>
<li>Fix clean up of dynamic fetch groups when closing query/extent/pm</li>
<li>Fix to metadata requirement for map with embedded key/value so &lt;embedded&gt; is not needed
    when the key/value is marked as embedded-only</li>
<li>Fix to PMF startup process so that persistence properties are registered before enablement
    of some services</li>
<li>Fix to output from pm.getObjectsById(emptyCollection);</li>
<li>Improve type handling/comparison capabilities of in-memory query evaluator.</li>
<li>Basic support for JDO3.1 sequence allocation size and initial value</li>
<li>getObjectById/find : Ability to not validate objects obtained from L2 cache</li>
<li>RDBMS : change handling of range when not possible in datastore, now handled in the query result
    rather than loading all rows into memory first.</li>
<li>RDBMS : re-enable connection provider plugin point (failover)</li>
<li>RDBMS : several minor changes to types available for IBM DB2</li>
<li>RDBMS : fix to validation of candidate keys, that prevented creation of some unique keys under
    some circumstances</li>
<li>RDBMS : fix to List.get() when used in result clause of JDOQL query</li>
<li>RDBMS : fix to maps of embedded keys/values where key part of value (or vice-versa)</li>
<li>RDBMS : fix to retrieval of existing indices on Oracle for some table names</li>
<li>RDBMS : fix to SQL queries in a J2EE environment</li>
<li>RDBMS : fix to order of creation of tables with SchemaTool</li>
<li>RDBMS : some fixes to use of "allowNulls" on collections/arrays - typo</li>
<li>JPA : fix to case where sequence name not set</li>
<li>JPA : fix to EM.getReference to not validate the object</li>
<li>JPA : fix to use of @Enumerated with @Column</li>
<li>Enhancer : fix to runtime enhancement, class loading problem</li>
<li>Enhancer : fix to error message of override of invalid field</li>
<li>Cache : add option to allow retention of cached objects after close of PMF/EMF, for the case
    where used by other instances</li>
<li>LDAP : Remove dependency to "shared-ldap"</li>
</ul>


# DataNucleus AccessPlatform 2.2.0.M1

__Jul 15th 2010__ : _Version 2.2 Milestone 1_ includes the following changes

<ul>
<li>Add support for more generalised column "position" via metadata - likely in JDO3.1</li>
<li>Add support for 36-character UUID string generator</li>
<li>Improved type safety for queued operations on SCO classes</li>
<li>Drop legacy query expressions for "mapped" datastores - use 2.0 if you still require this</li>
<li>RDBMS : Drop legacy JDOQL implementation - use 2.0 if you still require this</li>
<li>RDBMS : Support for fetching just a FK when the FK is in the candidate query class (avoiding
    adding a join - performance)</li>
<li>RDBMS : Fix for Oracle NLS</li>
<li>RDBMS : Fix to SchemaTool for sequence creation</li>
<li>Fix to EHCache evict() handling</li>
<li>JPA : Criteria Query - Fix to handle fields of superclass</li>
<li>JPA : Criteria Query - Fix to not require candidate alias</li>
<li>Upgrade provided DBCP dependency to latest</li>
</ul>
