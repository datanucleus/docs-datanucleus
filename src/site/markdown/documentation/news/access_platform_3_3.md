<head><title>AccessPlatform 3.3</title></head>

#Release Notes for DataNucleus AccessPlatform v3.3

The 3.3 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 3.3_ includes the following over 3.2

<ul>
<li>JPA 2.1 : support for Criteria FROM "ON" clause.</li>
<li>JPA 2.1 : support for Criteria UPDATE/DELETE statements.</li>
<li>JPA 2.1 : support for ForeignKey and Index specification for schema generation.</li>
<li>JPA 2.1 : support for JPQL "FUNCTION"</li>
<li>JPA 2.1 : support for EntityGraphs</li>
<li>Several bug fixes, and minor feature additions.</li>
</ul>


# DataNucleus AccessPlatform 3.3.6

__Jan 1st 2014__ : _Version 3.3.6_ includes the following changes

<ul>
<li>Auto-generate MANIFEST.MF OSGi information using Maven bundle plugin</li>
<li>Change use of StringBuffer to StringBuilder for efficiency</li>
<li>Add fix to enhancement contract for JDK1.7+ for getter when using persistence properties</li>
<li>Add support for in-memory query evaluation of String.concat</li>
<li>Provide fallback API for runtime enhancement</li>
<li>Add metadata checks for some common primary-key specification errors</li>
<li>Support persistence of StringBuilder fields</li>
<li>JPA : Fix Criteria FromImpl getJoins/getFetches to return empty set when null</li>
<li>XML : restructured to allow potential of using different JAXB implementations internally</li>
<li>XML : add support for XML indentation formatting</li>
<li>Cache : upgraded Coherence support to 3.6+</li>
<li>RDBMS : support added for query range in datastore for Derby, SQLServer 2012, Firebird</li>
<li>RDBMS : support added for sequences with SQLServer 2012</li>
<li>RDBMS : support added for M-N relations using ordered lists</li>
<li>RDBMS : fixes to schema creation for M-N relations</li>
<li>RDBMS : support added for parameters with bulk-fetch feature</li>
<li>RDBMS : bulk-fetch support added for array fields</li>
<li>RDBMS : add ability to turn off bulk-fetch on a per-query basis</li>
<li>Geospatial : new plugin comprising merged spatial/awtgeom plugins</li>
<li>Geospatial : added some missing PostGIS methods and validated against latest PostGIS JDBC driver</li>
<li>MongoDB : improved handling of ordering/range parts of query to correct previous contribution</li>
<li>MongoDB : upgrade to use latest java driver</li>
<li>HBase : fix problem with retrieval of Enum stored as numeric (ordinal)</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.3.5

__Dec 10th 2013__ : _Version 3.3.5_ includes the following changes

<ul>
<li>Wrap any exception thrown from JDOHelper.getObjectId so that it meets the JDO spec</li>
<li>Fix to class loading for property validators for OSGi</li>
<li>Couple of fixes for optimistic relationship management</li>
<li>JDO : Change PMF to be Serializable</li>
<li>JPA : Change EMF and CriteriaQuery to be Serializable</li>
<li>JPA : Fix criteria CONCAT support to give correct JPQL string form</li>
<li>JPA : Add support for IN with criteria queries via CriteriaBuilder</li>
<li>JPA : Add support for JPQL "TREAT" in WHERE clause</li>
<li>RDBMS : Add support for bulk fetch of multi-valued collection fields of a candidate when in FetchPlan of a query (removes "1+N" problem)</li>
<li>RDBMS : Add support for SQLServer to handle JDOQL String.substring with 2 args (Daniel Dai)</li>
<li>RDBMS : Add support for JDOQL String.concat (Daniel Dai)</li>
<li>RDBMS : Fix to detection of type of backing store required for a collection, using metadata more</li>
<li>MongoDB : Add support for specifying the MongoOptions when creating the first connection (Robin Zhang)</li>
<li>Spatial : Fix some missing PostGIS methods</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.3.4

__Nov 19th 2013__ : _Version 3.3.4_ includes the following changes

<ul>
<li>Metadata : Add level of locking to metadata load process to assist in multithreaded environments</li>
<li>Metadata : fix bug in OrderMetadata for multithreaded environments</li>
<li>Fix to some potential startup problems with ExecutionContext/ObjectProvider in multithreaded environments</li>
<li>Change "datanucleus.SerializeRead", "datanucleus.cache.collections", "datanucleus.deletionPolicy", 
    "datanucleus.query.jdoql.allowAll", "datanucleus.query.sql.allowAll" to be overrideable on the PM/EM</li>
<li>Cache : update javax.cache support to "1.0-PFD" standard</li>
<li>JPA : Fix to metamodel Attribute.isOptional to return false for PK fields</li>
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
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.3.3

