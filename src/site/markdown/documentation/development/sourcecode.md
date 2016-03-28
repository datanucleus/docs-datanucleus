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

DataNucleus can be easily developed using Maven, Eclipse (plus m2e plugin),  or other IDEs (let us know if you write docs for how to develop DataNucleus with a different IDE).
You require __JDK1.8+__, a __Git client__ (to download/commit DataNucleus Git-based projects) and __an editor__.

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
[datanucleus-java8](https://github.com/datanucleus/datanucleus-java8)  

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



## Coding Standards

Here we provide an overview of the coding standards employed in DataNucleus source code.
__If you want to work on DataNucleus or contribute code to DataNucleus you are expected to use these coding standards. 
We know everyone has their own preference but these are ours so you follow them or any contributed code will not be directly included as is__.
They may differ from Oracle's coding conventions but then those are the conventions of some US company and that doesn't 
mean that they are necessarily "the best", "the official" or any such title. These are ours, so best get used to it ;-).

* __Indentation__ : 4 characters indent
* __Tabs__ : no tabs please!
* __Braces__ : insert a new line before opening brace and a new line before closing brace. Opening and closing braces should line up vertically.
* __Line Length__ : max line length 140
* __Imports__ : fully specify imports. Do NOT use asterisk notation!
* __Java Language Level__ : write for JDK1.7 as a minimum. Anything that requires Java 1.8 should go in the <i>datanucleus-java8</i> plugin. The test suite can use Java 1.8 code.
* __Fields positioning__ : place fields at the top of a class.
* __Logging__ : use _org.datanucleus.util.NucleusLogger_ which wraps Log4j, java.util.logging etc. Log as much info as is considered necessary at the appropriate level.
See [org.datanucleus.util.NucleusLogger](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/util/NucleusLogger.html) for details
* __Localisation__ : all output exception and log messages should be localised. 
See [org.datanucleus.util.Localiser](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/util/Localiser.html) for details
* __Licensing__ : make sure you include the [standard DataNucleus/Apache 2 license copyright header](#Licensing) to all files


If you are using Eclipse then we have an [XML Configuration](code-conventions-eclipse.xml) to specify in Eclipse.

### Examples

Example of brace policy and other things

	package mypackage;

	import java.util.LinkedList;

	public class MyIntStack
	{
	    private final LinkedList fStack;
	
	    public MyIntStack()
	    {
	        fStack = new LinkedList();
	    }
	
	    public int pop()
	    {
	        return ((Integer) fStack.removeFirst()).intValue();
	    }
	
	    public void push(int elem)
	    {
	        fStack.addFirst(new Integer(elem));
	    }
	
	    public boolean isEmpty()
	    {
	        return fStack.isEmpty();
	    }
	}

Example of indentation

	class Example
	{
	    int[] myArray = {1, 2, 3, 4, 5, 6};
	    int theInt = 1;
	    String someString = "Hello";
	    double aDouble = 3.0;
	
	    void foo(int a, int b, int c, int d, int e, int f)
	    {
	        switch (a)
	        {
	            case 0 :
	                Other.doFoo();
	                break;
	            default :
	                Other.doBaz();
	        }
	    }
	
	    void bar(List v)
	    {
	        for (int i = 0; i &lt; 10; i++)
	        {
	            v.add(new Integer(i));
	        }
	    }
	}

Example with if ... else

	class Example
	{
	    void bar()
	    {
	        do
	        {
	        }
	        while (true);
	        try
	        {
	        }
	        catch (Exception e)
	        {
	        }
	    }

	    void foo2()
	    {
	        if (true)
	        {
	            return;
	        }
	        if (true)
	        {
	            return;
	        }
	        else if (false)
	        {
	            return;
	        }
	        else
	        {
	            return;
	        }
	    }

	    void foo(int state)
	    {
	        if (true)
	        {
	            return;
	        }
	        if (true)
	        {
	            return;
	        }
	        else if (false)
	        {
	            return;
	        }
	        else
	        {
	            return;
	        }
	    }
	}

## Licensing

All contributions to the DataNucleus Project must adhere to the Apache 2 license. Notwithstanding the above, at the discretion of the PMC, 
DataNucleus Project downloads may include separately licensed code from third parties as a convenience and where permitted by the third party license, 
provided this is clearly indicated.

All contributions must contain the following copyright notice.

	/**********************************************************************
	Copyright (c) 2006 {your name} and others. All rights reserved.
	Licensed under the Apache License, Version 2.0 (the "License");
	you may not use this file except in compliance with the License.
	You may obtain a copy of the License at
	
	    http://www.apache.org/licenses/LICENSE-2.0
	
	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.
	
	Contributors:
	{year} {contributor1} - {description of contribution}
	{year} {contributor2} - {description of contribution}
	    ...
	**********************************************************************/


## References

In this document we describe just a small set of guidelines. Some references are really worth a read, though our particular guidelines above override some of the things here.

* [Java Code Conventions](http://www.oracle.com/technetwork/java/javase/documentation/codeconvtoc-136057.html)
* [How to write doc comments for Javadoc](http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html)
* [How to write unmaintainable code (what not to do)](http://mindprod.com/jgloss/unmain.html)
* [Scott Ambler Programming Guidelines](http://www.ambysoft.com/essays/codingGuidelines.html)
