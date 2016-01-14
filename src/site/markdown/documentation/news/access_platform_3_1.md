<head><title>AccessPlatform 3.1</title></head>

#Release Notes for DataNucleus AccessPlatform v3.1

The 3.1 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 3.1_ includes the following over 3.0

<ul>
<li>Now aimed at JRE 1.6+ (though many plugins will work with JDK1.5)</li>
<li>Enhancer : works with JDK1.7 too, using ASM v4</li>
<li>javax.time support now present in datanucleus-core</li>
<li>Support for <i>atomic</i> non-transactional updates (use of field setters, or SCO mutating methods)</li>
<li>Support for monitoring API providing statistics about DataNucleus calls to the datastore etc, and
    merged "datanucleus-management" plugin into this monitoring API</li>
<li>Cache : javax.cache support now present in datanucleus-core</li>
<li>Cache : JCache support now present in datanucleus-cache</li>
<li>JPA 2.1 <a href="http://www.datanucleus.org/products/accessplatform_3_1/jpa/stored_procedures.html">Stored Procedure API</a> supported for RDBMS</li>
<li>JPA 2.1 <a href="http://www.datanucleus.org/products/accessplatform_3_1/jpa/types.html#typeconverter">Type Converter API</a> supported for RDBMS, Excel, 
    ODF, HBase, MongoDB and JSON datastores</li>
<li>JPA : Fully working JTA integration</li>
<li>JPA : Support for specifying named query annotations on non-Entity classes (vendor extension)</li>
<li>JDO : Support for specifying named query annotations on non-PersistenceCapable classes (vendor extension)</li>
<li>JDO : Complete support for non-durable identity with RDBMS, Excel, ODF, MongoDB, HBase</li>
<li>REST : Much improved handling, also allowing full (JDOQL or JPQL) querying now</li>
<li>REST : Support for bulk delete</li>
<li>REST : Support for datastore identity</li>
<li>SchemaTool : support for delete+create mode of operation</li>
<li>HBase : support for multitenancy</li>
<li>HBase : support JDO/JPA table/column naming strategies</li>
<li>MongoDB : support JDO/JPA table/column naming strategies</li>
<li>MongoDB : support for embedded objects with inheritance</li>
<li>MongoDB : add support to in-datastore querying for COUNT, as well as parameters</li>
<li>ODF : support JDO/JPA table/column naming strategies</li>
<li>Excel : support JDO/JPA table/column naming strategies</li>
<li>RDBMS : "xmltypeoracle" plugin merged into RDBMS plugin</li>
<li>Many bug fixes, and minor feature additions.</li>
</ul>



# DataNucleus AccessPlatform 3.1.5

__May 23rd 2013__ : _Version 3.1.5_ includes the following changes

<ul>
<li>JDO : Fix to Localiser creation to avoid problem under OSGi</li>
<li>RDBMS : Fix to SQL query execution to avoid connection close problem</li>
<li>RDBMS : Fix to pessimistic locking for SQLServer</li>
</ul>


# DataNucleus AccessPlatform 3.1.4

__Jan 22nd 2013__ : _Version 3.1.4_ includes the following changes

<ul>
<li>Fix to ordering problem with class loaders</li>
<li>Fix to persist of N side of 1-N bidir with detached owner so we don't get persist of 2 elements</li>
<li>JPA : improvements to checks for JTA transactions when used in JavaEE</li>
<li>Minor improvements to location of persistence-unit and detection of duplicate named units</li>
<li>RDBMS : Fix to SQLServer usage with bulk delete query statement</li>
<li>RDBMS : Fix to JDOQL compilation with parameters in range clause</li>
</ul>


# DataNucleus AccessPlatform 3.1.3

__Nov 12th 2012__ : _Version 3.1.3_ includes the following changes

<ul>
<li>JPA : Fix missing space after filter in criteria query filter/having clauses</li>
<li>JPA : Support Criteria parameter() method without name.</li>
<li>Fix to JTA transaction manager locator constructors</li>
<li>Add support for L2 caching of embedded/serialised fields (disabled by default)</li>
<li>Change process for update of an object in L2 cache to avoid concurrent access</li>
<li>LDAP : Fix to concurrent modification exception</li>
<li>MongoDB : update "native"/"auto" value generator to use "increment" when using numeric PK</li>
<li>HBase : make use of Table pool (Simon Kelly)</li>
<li>RDBMS : Clean up DeleteRequest code</li>
<li>RDBMS : Support for specifying indexes/unique-keys on map join tables</li>
<li>Updates to all plugins to place upper limit on Maven dependency versions (pre-3.2 releases)</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.1.2

__Sep 27th 2012__ : _Version 3.1.2_ includes the following changes

