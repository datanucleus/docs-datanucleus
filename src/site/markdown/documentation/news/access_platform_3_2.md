<head><title>AccessPlatform 3.2</title></head>

#Release Notes for DataNucleus AccessPlatform v3.2

The 3.2 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 3.2_ includes the following over 3.1

<ul>
<li>The enhancer and ASM are now merged into <i>datanucleus-core</i></li>
<li>L2 caching of embedded/serialised fields now defaults to ON</li>
<li>ExecutionContext objects are now pooled, together with various other improvements for performance</li>
<li>Enhancer now includes an option to enhance classes as <i>detachable</i> regardless of metadata</li>
<li>Neo4j : now uses a single connection per PM/EM</li>
<li>Neo4j : now supports bulk delete</li>
<li>MongoDB : now uses a single connection per PM/EM</li>
<li>MongoDB : now supports bulk delete</li>
<li>HBase : supports various extensions for bloom filters, compression, in-memory etc (Nicolas Seyvet)</li>
<li>HBase : now supports bulk delete</li>
<li>RDBMS : support added for the Virtuoso database (Emmanuel Poitier)</li>
<li>RDBMS : support added for Tomcat connection pool (Marshall Reeske)</li>
<li>OSGi : improved deployability due to dependency version restrictions</li>
<li>JPA : validated to work with JBoss 7 (thanks to Nicolas Seyvet and Scott Marlow)</li>
<li>JPA : access of non-detached field will result in IllegalAccessException instead of the previous JDO exception</li>
<li>JPA : support for JPA2.1 FROM "ON" clauses</li>
<li>JPA : support for bulk usage of persist(), remove(), merge() and detach() (pass in Collection or array of entities)</li>
<li>JPA : support for JPA2.1 "Generate Schema" feature</li>
<li>If a type is supported to be persistent then it defaults to persistent now (no need to mark all non-standard typed fields as persistent).</li>
<li>Add ability to disable the L2 cache on a PM/EM-basis where the PMF/EMF has it enabled.</li>
<li>Cache : provides support for <i>javax.cache</i> v0.61</li>
<li>Many bug fixes, and minor feature additions.</li>
</ul>



# DataNucleus AccessPlatform 3.2.9

__Dec 10th 2013__ : _Version 3.2.9_ includes the following changes

<ul>
<li>Wrap any exception thrown from JDOHelper.getObjectId so that it meets the JDO spec</li>
<li>Fix to class loading for property validators for OSGi</li>
<li>Couple of fixes for optimistic relationship management</li>
<li>JDO : Change PMF to be Serializable</li>
<li>RDBMS : Add support for bulk fetch of multi-valued collection fields of a candidate when in FetchPlan of a query (removes "1+N" problem)</li>
<li>RDBMS : Add support for SQLServer to handle JDOQL String.substring with 2 args (Daniel Dai)</li>
<li>RDBMS : Add support for JDOQL String.concat (Daniel Dai)</li>
<li>RDBMS : Fix to detection of type of backing store required for a collection, using metadata more</li>
<li>MongoDB : Add support for specifying the MongoOptions when creating the first connection (Robin Zhang)</li>
<li>Spatial : Fix some missing PostGIS methods</li>
<li>Some other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.8

__Nov 19th 2013__ : _Version 3.2.8_ includes the following changes

<ul>
<li>Metadata : Add level of locking to metadata load process to assist in multithreaded environments</li>
<li>Metadata : fix bug in OrderMetadata for multithreaded environments</li>
<li>Fix to some potential startup problems with ExecutionContext/ObjectProvider in multithreaded environments</li>
<li>Change "datanucleus.SerializeRead", "datanucleus.cache.collections", "datanucleus.deletionPolicy", 
    "datanucleus.query.jdoql.allowAll", "datanucleus.query.sql.allowAll" to be overrideable on the PM/EM</li>
<li>Cache : update javax.cache support to "1.0-PFD" standard</li>
<li>RDBMS : Fix to persistence of bidirectional 1-N with Set&lt;interface&gt;</li>
<li>RDBMS : Change backing stores to be one per field and be thread-safe</li>
<li>RDBMS : Support for more boolean expressions in result clause for JDOQL/JPQL</li>
<li>RDBMS : Support for persisting a field serialised into a local file</li>
<li>RDBMS : Support for persisting a File type field streamed to/from datastore</li>
<li>RDBMS : Upgrade "datasource" plugin point to be "connectionpool", adding more capabilities</li>
<li>Neo4j : support for persistence of map fields (Map&lt;PC,NonPC&gt;, Map&lt;NonPC, PC&gt;)</li>
<li>Neo4j : support for using embedded database with user-provided configuration properties</li>
<li>Neo4j : support for access to underlying Cypher query for a JDOQL/JPQL query</li>
<li>MongoDB : support for query evaluation of several String methods in-datastore (Marcin Jurkowski)</li>
<li>MongoDB : support for query evaluation of Collection.contains in-datastore (Marcin Jurkowski)</li>
<li>MongoDB : fix to retrieval of class version field (Marcin Jurkowski)</li>
<li>MongoDB : support for query literals of type Character</li>
<li>Some other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.7

