<head><title>Products</title></head>

# Section : [Documentation](../index.html) > Products

## DataNucleus Plugins Documentation

DataNucleus products are built from a series of plugins. Each plugin is an OSGi bundle. 
Each plugin provides a level of functionality to the overall DataNucleus platform. This 
section documents the available provided plugins, and their purpose and state.
The plugins can be individually downloaded if required rather than waiting for the next
full release of a product, but if doing that always be careful of cross-compatibility of versions of plugins.


+ [datanucleus-core](https://github.com/datanucleus/datanucleus-core) : Primary building block of DataNucleus persistence
+ APIs
	* [datanucleus-api-jdo](https://github.com/datanucleus/datanucleus-api-jdo) : Support for persistence using the JDO API
	* [datanucleus-api-jpa](https://github.com/datanucleus/datanucleus-api-jpa) : Support for persistence using the JPA API
	* [datanucleus-api-rest](https://github.com/datanucleus/datanucleus-api-rest) : Support for persistence using a REST API
+ Datastores
	* [datanucleus-cassandra](https://github.com/datanucleus/datanucleus-cassandra) : Support for persistence to Cassandra
	* [datanucleus-excel](https://github.com/datanucleus/datanucleus-excel) : Support for persistence to Excel
	* [datanucleus-hbase](https://github.com/datanucleus/datanucleus-hbase) : Support for persistence to HBase
	* [datanucleus-json](https://github.com/datanucleus/datanucleus-json) : Support for persistence to JSON
	* [datanucleus-ldap](https://github.com/datanucleus/datanucleus-ldap) : Support for persistence to LDAP
	* [datanucleus-mongodb](https://github.com/datanucleus/datanucleus-mongodb) : Support for persistence to MongoDB
	* [datanucleus-neo4j](https://github.com/datanucleus/datanucleus-neo4j) : Support for persistence to Neo4j
	* [datanucleus-neodatis](https://github.com/datanucleus/datanucleus-neodatis) : Support for persistence to NeoDatis
	* [datanucleus-odf](https://github.com/datanucleus/datanucleus-odf) : Support for persistence to ODF
	* [datanucleus-rdbms](https://github.com/datanucleus/datanucleus-rdbms) : Support for persistence to RDBMS
	* [datanucleus-xml](https://github.com/datanucleus/datanucleus-xml) : Support for persistence to XML
+ Other Plugins
	* [datanucleus-java8](https://github.com/datanucleus/datanucleus-java8) : Support for persisting fields of Java 1.8 types
	* [datanucleus-cache](https://github.com/datanucleus/datanucleus-cache) : Support for third-party caching tools
	* [datanucleus-jodatime](https://github.com/datanucleus/datanucleus-jodatime) : Support for persisting fields of Jodatime types
	* [datanucleus-geospatial](https://github.com/datanucleus/datanucleus-geospatial) : Support for persisting fields of Geospatial types
	* [datanucleus-guava](https://github.com/datanucleus/datanucleus-guava) : Support for persisting fields of Guava types
	* [datanucleus-jdo-jca](https://github.com/datanucleus/datanucleus-jdo-jca) : Support for using JDO in JavaEE environments via JCA
	* [datanucleus-jdo-query](https://github.com/datanucleus/datanucleus-jdo-query) : Support for generating JDO typesafe query classes
	* [datanucleus-jpa-query](https://github.com/datanucleus/datanucleus-jpa-query) : Support for generating JPA criteria query classes
+ Tools
	* [datanucleus-maven-plugin](https://github.com/datanucleus/datanucleus-maven-plugin) : For developing applications using DataNucleus and Maven
	* [datanucleus-eclipse-plugin](https://github.com/datanucleus/datanucleus-eclipse-plugin) : For developing application using DataNucleus in Eclipse
	* [datanucleus-idea-plugin](https://github.com/datanucleus/datanucleus-idea-plugin) : For developing applications using DataNucleus in Intellij IDEA
+ Inactive Plugins
	* datanucleus-enhancer - now part of datanucleus-core
	* datanucleus-java5 - now part of datanucleus-core and datanucleus-api-jpa
	* maven1 - no longer used, since Maven1 is deprecated
	* datanucleus-db4o - no longer supported. Code still present in SourceForge if required
	* datanucleus-db4o-sql - no longer supported. Code still present in SourceForge if required
	* datanucleus-javaxtime - now part of datanucleus-core
	* datanucleus-awtgeom - now part of datanucleus-geospatial
	* datanucleus-xmltypeoracle - now part of datanucleus-rdbms
	* datanucleus-connectionpool - now part of datanucleus-rdbms
	* datanucleus-spatial - now part of datanucleus-geospatial
	* datanucleus-management - now part of datanucleus-core