<ul>
<li>Fix to lookup of object inheritance level in some corner-case situations</li>
<li>Provide TypeConverters for persisting Serializable object as byte[] or base-64 encoded string</li>
<li>Fix clone of JPQL query so that "from" is cloned</li>
<li>Log which fields (numbers) are being attached</li>
<li>Complete TODO in FetchPlan code for dynamic fetch groups from PM</li>
<li>JDO : Fix bug in map key/value metadata handling introduced in 3.1.1</li>
<li>JPA : Fix bug in use of Query.getParameters when used by Spring Data JPA</li>
<li>XML : Fix to class loading in relation lookup</li>
<li>Neo4j : Fix to some JPQL queries causing exception</li>
<li>Neo4j : Fix to lazy load iterator for empty result condition</li>
<li>Neo4j : Fix to stackoverflow with bidirectional relation retrieval</li>
<li>Neo4j : Support persistence of arrays</li>
<li>Neo4j : Support persistence of serialised fields</li>
<li>Neo4j : Support "increment" value generator</li>
<li>MongoDB : Support for capped DB collections (size limit on objects of a type)</li>
<li>MongoDB : Fix to replica-set URL string parsing</li>
<li>RDBMS : Extend support for stored procedure parameters to other types</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.1.1

__Aug 29th 2012__ : _Version 3.1.1_ includes the following changes

<ul>
<li>Add hook for transaction event listeners</li>
<li>Improvements to metadata loading process to exceptions thrown and access to class/field that is
    causing the problem (allowing IDE tools to highlight the problem).</li>
<li>Support for datastores that use simple SCO wrappers for some fields and backed SCO wrappers for others</li>
<li>Major improvements to in-memory query evaluation : SUM, result class handling, creator expressions, 
    JPQL "case", JPQL "type", support for Math functions, fix to some Date methods, support for methods on arrays.</li>
<li>Fix to reuse of queries (e.g when using COUNT to get size of original query result) to respect "subclasses" flag</li>
<li>Fix to pm.getObjectsById to cater for inheritance level</li>
<li>JDO : more flexibility on specification of embedded fields</li>
<li>JPA : vendor extension annotation for specifying indexes</li>
<li>JPA : fix to some obscure IdentifiableType method</li>
<li>RDBMS : more flexibility on query method invocation to allow them to be usable on subclasses
    of the invoked type</li>
<li>RDBMS : more flexibility on storage of Time fields</li>
<li>RDBMS : use plugin manager to handle method/operator invocations</li>
<li>Neo4j : first major release with Neo4j support</li>
<li>Neo4j : support lazy loading on results from queries</li>
<li>Neo4j : better handling of polymorphic queries excluding subclasses</li>
<li>MongoDB : support lazy loading on results from queries</li>
<li>MongoDB : support use of embedded fields in queries</li>
<li>MongoDB : support use of Enum as query parameter</li>
<li>Spatial : support Java-style method invocation in queries of spatial methods (for the majority of
    methods at least).</li>
<li>AWTGeom : support for Rectangle.contains with in-memory query evaluation</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.1.0.RELEASE

__Jul 24th 2012__ : _Version 3.1 RELEASE_ includes the following changes

<ul>
<li>In-memory query evaluation support for comparative operations on all Comparable types</li>
<li>In-memory query evaluation support for various array methods</li>
<li>In-memory query evaluation support for various expression constructs involving DyadicExpression
    and many others</li>
<li>In-memory query evaluation support for JodaTime methods</li>
<li>In-memory query evaluation support for Point/Rectangle methods</li>
<li>Fix to <i>uuid-string</i> value generator to use correct charset</li>
<li>Some fixes to Data Federation in the allocation of secondary datastores</li>
<li>Added type converters for java.sql.* types to String/Long</li>
<li>Support for Bitronix transaction manager</li>
<li>RDBMS : cater for sql-type being in wrong case</li>
<li>RDBMS : Fix to H2 to create index before foreign-key to avoid validation problem</li>
<li>Enhancer : fix to only add stackmap frames when the JDK is 1.7 or above (so javap will work).</li>
<li>ODF : Fix to persistence of Enum type, and support for java.sql.* types</li>
<li>MongoDB : Many improvements to supported types able to be persisted/queried</li>
<li>MongoDB : Fixes to use of datastore-identity, and use of NATIVE value generation strategy</li>
<li>MongoDB : Fix to not persist a field when persistence-modifier is inappropriate</li>
<li>MongoDB : Add support for evaluating a query in-memory</li>
<li>MongoDB : Support use of "owner field" on embedded relations</li>
<li>MongoDB : Support persistence of Collection of non-PC elements where the element type would not
    be supported natively in MongoDB</li>