__Oct 23rd 2013__ : _Version 3.2.7_ includes the following changes

<ul>
<li>JPA : fix to metamodel SimpleAttributeImpl.isVersion (Adrian Ber)</li>
<li>JPA : add support for multi-field join syntax in JPQL FROM clause</li>
<li>JPA : update to handling of JPQL range when just first result set</li>
<li>RDBMS : fix for SQLServer schema name problem (Shanyu Zhao)</li>
<li>RDBMS : add support for using FetchPlan when querying over "complete-table" candidate (previous just retrieved primary key)</li>
<li>RDBMS : improvement in process to determine class name when no subclasses known about, to avoid SQL</li>
<li>RDBMS : support for persisting Double type into SQLServer FLOAT datastore type (Shuaishai Nie)</li>
<li>JSON : fix to retrieval of objects in query so that application-identity cases have id assigned</li>
<li>MongoDB : add support for query ordering being processed in the datastore (Marcin Jurkowski))</li>
<li>Rename "google-collections" plugin to "guava"</li>
<li>JDO : distribute jdo-api 3.1-rc1</li>
<li>Some other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.6

__Aug 31st 2013__ : _Version 3.2.6_ includes the following changes

<ul>
<li>L2 Cache : store class name of "id" of object to avoid some inheritance lookups</li>
<li>L2 Cache : allow configurable "update" mode</li>
<li>L2 Cache : cache copies of Date, Calendar when caching fields of those types</li>
<li>Update javax.cache support to v0.9</li>
<li>Add fallback method for getting types of a TypeConverter</li>
<li>Improvement to lookup of an object using class name from the identity where possible</li>
<li>Key FetchPlan for a class by the class name rather than by its metadata</li>
<li>JPA : fix support for Criteria function() method</li>
<li>RDBMS : support for querying ==/!= of String parameters</li>
<li>RDBMS : support query select of fetch plan fields of related N-1 FK field</li>
<li>RDBMS : support detection of discriminator in SQL query</li>
<li>HBase : improvement for primitive wrapper field types</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.5

__Aug 1st 2013__ : _Version 3.2.5_ includes the following changes

<ul>
<li>Provide different ObjectProvider (StateManager) when using non-RDBMS datastores</li>
<li>Improve process of defining static query method support</li>
<li>In-memory querying : add support for String.charAt(int)</li>
<li>Upgrade javax.cache support to v0.8</li>
<li>MetaData : fix to merging of unmapped columns from ORM mapping file</li>
<li>RDBMS : add support for ordering with NULLS FIRST/NULLS LAST in JDOQL/JPQL</li>
<li>RDBMS : add support for use of startup load-scripts etc</li>
<li>RDBMS : fix to entrySet for FK Map where the key/value have inheritance</li>
<li>RDBMS : fix to handling of auto-apply of TypeConverter</li>
<li>MongoDB : fix to handling of version field under some circumstances</li>
<li>Spatial : various additions for use with PostGIS (Baris Ergun)</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.4

__Jun 27th 2013__ : _Version 3.2.4_ includes the following changes

<ul>
<li>Drop support for DataNucleus extension @FetchGroup/@FetchPlan</li>
<li>Fix to attach process for SCO collections under some circumstances</li>
<li>Fix to L2 cache to not perform lookup if identity is for class that is not cacheable</li>
<li>Schema Generation : fix to case where using complete-table and version/discriminator not being added
    to subclasses</li>
<li>Fix to query caching to cater for FetchPlan being different on a query</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.3

__Jun 9th 2013__ : _Version 3.2.3_ includes the following changes

<ul>
<li>Mapping : cater for inheritance with (multiple) MappedSuperclass part way down tree but with 
    superclass Entity with own table (i.e effectively @MappedSubclass)</li>