__Oct 23rd 2013__ : _Version 3.3.3_ includes the following changes

<ul>
<li>JPA : fix to metamodel SimpleAttributeImpl.isVersion (Adrian Ber)</li>
<li>JPA : add support for multi-field join syntax in JPQL FROM clause</li>
<li>JPA : update to handling of JPQL range when just first result set</li>
<li>JPA : support inherited TypeConverters (Adrian Ber)</li>
<li>JPA : pass properties from EMF to ClassTransformer when run in managed mode</li>
<li>RDBMS : fix for SQLServer schema name problem (Shanyu Zhao)</li>
<li>RDBMS : add support for using FetchPlan when querying over "complete-table" candidate (previous just retrieved primary key)</li>
<li>RDBMS : improvement in process to determine class name when no subclasses known about, to avoid SQL</li>
<li>RDBMS : support for persisting Double type into SQLServer FLOAT datastore type (Shuaishai Nie)</li>
<li>JSON : fix to retrieval of objects in query so that application-identity cases have id assigned</li>
<li>MongoDB : add support for query ordering being processed in the datastore (Marcin Jurkowski))</li>
<li>Rename "google-collections" plugin to "guava"</li>
<li>JDO : distribute jdo-api 3.1-rc1</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.3.2

__Aug 31st 2013__ : _Version 3.3.2_ includes the following changes

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


# DataNucleus AccessPlatform 3.3.1

__Aug 1st 2013__ : _Version 3.3.1_ includes the following changes

<ul>
<li>Provide different ObjectProvider (StateManager) when using non-RDBMS datastores</li>
<li>Improve process of defining static query method support</li>
<li>In-memory querying : add support for String.charAt(int)</li>
<li>Upgrade javax.cache support to v0.8</li>
<li>MetaData : fix to merging of unmapped columns from ORM mapping file</li>
<li>JPA : fix to handling of ForeignKey annotations</li>
<li>JPA : fix to OSGi MANIFEST version info</li>
<li>RDBMS : add support for ordering with NULLS FIRST/NULLS LAST in JDOQL/JPQL</li>
<li>RDBMS : add support for use of startup load-scripts etc</li>
<li>RDBMS : fix to entrySet for FK Map where the key/value have inheritance</li>
<li>RDBMS : fix to handling of auto-apply of TypeConverter</li>
<li>MongoDB : fix to handling of version field under some circumstances</li>
<li>Spatial : various additions for use with PostGIS (Baris Ergun)</li>
<li>Various other bug fixes and minor improvements</li>
</ul>


# DataNucleus AccessPlatform 3.3.0.RELEASE

__Jun 27th 2013__ : _Version 3.3 RELEASE_ includes the following changes

<ul>
<li>JPA : Add support for JPA 2.1 EntityGraph</li>
<li>JPA : Add support for JPA 2.1 @Converter autoApply and @Convert disableConversion</li>
<li>Fix to JPA fields marked as embedded to cascade persist/delete etc</li>
<li>Drop support for DataNucleus extension @FetchGroup/@FetchPlan</li>
<li>Fix to attach process for SCO collections under some circumstances</li>
<li>Fix to L2 cache to not perform lookup if identity is for class that is not cacheable</li>
<li>Schema Generation : fix to case where using complete-table and version/discriminator not being added to subclasses</li>
<li>Fix to query caching to cater for FetchPlan being different on a query</li>
</ul>


# DataNucleus AccessPlatform 3.3.0.M1

__Jun 9th 2013__ : _Version 3.3 Milestone 1_ includes the following changes

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
<li>JPA : run against JPA 2.1 API jar</li>
<li>JPA : Support JPA 2.1 Index and ForeignKey specification</li>
<li>JPA : Support JPA 2.1 JPQL "FUNCTION"</li>
<li>JPA : Support JPA 2.1 Criteria UPDATE/DELETE</li>
<li>JPA : Support JPA 2.1 FROM "ON" in Criteria query</li>
<li>JPA : Drop support for DN extension @Index annotation (use JPA 2.1 annotation now)</li>
<li>RDBMS : Schema Generation improvement to better cater for any ordering of input classes</li>
<li>RDBMS : Schema Generation fix to recursive initialisation of PK of a table</li>
<li>RDBMS : Fix to handling of FK Map where key/value have inheritance and the value/key is stored
    in a superclass</li>
<li>RDBMS : Fix to value-map discriminator handling for embedded object</li>
<li>RDBMS : add ability to invoke any SQL function (for JPA 2.1)</li>
<li>MongoDB : fix to explicitly specify the storage type for primitive wrapper types</li>
<li>Various minor bug fixes and improvements</li>
</ul>
