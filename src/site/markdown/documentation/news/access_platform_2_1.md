<head><title>AccessPlatform 2.1</title></head>

#Release Notes for DataNucleus AccessPlatform v2.1

The 2.1 release of AccessPlatform is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 


_Version 2.1_ includes the following over 2.0

<ul>
<li>Support for persistence to OOXML files</li>
<li>Support for persistence to GoogleStorage</li>
<li>Support for persistence for fields of some javax.time types</li>
<li>Support for persistence for fields of some Google Collection types</li>
<li>Changed to use rewritten JDOQL implementation for RDBMS by default. This makes many more 
    JDOQL statements runnable than were previously possible</li>
<li>Uses JDO3 "final" jar</li>
<li>Uses JPA2 "final" jar</li>
<li>Supports full JPA2 definition of JPQL</li>
<li>Supports JPA2 static metamodel creation</li>
<li>Supports JPA2 orphan removal</li>
<li>Support for embedded PC objects with Excel persistence</li>
<li>Support for using spatial methods in queries with the new JDOQL implementation for RDBMS</li>
<li>Support for BoneCP RDBMS connection pooling library</li>
<li>Many bug fixes, and minor feature additions.</li>
</ul>



# DataNucleus AccessPlatform 2.1.4

__Dec 18th 2010__ : _Version 2.1.4_ includes the following changes

<ul>
<li>Fix to bug in determination of inheritance level of application identity object</li>
<li>Fix couple of places where code not thread-safe</li>
<li>Fix to ConnectionFactory2 usage</li>
<li>JPA : Support for fetch groups (DataNucleus extension)</li>
<li>JPA : few minor corrections to JPA2 handling</li>
</ul>


# DataNucleus AccessPlatform 2.1.3

__Nov 13th 2010__ : _Version 2.1.3_ includes the following changes

<ul>
<li>Drop "attachPolicy" and provide complete attachment in default scenario</li>
<li>Couple of fixes to result handling in in-memory query evaluator</li>
<li>RDBMS : Allow column reuse for multiple fields of a class</li>
<li>RDBMS : Fix to use of subclass-table with 1-1 bidirectional relations</li>
<li>RDBMS : Fix to use of lengths with BLOB/CLOB on MySQL</li>
<li>RDBMS : Fix to index/FK creation on Derby to avoid warning messages</li>
<li>JPA : Outline implementation of JPA2 lock methods</li>
<li>JPA : Support use of @PrimaryKeyJoinColumn for 1-1s</li>
</ul>


# DataNucleus AccessPlatform 2.1.2

__Oct 20th 2010__ : _Version 2.1.2_ includes the following changes

<ul>
<li>Improved merge of metadata information when sequence or cascade info specified in annotations</li>
<li>Fix to PMF startup process so that persistence properties are registered before enablement
    of some services</li>
<li>RDBMS : fix to use of positional parameters</li>
<li>RDBMS : fix to validation of candidate keys, that prevented creation of some unique keys under
    some circumstances</li>
<li>RDBMS : fix to List.get() when used in result clause of JDOQL query</li>
<li>RDBMS : fix to creation of sequences with SchemaTool to take extension props</li>
<li>JPA : fix to case where sequence name not set</li>
<li>JPA : fix to EM.getReference to not validate the object</li>
<li>JPA : fix to use of @Enumerated with @Column</li>
<li>Enhancer : fix to runtime enhancement, class loading problem</li>
<li>Enhancer : fix to error message of override of invalid field</li>
<li>Cache : add option to allow retention of cached objects after close of PMF/EMF, for the case
    where used by other instances</li>
</ul>


# DataNucleus AccessPlatform 2.1.1

__Jun 26th 2010__ : _Version 2.1.1_ includes the following changes

<ul>
<li>Changed method for instantiating objects using application identity when returned by queries,
    reducing the memory and CPU requirement</li>
<li>RDBMS : Ability to specify global default for sequence/increment value generator cache size</li>
<li>RDBMS : Fix to BLOB/CLOB handling with Derby 10.6+</li>
<li>RDBMS : Full support for HSQLDB 2.0</li>
<li>RDBMS : Fix to query String.startsWith/endsWith on H2</li>
<li>RDBMS : Fix to query String.substring(int, int) on Derby</li>
<li>RDBMS : Fix to BLOB/CLOB handling in queries with MSSQL</li>
<li>RDBMS : Support for batched INSERTs, so you re-run all of your benchmarks ;-)</li>
<li>RDBMS : SchemaTool now creates necessary auto-start table, sequence table, and sequences</li>
<li>JSON : Fix to HTTP Error 409 handling</li>
</ul>


