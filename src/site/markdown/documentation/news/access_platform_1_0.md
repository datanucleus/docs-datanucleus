<head><title>AccessPlatform 1.0</title></head>

#Release Notes for DataNucleus AccessPlatform v1.0

The 1.0 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


# DataNucleus AccessPlatform 1.0.5

__Apr 14th 2009__ : _Version 1.0.5_ includes the following changes

<ul>
<li>Bug fix so that any remaining non-transactional update when closing the PM 
    always goes to the datastore</li>
<li>Bug fix to JTA handling of afterCompletion()</li>
<li>Bug fix to the enhancer Ant task to allow fork=false</li>
<li>RDBMS: Bug fix to the SchemaTool Ant task to allow fork=false</li>
<li>XML : Fix to retrieval of objects where a class has no "xpath" specified.</li>
<li>Improvement to efficiency of EHCache contains() handling.</li>
<li>Bug fix to the reading of @FetchPlan annotation</li>
</ul>


# DataNucleus AccessPlatform 1.0.4

__Feb 1st 2009__ : _Version 1.0.4_ includes the following changes

<ul>
<li>Upgrade to NeoDatis 1.9RC1</li>
<li>Bug fix to allow registration of persistent classes when loaded by ClassLoader</li>
<li>Support for QueryResult toArray/subList</li>
</ul>


# DataNucleus AccessPlatform 1.0.3

__Dec 11th 2008__ : _Version 1.0.3_ includes the following changes

<ul>
<li>Upgrade to Apache POI 3.2</li>
<li>Support for String.startsWith/endsWith/indexOf with parameter/primary expressions</li>
<li>Catch leading/trailing blanks in persistence properties</li>
<li>Support for OpenJPA/Kodo style datastore identity (for people migrating from Kodo)</li>
<li>Support for Xcalia style datastore identity (for people migrating from Xcalia)</li>
<li>LDAP : Support for native queries rather than performing all in-memory.</li>
<li>Fix for unary minus in generic query mechanism</li>
<li>Remove enhancer "verify" mode since no longer used</li>
<li>Provide access to class bytes after enhancement via enhancer API</li>
<li>Fix to replication in some cases where object didnt exist in datastore 2</li>
<li>Fix to RDBMS large result "count" method to ignore ordering</li>
</ul>


# DataNucleus AccessPlatform 1.0.2

__Oct 30th 2008__ : _Version 1.0.2_ includes the following changes

<ul>
<li>Upgrade to ASM 3.1</li>
<li>Upgrade to JDO 2.2 final jar</li>
<li>Bug fixes to L2 caching of object version, and handling of garbage collected objects</li>
<li>Removal of a JDK1.5 method so people with JDK1.3/4 can use it</li>
<li>Fix to how fields are marked as loaded with application identity</li>
<li>Fix to replication of SCO fields</li>
<li>Fix to URL handling with DB4O plugin</li>
<li>Fix to XMLIDRef handling in XML plugin</li>
</ul>


# DataNucleus AccessPlatform 1.0.1

__Sept 23rd 2008__ : _Version 1.0.1_ includes the following changes

<ul>
<li>Support for JDO2.2 transaction isolation specification mechanism</li>
<li>Support for JPQL bulk delete for db4o, NeoDatis, Excel, XML, LDAP and JSON datastores</li>
<li>Log any invalid/unsupported persistence properties</li>
<li>Performance improvement to Excel and XML datastores to not repeatedly open/close the datastore</li>
<li>When checking for RDBMS table existence use DatabaseMetaData.getTables for performance</li>
<li>Fix logging of initialisation of Derby datastores to remove logged exception</li>
<li>Fix bug in loading of unloaded fields to cater for corner case</li>
<li>Fix bug in DB4O and NeoDatis JDOQL handling of "{alias}.b" syntax</li>
<li>Fix bug in Extents with subclasses for Excel, XML, LDAP and JSON datastores</li>
<li>Fix bug in LDAP persistence of boolean fields</li>
</ul>