<li>SchemaTool : support properties file and/or System props overriding persistence.xml</li>
<li>Simplify internal metadata storage for fetch groups and constraints</li>
<li>Rename "datanucleus.metadata.validate" persistence property to "datanucleus.metadata.xml.validate"</li>
<li>Add "datanucleus.metadata.xml.namespaceAware" to allow control over use of XML namespaces</li>
<li>Fix to operation queue for Map remove operations</li>
<li>Add check on specification of discriminator value for abstract classes</li>
<li>JPA : Support more &lt;order-column&gt; situations</li>
<li>RDBMS : Schema Generation improvement to better cater for any ordering of input classes</li>
<li>RDBMS : Schema Generation fix to recursive initialisation of PK of a table</li>
<li>RDBMS : Fix to handling of FK Map where key/value have inheritance and the value/key is stored
    in a superclass</li>
<li>RDBMS : Fix to value-map discriminator handling for embedded object</li>
<li>RDBMS : add ability to invoke any SQL function (for JPA 2.1)</li>
<li>MongoDB : fix to explicitly specify the storage type for primitive wrapper types</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.2

__May 14th 2013__ : _Version 3.2.2_ includes the following changes

<ul>
<li>JPA : support for JPA2.1 EM.isJoinedToTransaction</li>
<li>JPA : support for JPA2.1 EMF.addNamedQuery</li>
<li>JDOQL : support more usages of DyadicExpression</li>
<li>Make operation queue more flexible so can contain any type of operation</li>
<li>Fix bug in operation queue optimisation</li>
<li>Add support for L2 cache storeMode/retrieveMode</li>
<li>Fix to bug with embedded 1-1 with no "embedded" block of mappings</li>
<li>Add support for specifying the ObjectProvider class name</li>
<li>Add optimisation to operation queue to detect Map put+remove of same key in succession</li>
<li>Fix JDOStateManager to throw API-specific exception rather than JDOException</li>
<li>RDBMS : fix to JDOQL getHour, getMinute, getSecond for SQLServer (Ivan Badia)</li>
<li>RDBMS : support evaluation of "(dyadicExpr).method()"</li>
<li>RDBMS : Fix to Map preDelete to better handle situation where a value was removed from the map before deletion</li>
<li>Spatial : fix to concurrency issue (Jan Heuer)</li>
<li>Move to release via Sonatype</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.1

__Apr 5th 2013__ : _Version 3.2.1_ includes the following changes

<ul>
<li>Enhancer : important fix to detection of JDK1.6/1.7 so we add stackmap frames correctly</li>
<li>Fix to attach of elements of collection that aren't yet persistent</li>
<li>Fix to attach process of marking of when an object is dirty</li>
<li>Fix to cascade-delete of embedded field</li>
<li>JDOQL : Support Date.getDate()</li>
<li>Add cached lookup mechanism for discriminator when using value-map</li>
<li>Default "datanucleus.attachSameDatastore" to true to match main use-cases</li>
<li>Move control over which FlushProcess to use to the datastore plugin (so they can optimise it)</li>
<li>JDO : support update of PM transaction properties through PM.setProperty</li>
<li>JDO : support validation of property values passed to PM.setProperty</li>
<li>JDO : return from PM.getProperties/getSupportedProperties uses correct case for names</li>
<li>JPA : fix to metamodel for whether a class was marked as MappedSuperclass or Entity</li>
<li>RDBMS : Change default for PreparedStatement pooling to false since DBCP is buggy</li>
<li>RDBMS : Fix to PostgreSQL bulk update syntax usage</li>
<li>RDBMS : Cater for ResultSet that returns column names with different case to the SQL statement</li>
<li>RDBMS : Set default for schema for sequence/sequence-table as that of the store manager</li>
<li>RDBMS : Fix bug in SQLAlphaTableNamer for case sensitivity</li>
<li>RDBMS : Support IDENTITY columns for VirtuosoDB (Emmanuel Poitier))</li>
<li>Neo4j : support embedded objects with reference to non-embedded objects</li>
<li>MongoDB : support embedded objects with reference to non-embedded objects</li>
<li>MongoDB : only apply a query to instantiable candidates</li>
<li>MongoDB : upgrade to mongo-java-driver v2.9+</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.0.RELEASE

__Mar 11th 2013__ : _Version 3.2 RELEASE_ includes the following changes

<ul>
<li>Fix to in-memory evaluation when using a variable that has no possible value</li>
<li>Move operation queue for SCOs to ExecutionContext so that it can control the whole flush process</li>
<li>Disable ObjectProvider pooling since it currently causes issues when in a highly multithreaded environment</li>
<li>Add check on attempted persistence of <i>final</i> fields</li>
<li>JPA : allow for user overriding a JNDI datasource with a URL-based datasource</li>
<li>RDBMS : fix to bulk update when setting fields to NULL</li>
<li>RDBMS : Cater for fields of a type that have a TypeConverter but no Mapping defined, falling
    back to the TypeConverter</li>