# DataNucleus AccessPlatform 2.1.0.RELEASE

__Jul 11th 2010__ : _Version 2.1 RELEASE_ includes the following changes

<ul>
<li>Changed to use JDO3 jar</li>
<li>Support for persistence to GoogleStorage</li>
<li>Support for persistence of some Google Collections classes</li>
<li>Added initial version of a generic query optimiser, removing redundant variable clauses</li>
<li>Fix to JPA inheritance strategy "JOINED" when having subclasses with discriminator</li>
<li>Fix to persist of new object with collection that contains detached objects</li>
<li>Fix to persist of new object with related detached compound identity chain</li>
<li>Optimise out some SCO collection operations such as add+delete of same object in succession</li>
<li>Support persist of enums as arbitrary value</li>
<li>JPA2 : Support for orphan removal</li>
<li>JPA2 : Support for JPQL "INDEX" keyword</li>
<li>RDBMS : Fix to setting of BLOB/CLOB on bidirectional relations for Oracle</li>
<li>RDBMS : Fix to SQL table namer to allow for unioned statements when choosing table name</li>
<li>RDBMS : Support for use of BoneCP connection pools</li>
</ul>


# DataNucleus AccessPlatform 2.1.0.M3

__May 21st 2010__ : _Version 2.1 Milestone 3_ includes the following changes

<ul>
<li>Change some Maven dependencies to allow use with JDO3</li>
<li>Fix to generic compilation for "param.field" and use of subquery candidate</li>
<li>Extend in-memory query evaluation result clause handler to allow variable expression and more</li>
<li>Fix to in-memory query evaluation for String.matches when the string is null</li>
<li>RDBMS : Fix to cascade delete on 1-1 when there is a FK present (so leave to datastore)</li>
<li>RDBMS : Fix to Derby syntax for CROSS JOIN pre-10.6</li>
<li>RDBMS : Fix to Derby usage with JDOQL2 to restrict use of CLOB/BLOC with DISTINCT/UNION</li>
<li>RDBMS : Add ability to query in datastore when candidate collection being input</li>
<li>RDBMS : Fix to Map.containsKey/containsValue to allow for contained variable already having
    a table in the statement</li>
<li>RDBMS : Fix to use of subqueries with parameters linking back to the main query</li>
<li>RDBMS : Fix to use of input positional parameters when one is used multiple times in the 
    statement</li>
<li>RDBMS : Fetching optimisation when fetching a field and taking the opportunity to load
    any other non-relation or 1-1/N-1 unloaded fields</li>
<li>RDBMS : Fix to SQL table namers to allow for multiple levels of subquery</li>
<li>RDBMS : Fix to Collection.contains(Enum)</li>
<li>RDBMS : Fix to use of parameter with null value in comparisons</li>
<li>RDBMS : Fix to use of explicit parameters in subquery</li>
<li>RDBMS : Fix to generation of "count" query to get size so it takes into account 
    DISTINCT in the main query</li>
<li>Excel : Support for persistence of primitive wrapper types</li>
<li>Excel : Support for persistence of embedded PC fields (Guido)</li>
<li>Spatial : Added support for all Oracle/PostGIS/MySQL specific methods</li>
<li>Spatial : Fix to handling of user object in Jts objects when querying</li>
<li>Spatial : Addition of remaining methods for querying</li>
</ul>


# DataNucleus AccessPlatform 2.1.0.M2

__Apr 26th 2010__ : _Version 2.1 Milestone 2_ includes the following changes

<ul>
<li>Add ability to skip the check on unused input parameters to queries</li>
<li>Fix issue with detachment when finding an object already detached but not far enough</li>
<li>Add support for compilation of queries with parameters in subqueries linking back to the main query</li>
<li>Fix to L2 caching of StringBuffer fields to cache a copy</li>
<li>Fix to handle input query with special characters (tab, eol, etc)</li>
<li>Extend query compilation to store whether the query result is distinct</li>
<li>Support specification of interface fields where there isn't currently an available implementation</li>
<li>Fix to use of dynamic fetch groups in multiple threads</li>
<li>Fix to support non-standard SQL statements (stored procs, statements not starting with
    SELECT/INSERT/UPDATE/MERGE/DELETE)</li>
<li>Fix to the query in-memory evaluator to support aggregate names in upper or lower case</li>
<li>Fix to a couple of situations where a versioned object can be returned to the user without 
    the version set</li>
<li>Fix to reset the version of an object on rollback()</li>
<li>Fix to SCOListIterator</li>
<li>RDBMS : Fix to generation of indexes for reference fields when having a FK per implementation
    so that the index is created for the implementations FK only</li>