<li>MongoDB : Support for "$and" in queries (required MongoDB 1.9.1 or later)</li>
</ul>


# DataNucleus AccessPlatform 3.1.0.M5

__Jul 8th 2012__ : _Version 3.1 Milestone 5_ includes the following changes

<ul>
<li>Drop enhancer extension point since we only provide a single enhancer implementation now</li>
<li>Make generic query compilation serializable for better portability</li>
<li>Fix couple of NPEs, in statistics handling for JMX and operation with no L1 cache</li>
<li>Improvement to processing of annotations to only process fields if the class is @PersistenceCapable</li>
<li>JPA : Support for @NamedQuery specified on non-Entity classes</li>
<li>JPA : Fix to EntityManager.joinTransaction to correctly join to the current JTA transaction (and throw exception
    if not active)</li>
<li>JPA : Support override of embedded collection element column names.</li>
<li>JPA : Fix to handling of query when JTA transaction active</li>
<li>JDO : Support for @Query specified on non-persistable classes</li>
<li>JDO : Improvement for typesafe query returning a single aggregate</li>
<li>RDBMS : update to schema lock process for when schema is being updated (doesn't cater for 100% of cases yet)</li>
<li>RDBMS : fix to JDOQL/JPQL handling of "=="/"!=" with a parameter where the parameter is a non-persistable
    type and is mapped to more than 1 column</li>
<li>RDBMS : add handling for case where a field has "jdbc-type" and "sql-type" to fallback to the
    "jdbc-type" if the "sql-type" is not explicitly supported.</li>
<li>Jodatime : support for use of Interval start/end in JDOQL (Jasper Siepkes)</li>
<li>Jodatime : cater for null Jodatime type literals in queries</li>
<li>AWTGeom : support for use of Point and Rectangle in queries</li>
<li>Spatial : support for some methods in JDOQL</li>
<li>Various minor bug fixes and improvements</li>
</ul>


# DataNucleus AccessPlatform 3.1.0.M4

__Jun 17th 2012__ : _Version 3.1 Milestone 4_ includes the following changes

<ul>
<li>Enhancer upgraded to use ASM v4, and to support JDK1.7</li>
<li>Add support for embedded objects with container fields</li>
<li>Fix bug in use of type converters for javax.time types</li>
<li>SchemaTool : add "delete+create" mode of operation</li>
<li>Fix to metadata startup processing (Chris Coleman)</li>
<li>Fix so that objects created with "identity" value strategy can be L2 cached</li>
<li>Fix to managed relations for 1-1 bidir field</li>
<li>JDO : Fix to support for discriminator of @Embedded mappings (inherited embedded objects)</li>
<li>JDO : Add convenience accessor for PMF properties</li>
<li>JDO : Add convenience method to create PMF for a persistence-unit metadata object</li>
<li>JPA : Fix couple of NPEs (criteria FromImpl, and EMF with null overriding props)</li>
<li>JPA : Fix to creation of listeners for annotations</li>
<li>RDBMS : upgraded to support JDK1.7 (JDBC4.1), and require JDK1.6 minimum</li>
<li>RDBMS : Fix to JDOQL "instanceof" handling for some corner cases</li>
<li>RDBMS : Fix to JDOQL/JPQL bulk update for some inheritance cases</li>
<li>RDBMS : Treat JPQL "FETCH JOIN" to mean add to fetch group</li>
<li>RDBMS : Support SchemaTool "delete+create" mode</li>
<li>RDBMS : Support persisting String to BIGINT column type</li>
<li>RDBMS : Fix to JDOQL using "contains" on collection using FK</li>
<li>LDAP : Cleanup of logging to use NATIVE category when communicating with datastore</li>
<li>MongoDB : support for query range (Chris Rued)</li>
<li>MongoDB : support for java.util.Date in queries (Chris Rued)</li>
<li>MongoDB : improvement to processing of "count()" in query (Chris Rued)</li>
<li>JodaTime : fix to some null handling cases</li>
<li>Various minor bug fixes and improvements</li>
</ul>


# DataNucleus AccessPlatform 3.1.0.M3

__May 10th 2012__ : _Version 3.1 Milestone 3_ includes the following changes

<ul>
<li>Support for nontransactional atomic updates</li>
<li>Fix to use of JMX so that the implementation can be selected, and also for OSGi usage</li>
<li>Improvement to findObject process to shortcut search of subclasses</li>
<li>Rewrite "native"/"auto" value generator strategy to support "identity"/"sequence"/"increment"/"uuidhex" strategies</li>
<li>Clean-up ObjectProvider/ExecutionContext APIs for simpler store plugins</li>
<li>Fix to "simple" SCO container wrappers (non-RDBMS datastores) for cascade-delete and managed relations</li>
<li>Fix bug with syncing of DateFormat in handling of date/calendar fields persisted as String</li>
<li>Fix bug with non-detach of N-1 join table relation</li>
<li>Support persisting javax.time LocalTime as numeric</li>
<li>JPA : set default for nontransactional operations as atomic=false to match JPA spec</li>
<li>REST : rewrite to support query operations, and to support full JDOQL queries</li>
<li>REST : support for datastore identity</li>
<li>RDBMS : full support for nondurable identity</li>
<li>ODF : full support for nondurable identity</li>
<li>Excel : full support for nondurable identity</li>
<li>HBase : full support for nondurable identity</li>
<li>HBase : fix bug in handling of literal in comparison</li>
<li>MongoDB : full support for nondurable identity</li>
<li>Various minor bug fixes and improvements</li>
</ul>


# DataNucleus AccessPlatform 3.1.0.M2

__Apr 6th 2012__ : _Version 3.1 Milestone 2_ includes the following changes

<ul>
<li>Merge "store.rdbms.xmltypeoracle" plugin into DataNucleus "store.rdbms" jar</li>
<li>Merge "management" plugin into DataNucleus "core" jar</li>
<li>Add Statistics API for persistence, adding on number of reads/writes etc to what JMX already provided.
    Supported by RDBMS, MongoDB, HBase, Excel, ODF, JSON, LDAP, NeoDatis plugins</li>
<li>Change Set proxy to not do clear+addAll on an update</li>
<li>Fix bug in removeAll() method of Set proxies</li>
<li>Fix to persist of 1-N uni FK Lists to not to update the FK even though already set (less SQL calls)</li>
<li>Fix to delete of N side of a 1-N bidir catering for relation not loaded</li>
<li>JPA : fix to javax.persistence.XXXDataSource persistence properties</li>
<li>Cache : move support for latest version of javax.cache into "core". Old version of javax.cache is
    now in the "cache" plugin as "jcache".</li>
<li>Provide helper method to do ordering of candidates based on a JPA style ordering clause, usable
    by all non-RDBMS store plugins</li>
<li>Remove old ObjectXXXConverter code now that we are using TypeConverter API</li>
<li>RDBMS : Fix to Oracle Range handling to cater for related class with same named fields</li>
<li>RDBMS : Support for NCHAR/NVARCHAR jdbc types (MSSQL)</li>
<li>RDBMS : Support inheritance check on input identity for abstract base class where we have 
    multiple possible subclasses</li>
<li>MongoDB : support for using query input parameters in the datastore evaluation (Chris Rued)</li>
<li>MongoDB : support for query COUNT in the datastore (Chris Rued)</li>
<li>MongoDB : Fix to version field update process</li>
<li>MongoDB : Support for enum persisted as numeric</li>
<li>MongoDB : Support for inherited embedded objects</li>
<li>MongoDB : Support for inheritance determination using pm.getObjectById/em.find</li>
<li>Excel : Support for enum persisted as numeric</li>
<li>Excel : Fix to version field update process</li>
<li>ODF : Support for enum persisted as numeric</li>
<li>ODF : Fix to version field update process</li>
<li>HBase : Support for enum persisted as numeric</li>
<li>HBase : Fix to version field update process</li>
<li>JSON : Fix to version field update process</li>
<li>Various minor bug fixes and improvements</li>
</ul>


# DataNucleus AccessPlatform 3.1.0.M1

__Mar 10th 20121__ : _Version 3.1 Milestone 1_ includes the following changes

<ul>
<li>Merge javax.time type support into DataNucleus "core" jar</li>
<li>Support bulk-loading of objects from datastore with PM.getObjectsById()</li>
<li>Support general type-converter API to replace ObjectXXXConverter</li>
<li>Fix to PM.getObjectsById when no L2 cache configured</li>
<li>JPA2.1 : Support for AttributeConverter interface and @Convert annotation</li>
<li>RDBMS : Support type converter API</li>
<li>MongoDB : Support type converter API</li>
<li>MongoDB : Support naming factory to follow JDO/JPA schema naming conventions</li>
<li>Excel : Support type converter API</li>
<li>Excel : Support naming factory to follow JDO/JPA schema naming conventions</li>
<li>ODF : Support type converter API</li>
<li>ODF : Support naming factory to follow JDO/JPA schema naming conventions</li>
<li>JSON : Support type converter API</li>
<li>JSON : Support naming factory to follow JDO/JPA schema naming conventions</li>
<li>HBase : Support type converter API</li>
<li>HBase : Support multitenancy via discriminator</li>
<li>AWTGeom : Migrate to use type converter API</li>
<li>JodaTime : Migrate to use type converter API</li>
<li>Various minor bug fixes and improvements</li>
</ul>