# DataNucleus AccessPlatform 1.0.0.RELEASE

__Sept 1st 2008__ : _Version 1.0 RELEASE_ includes the following changes

<ul>
<li>Migration to JDO 2.2 standardised dynamic Fetch Groups from DataNucleus custom groups</li>
<li>Support for chained method operations with in-memory query evaluation</li>
<li>Support for generic compilation of query subqueries</li>
<li>Bug fix so JPA persistence.jar doesnt need to be in CLASSPATH when not using JPA</li>
<li>Support RDBMS dynamic schema upgrades when new implementations of an interface
    are encountered.</li>
<li>Bug fix for loading of implementations of interfaces and subsequent handling</li>
<li>Add support for datastore identity with Excel datastores</li>
<li>Bug fix to Excel datastores for persistence of null field values, and for retrieval
    of Float, Double, Integer, Long, BigDecimal, BigInteger</li>
<li>Add support for cascade delete with NeoDatis datastores</li>
<li>Add support for specified indexes with NeoDatis datastores</li>
<li>Bug fix for cascade delete with db4o datastores</li>
</ul>


# DataNucleus AccessPlatform 1.0.0.M4

__Aug 4th 2008__ : _Version 1.0 Milestone 4_ includes the following changes

<ul>
<li>Upgrade to JDO 2.2 (snapshot), NeoDatis 1.9-beta-3, Apache POI 3.1</li>
<li>Added cache for compiled queries for XML, db4o, Excel, NeoDatis, JSON and LDAP</li>
<li>Added support for NeoDatis embedded server</li>
<li>Added full support for JPQL query compilation using generic compiler</li>
<li>Added support for in-memory JPQL query evaluation of all spec required functions.</li>
<li>Added support for in-memory JDOQL query evaluation of all spec required methods, with
    the exception of Collection.contains, Map.containsKey, Map.containsValue, Map.get</li>
<li>Support for JDO2.2 @Cacheable allowing control over classes/fields to be cached</li>
<li>Added pluggable support for generic query methods/functions</li>
<li>Added support for use of implicit/explicit parameters with generic JDOQL/JPQL</li>
<li>Added support for use of DISTINCT with generic JDOQL/JPQL</li>
<li>Expanded the support for in-memory evaluation of aggregates to cater for all types of 
    fields</li>
<li>Bug fix to runtime bytecode enhancement allowing its use with annotated classes, and
    added optimisation to specify the packages to be runtime enhanced providing big speedups</li>
<li>Fixes to allow complete use of Access Platform in a java security environment</li>
<li>Support for JPA2 @ElementCollection/@CollectionTable</li>
<li>Support for performing db4o/NeoDatis JDOQL/JPQL queries totally in-memory where required</li>
<li>Bug fix to allow use of RDBMS datastores that store in lowercase without the need to
    provide a persistence property to specify this</li>
<li>Bug fix to RDBMS persistence of complicated hierarchy with container+inheritance
    and multiple relations between container and element, avoiding FK violation</li>
<li>Bug fix to L2 caching for multithreaded operations</li>
</ul>


# DataNucleus AccessPlatform 1.0.0.M3

__July 6th 2008__ : _Version 1.0 Milestone 3_ includes the following changes

<ul>
<li>Rewritten Level 2 caching, allowing full control over which classes are cached
    and which fields of which classes are cached. Fixed bugs relating to deleted objects
    previously being cached, and caching of SCO fields</li>
<li>Rewritten JPQL compiler for use by all datastores.</li>
<li>Addition of an in-memory JPQL evaluator, supporting basic JPQL syntax so far.</li>
<li>Support for JDO2.2 "ReadOnly"</li>
<li>Change in-memory evaluation of JDOQL/JPQL queries to allow evaluation of specific
    components of the query (rather than the whole query)</li>