<li>RDBMS : Fix JDOQL2 to not select CLOB fields when using UNION or DISTINCT for Derby</li>
<li>RDBMS : Fix JDOQL2 to add parentheses around ORed clauses</li>
<li>RDBMS : Fix JDOQL2 to pick the correct statement when using methods in subqueries</li>
<li>RDBMS : Fix JDOQL2 "alpha-namer" to handle more than 26 table groups</li>
<li>RDBMS : Fix JDOQL2 to handle comparisons of interface field with an implementation</li>
<li>RDBMS : Support use of CHECK constraint when persisting boolean as numeric</li>
<li>RDBMS : Change HSQLDB use of LIMIT to append to the end of the statement</li>
<li>RDBMS : Support for use of SQLXML type with DB2 (contrib)</li>
<li>RDBMS : Fix to JDOQL2 for use of input parameters with multiple columns</li>
<li>JPA : Add support for JPQL "case" expressions</li>
<li>JPA : Add support for generation of JPA2 static metamodel classes</li>
<li>JPA : Change to handling of "columnDefinition" to expect the type to be included</li>
<li>Enhancer : when using JDK1.6 and having the enhancer in the CLASSPATH default to not enabling
    the annotation processor to enhance the class(es) being compiled</li>
</ul>


# DataNucleus AccessPlatform 2.1.0.M1

__Apr 2nd 2010__ : _Version 2.1 Milestone 1_ includes the following changes

<ul>
<li>Addition of plugin for persistence of javax.time (JSR0310) types</li>
<li>Fix to a typo in the use of ConnectionFactory when defining the datastore as a DataSource</li>
<li>Cleanup to process of creation of L1/L2/Query caches</li>
<li>Change generic query compilation expression tree bidirectional for ease of navigation</li>
<li>Support generic query compilation of {param}.field</li>
<li>Enforce JDO2 spec rules for JDOQL result/grouping/ordering clauses validity</li>
<li>Fix to generic query compilation of {variable}.field</li>
<li>Fix to generic query compilation of cast expressions</li>
<li>Added checks on invalid use of keywords during generic query compialtion</li>
<li>Fix to generic query compilation of {array}.length</li>
<li>Fix to use of Extent to close all iterators correctly</li>
<li>FIx to in-memory evaluation of queries to better handle date equality</li>
<li>Fix to getParent() of class/package metadata of JDO Metadata API</li>
<li>Fix to use of set() on ListIterator obtained from list wrapper</li>
<li>Fix to persistence of object with reference to the same object</li>
<li>RDBMS : change to use "JDOQL2" implementation by default. Use "JDOQL-Legacy" if wanting
    the old JDOQL implementation.</li>
<li>RDBMS : having expression that are not boolean should throw XXXUserException for JDOQL2</li>
<li>RDBMS : fix to use of parameters for range and passed in as unnamed to API</li>
<li>RDBMS : fix to caching of queries when using String.matches with input parameter for JDOQL2</li>
<li>RDBMS : fix to not create indexes for serialised field (problem on MySQL)</li>
<li>RDBMS : support override of datastore mapping by user plugins</li>
<li>RDBMS : fix to only use CROSS JOIN with Derby from v10.6 onwards</li>
<li>RDBMS : fix to use of Boolean expression/literals for JDOQL2</li>
<li>RDBMS : fix to candidate query on persistent interface candidate for JDOQL2</li>
<li>RDBMS : add support for persistent object "identity" as input parameter for JDOQL2</li>
<li>RDBMS : fix to numeric type comparisons for JDOQL2</li>
<li>RDBMS : fix to use of parameter in result clause when null for JDOQL2</li>
<li>RDBMS : add support for Cast expression in result clause for JDOQL2</li>
<li>RDBMS : add support for array of expressions in JDOQL2</li>
<li>RDBMS : add support for joins to interface implementations in JDOQL2</li>
<li>RDBMS : add support for subquery.contains() in JDOQL2</li>
<li>RDBMS : fix handling of DISTINCT in JDOQL2</li>
<li>RDBMS : make use of Query imports when resolving classes in instanceof/cast for JDOQL2</li>
<li>RDBMS : fix use of navigation of N-1 relation via join table in JDOQL2</li>
<li>RDBMS : Delete "JPQL-Legacy" implementation</li>
<li>JodaTime : fix handling of null fields</li>
<li>JPA : upgrade to use JPA2 "final" jar API</li>
<li>Much internal refactoring has also been performed to remove unneeded components
    or to simplify the API's for things needed in the 2.1 timeline. Any use of internal
    API's by applications will likely need changes.</li>
</ul>