<li>Neo4j : Support for bulk delete</li>
<li>MongoDB : Support for bulk delete</li>
<li>HBase : Support for bulk delete</li>
</ul>


# DataNucleus AccessPlatform 3.2.0.M4

__Feb 20th 2013__ : _Version 3.2 Milestone 4_ includes the following changes

<ul>
<li>Upgrade support for javax.cache to v0.61</li>
<li>Add support for javax.cache "readThrough", "writeThrough", "statisticsEnabled" and "storeByValue"</li>
<li>Fix bug where user had JPA inheritance tree with MappedSuperclass part way through tree
    and no discriminator value specified.</li>
<li>JDO : Fix to JDO PM.getProperties to present the properties in the case they are in the JDO spec.</li>
<li>Support disabling of L2 cache on a PM basis</li>
<li>Add synchronisation to evict method on query results cache</li>
<li>Much code refactoring around the enhancer and restricting JDO classes to just two places specific
    to the bytecode enhancement contract.</li>
<li>JPA : Support for JPA2.1 XSD (Proposed Final Draft (PFD))</li>
<li>JPA : Update support for "generate-schema" to match JPA2.1 PFD</li>
<li>JPA : Fix bug in XML &lt;collection-table name=...&gt; processing</li>
<li>JPA : Add missing support for @MapKeyTemporal and associated XML variant.</li>
<li>JPA : Cater for missing @OneToOne on persistable field</li>
<li>JDO : Fix initialisation of a Localiser that caused problems in OSGi</li>
<li>RDBMS : Fix to NPE in UpdateRequest/DeleteRequest for corner-case version handling</li>
<li>RDBMS : Fix to not setting version when class was read in and has no DFG fields</li>
<li>RDBMS : Fix to bulk update for SQLServer</li>
<li>RDBMS : Support for Tomcat connection pool (Marshall Reeske)</li>
<li>RDBMS : Better control over how statements are logged</li>
<li>RDBMS : Fix bug in HAVING clause application</li>
<li>RDBMS : Omit class from discriminator restriction when class is abstract</li>
<li>Various minor bug fixes and improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.0.M3

__Feb 1st 2013__ : _Version 3.2 Milestone 3_ includes the following changes

<ul>
<li>Introduction of a 2-phase flush process for corner cases that discover extra objects to be persisted
    during the first phase of flush</li>
<li>Support for JTA TransactionSynchronizationRegistry</li>
<li>Support for JTA transactions without auto-join</li>
<li>Fixes to JTA support for JBoss 7 (Nicolas Seyvet)</li>
<li>Fix to JDOQL bulk update bug</li>
<li>Various fixes to integration of Bean Validation</li>
<li>Support ability to precompile all named queries during PMF/EMF creation</li>
<li>Improvements to L2 cache update process to only update particular fields</li>
<li>Fix to XML auto-start mechanism to avoid duplicate entries</li>
<li>JPA2.1 : support for FROM "ON" clause</li>
<li>JPA : Support for multi-object usage of EntityManager persist(), merge(), remove() and detach() - vendor extension</li>
<li>JDO : Move JDO Typesafe classes to "datanucleus-api-jdo" plugin</li>
<li>RDBMS : Fix to getGeneratedKeys for MySQL (10-15% speed up for some cases)</li>
<li>RDBMS : Fix to pessimistic locking for SQLServer (Vladimir Konkov)</li>
<li>RDBMS : Improvements to bulk update to cope with inheritance and multiple tables</li>
<li>RDBMS : Improvements to bulk delete to cope with inheritance and multiple tables</li>
<li>RDBMS : Fix to query compilation caching to allow for serialize-read setting (Graham Stewart)</li>
<li>RDBMS : Support for Virtuoso database (Emmanuel Poitier)</li>
<li>RDBMS : Bug fix so that any HAVING clause is applied to all UNIONs</li>
<li>RDBMS : Change DB2 to use UNION ALL instead of UNION</li>
<li>HBase : fix to use of HTable (Nicolas Seyvet)</li>
<li>HBase : fix to extensions handling (Nicolas Seyvet)</li>
<li>Excel : allow connectionURL prefix of "xls" as alias for "excel"</li>
<li>MongoDB : fix to logger argument to be String</li>
<li>Various minor bug fixes and improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.0.M2

__Jan 1st 2013__ : _Version 3.2 Milestone 2_ includes the following changes