<li>Support for in-memory JDOQL/JPQL evaluation of "/", "%", "&lt;", "&gt;", 
    "&lt;=", "&gt;=", etc</li>
<li>Support for in-memory JDOQL evaluation of all common methods (String.matches,
    String.toUpperCase, etc)</li>
<li>Bug fix to List.remove(int) when using optimistic transaction</li>
<li>Bug fix to in-memory JDOQL evaluation of grouping/result clauses</li>
<li>Support for JPQL querying of db4o datastores</li>
<li>Support for JPQL querying of NeoDatis ODB datastores</li>
<li>Support for JPQL querying of XML documents</li>
<li>Support for JPQL querying of Excel documents</li>
<li>Support for JPQL querying of LDAP datastores</li>
<li>Support for JPQL querying of JSON datastores</li>
<li>Removed original JDOQL querying for db4o - now replaced by generic process, with inbuilt
    support for more JDOQL syntax.</li>
<li>Support for persistence of wider range of Object types to Excel datastores, using new
    generic "String-based" persistence</li>
<li>Optimisation of location of an object in Excel datastores resulting in reduced 
    object instantiation</li>
<li>Support for connection-pooling of LDAP connections (contrib Stefan Seelmann)</li>
<li>Support for JDOQL querying of NeoDatis ODB datastores</li>
<li>Support for multiple levels of "xpath" on XML datastores</li>
<li>Bug fix to GROUP BY on RDBMS datastores when the query has multiple components of a UNION</li>
<li>Bug fix on RDBMS datastores to re-enable creation of constraints</li>
<li>Bug fix on RDBMS datastores when using subclass-table inheritance and single subclass</li>
</ul>


# DataNucleus AccessPlatform 1.0.0.M2

__June 1st 2008__ : _Version 1.0 Milestone 2_ includes the following changes

<ul>
<li>Support for persistence to DB4O as an embedded server (contrib from Joe Batt)</li>
<li>Support for some early draft JPA 2 methods relating to caching and querying</li>
<li>Support for persistence to 
    <a href="http://www.datanucleus.org/products/accessplatform/neodatis/support.html">NeoDatis</a></li>
<li>Support for persistence to
    <a href="http://www.datanucleus.org/products/accessplatform/json/support.html">JSON (RESTful)</a></li>
<li>Improvements to persistence to XML, including allowing defining of the root for each class.</li>
<li>Significant improvements in support for XA transactions with the JDO JCA adapter, used
    extensively by <a href="http://www.jfire.org">JFire</a></li>
<li>Provision of a public 
    <a href="http://www.datanucleus.org/products/accessplatform/rdbms/datastore_schema_api.html">API</a>
    for accessing schema information for RDBMS</li>
<li>Bug fixes to L2 caching of SCO fields</li>
<li>Bug fix to detachment when a field was previously attached unchanged.</li>
<li>Bug fix to support @Persistent "recursionDepth" which was previously ignored.</li>
<li>Memory footprint improvements for StateManager.</li>
<li>Optimisation of some aspects of relationship management to prevent unnecessary loading
    of fields when not needed</li>
<li>Bug fix to use of autoincrement fields with PostgreSQL when used in non-default schema</li>
<li>Bug fix to use of "JDOHelper.getObjectId" within JDOQL for composite PK app id cases</li>
<li>Bug fix to the enhancement of jdoMakeDirty for detached cases to allow for inheritance</li>
</ul>

# DataNucleus AccessPlatform 1.0.0.M1

__April 25th 2008__ : _Version 1.0 Milestone 1_ includes the following changes (to JPOX codebase)

<ul>
<li>Support for persistence to and simple JDOQL querying of LDAP</li>
<li>Support for persistence to and simple JDOQL querying of Excel</li>
<li>Support for persistence to and simple JDOQL querying of XML</li>
<li>Support for SQL querying of db4o</li>
<li>Several bug fixes, and much restructuring of the JPOX codebase</li>
</ul>

