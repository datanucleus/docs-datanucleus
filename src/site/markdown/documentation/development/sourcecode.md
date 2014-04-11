<head><title>Source Code</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## DataNucleus Source Code : GitHub Repositories
![GitHub](../../images/GitHub-Mark-64px.png)

DataNucleus source code is hosted on [GitHub](https://github.com/datanucleus) and uses the [Git](http://git-scm.com/) 
(distributed) source code version control system. You can check out from GitHub using the following.

	Using SSH: git clone git@github.com:datanucleus/{repository-name}.git

	Using HTTPS: git clone https://github.com/datanucleus/{repository-name}.git

Obviously, not everyone will want to check out all DataNucleus project repositories, so use this command for the particular 
repositories that you require. Note that GitHub repositories are all browsable via the web, for example 
[the DataNucleus Neo4j datastore plugin](https://github.com/datanucleus/datanucleus-neo4j).
Note that all plugin repositories are [Maven projects](http://maven.apache.org) so you need to understand how to build 
with Maven to build these plugins.

DataNucleus can be easily developed using Maven, Eclipse,  or other IDEs (let us know if you write docs for how to develop DataNucleus with a different IDE).
You require __JDK1.8+__ (JDK1.7 would be adequate for DN 3.x), a __Git client__ (to download/commit DataNucleus Git-based projects) and __an editor__.

[__Note that (previous) source code for all versions up to and including 3.3.5 is stored in [SourceForge](sourcecode_sf.html)__]

### GitHub : Plugins

Within the DataNucleus project over on GitHub you have various repositories providing actual DataNucleus plugins. These are currently

[datanucleus-core](https://github.com/datanucleus/datanucleus-core)

APIs :  
[datanucleus-api-jdo](https://github.com/datanucleus/datanucleus-api-jdo)  
[datanucleus-api-jpa](https://github.com/datanucleus/datanucleus-api-jpa)  
[datanucleus-api-rest](https://github.com/datanucleus/datanucleus-api-rest)  

Datastores :  
[datanucleus-cassandra](https://github.com/datanucleus/datanucleus-cassandra)  
[datanucleus-excel](https://github.com/datanucleus/datanucleus-excel)  
[datanucleus-hbase](https://github.com/datanucleus/datanucleus-hbase)  
[datanucleus-json](https://github.com/datanucleus/datanucleus-json)  
[datanucleus-ldap](https://github.com/datanucleus/datanucleus-ldap)  
[datanucleus-mongodb](https://github.com/datanucleus/datanucleus-mongodb)  
[datanucleus-neo4j](https://github.com/datanucleus/datanucleus-neo4j)  
[datanucleus-neodatis](https://github.com/datanucleus/datanucleus-neodatis)  
[datanucleus-odf](https://github.com/datanucleus/datanucleus-odf)  
[datanucleus-rdbms](https://github.com/datanucleus/datanucleus-rdbms)  
[datanucleus-xml](https://github.com/datanucleus/datanucleus-xml)  

Type support :  
[datanucleus-geospatial](https://github.com/datanucleus/datanucleus-geospatial)  
[datanucleus-guava](https://github.com/datanucleus/datanucleus-guava)  
[datanucleus-jodatime](https://github.com/datanucleus/datanucleus-jodatime)  

Others :  
[datanucleus-cache](https://github.com/datanucleus/datanucleus-cache)  
[datanucleus-jdo-query](https://github.com/datanucleus/datanucleus-jdo-query)  
[datanucleus-jdo-jca](https://github.com/datanucleus/datanucleus-jdo-jca)  
[datanucleus-jpa-query](https://github.com/datanucleus/datanucleus-jpa-query)  

All plugins are independently versioned ("master" is the latest branch). This is because they have their own lifecycle, and plugins are
bundled together into the "products" (e.g AccessPlatform). So we could have AccessPlatform version 1.1 using version X of a plugin, and 
AccessPlatform version 2.0 using version Y of that plugin because it needs some new functionality.

#### Building with Maven

All DataNucleus plugins are Maven projects, with a _pom.xml_. To build and install the plugin using Maven simply type

	mvn clean install

and the plugin is built and installed in your local Maven repository. If you are developing some feature that requires updates to, 
for example core (__datanucleus-core__), __an api__ (e.g __datanucleus-api-jdo__) and a datastore (e.g __datanucleus-rdbms__) then you will need
to build these in the same order, core first, then the API, then the datastore.

#### Building with Eclipse

When building/developing using Eclipse the first thing you need to do is install the Eclipse __m2e__ plugin (if not already done).
This means that the build of any plugin will build using Maven (and get its dependencies from Maven).
You then need to import all DataNucleus projects you are working on. Since each plugin in Eclipse will build using Maven
you don't need to have all dependent projects present too, just the ones you're working on. 

<a name="tests"/>
### GitHub : Tests

In order to test DataNucleus capabilities we have many end-to-end tests. In the GitHub DataNucleus project these are available
in the repository [tests](https://github.com/datanucleus/tests). Below that you have some framework projects that need building first, 
then there are tests split by the persistence API they are for (JDO, JPA, REST, etc).

<a name="tools"/>
### GitHub : Tools

The GitHub DataNucleus project also provides some tools to help in using DataNucleus. The repositories providing tools are

[datanucleus-maven-plugin](http://github.com/datanucleus/datanucleus-maven-plugin)  
[datanucleus-eclipse-plugin](http://github.com/datanucleus/datanucleus-eclipse-plugin)  
[datanucleus-idea-plugin](http://github.com/datanucleus/datanucleus-idea-plugin)

Like with all plugins, the tools are independently versioned since they have their own lifecycle.

<a name="documentation"/>
### GitHub : Documentation

The GitHub DataNucleus project also provides the documentation for DataNucleus.

#### Documentation : datanucleus.org Project Site

DataNucleus has a main site __datanucleus.org__ for the overall project and the commercial services that we offer. 
This site makes use of a "skin" responsible for adding header/footer to all docs as well as the dropdown menus.
This "skin" is available in GitHub in the repository [docs-datanucleus-skin](https://github.com/datanucleus/docs-datanucleus-skin).
Now you need to build/install the skin, by typing

	mvn clean install

The documentation is in GitHub in repository [docs-datanucleus](https://github.com/datanucleus/docs-datanucleus)
Now you can build the site itself by typing

	mvn clean site

The site is then available under _target/site_. The documentation is also generated every night from what is in GitHub, 
and this appears on the website.

#### Documentation : AccessPlatform Product Site

The documentation for AccessPlatform uses the same Maven process, and also has its own "skin".
This "skin" is available in GitHub in repository [docs-accessplatform-skin](https://github.com/datanucleus/docs-accessplatform-skin).
Now you need to build/install the skin, by typing

	mvn clean install

The documentation is in GitHub in repository [docs-accessplatform](https://github.com/datanucleus/docs-accessplatform).
Now you can build the site itself by typing

	mvn clean site

The site is generated under _target/site_. You can also build a PDF of the docs by typing

	mvn pdf:pdf

The PDF is generated under _target/pdf_. The documentation is also generated every night from what is in GitHub, and this appears on the  website.