<ul>
<li>JDO : ability to mark all classes as detachable, overriding metadata</li>
<li>JDO : add convenience accessor for "detachedState" of an object</li>
<li>JDO : provide access to the native query performed by JDOQL</li>
<li>JPA : add convenience accessor for "detachedState" of an object</li>
<li>JPA : provide access to the native query performed by JPQL</li>
<li>JPA : support surrogate version on a class</li>
<li>JPA : fix to exception throwing when using JTA in a JavaEE environment</li>
<li>JPA : support for JPA2.1 "Generate Schema" feature</li>
<li>JPA : improved logix for finding a persistence-unit with a name, and flag duplicate units with the same name</li>
<li>JPA : default to not add classTransformer in JavaEE environment (so user has to enable it)</li>
<li>Update to JMX beans definitions for compliance</li>
<li>Bundle (repackaged) ASM into <i>datanucleus-core</i> for cleaner usage</li>
<li>Fix missing "PreMainClass" for enhancer so runtime enhancement works</li>
<li>Moved "mapped datastores" code into RDBMS plugin (from datanucleus-core) since only used there</li>
<li>Add pooling for ExecutionContext and ObjectProvider objects for performance.</li>
<li>Fix to persist of N-1 relation with detached owner so we don't get multiple element objects</li>
<li>Fix to ClassLoaderImpl/MetaDataUtils to preserve ordering whilst removing dups</li>
<li>RDBMS : fix to use of named parameters in range clause of query</li>
<li>RDBMS : add statement batching to shifting process for elements in a List</li>
<li>RDBMS : fix to schema generation when we have "subclass-table" part way down an inheritance tree</li>
<li>MongoDB : improvement for polymorphic queries to make use of discriminator column and handle
    all in single query</li>
<li>MongoDB : improvement to deletion process to not reload same fields multiple times</li>
<li>HBase : support for Bloom filters, in-memory and various other options (Nicolas Seyvet)</li>
<li>Excel : make "poi-ooxml" dependency optional since not needed with XLS</li>
<li>Various minor bug fixes and improvements</li>
</ul>


# DataNucleus AccessPlatform 3.2.0.M1

__Nov 24th 2012__ : _Version 3.2 Milestone 1_ includes the following changes

<ul>
<li>OSGi : add version restrictions on many ImportPackage specifications to allow much improved
    deployability out-of-the-box.</li>
<li>Merge bytecode enhancer into <i>datanucleus-core</i></li>
<li>Add option to enhance all classes in a directory and below</li>
<li>Clean up connection management so that when using Data Federation pooling is based on the
    ExecutionContext+Datastore and otherwise for the ExecutionContext</li>
<li>Attach/Detach : add logging of fields being attached/detached</li>
<li>L2 Cache : enable caching of embedded/serialised fields by default</li>
<li>L2 Cache : revised process for updating an object in the L2 cache to avoid concurrency</li>
<li>Clean up ExecutionContext/ObjectProvider contract, to allow for easier addition of alternate
    StateManagers for different use-cases.</li>
<li>Change all basic types to be default persistent (so the user doesn't need to explicitly mark them
    as such), and update several to also be in the DFG</li>
<li>Change LinkedHashMap support to allow null values</li>
<li>Significant refactoring of internal DataNucleus classes (see 
    <a href="http://www.datanucleus.org/documentation/plugin_migration.html">this guide</a></li>
<li>JPA : Update enhancement contract to throw IllegalXXXException instead of JDOXXXException when
    some error condition occurs, for less JDO impact on JPA usage</li>
<li>JPA : various fixes to Criteria Query conversion to JPQL</li>
<li>JPA : add property to cater for J2EE servers that don't respect JPA spec 3.11 EM.close contract</li>
<li>Neo4j : rewrite connection code to allow multithreaded, and use single connection per PM/EM</li>
<li>MongoDB : rewrite connection code to use single connection per PM/EM</li>
<li>MongoDB : use same connection for schema checks as for PM/EM</li>
<li>RDBMS : Allow SQL "CREATE" statements to be invoked</li>
<li>RDBMS : add lazy initialisation of secondary datasource (where possible)</li>
<li>RDBMS : clean up delete handling for some situations</li>
<li>RDBMS : add support for specifying indexes on map join tables</li>
<li>XML : clean up connection handling</li>
<li>Excel : clean up connection handling</li>
<li>ODF : clean up connection handling</li>
<li>LDAP : clean up connection handling</li>
<li>Spatial : add fix to bboxTest method for PostGIS</li>
<li>Various minor bug fixes and improvements</li>
</ul>
