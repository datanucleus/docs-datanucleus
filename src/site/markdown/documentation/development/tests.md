<head><title>Tests</title></head>

## DataNucleus : Component Tests

DataNucleus uses JUnit for unit testing. The traditional style of "unit" test are included with the project that 
they are testing. For example "core" has some "unit" tests, and these are run when you build the project. In general
DataNucleus doesn't have many of this style of tests (you're welcome to write some) because the more important aspect
of testing is the actual reading/writing involving the datastore (see below).

## DataNucleus : End-to-End Tests

__End-to-End tests__ also use JUnit, and are available in the GitHub DataNucleus repository [tests](https://github.com/datanucleus/tests).
In these tests we persist objects in a datastore, and test the result. There are several scenarios for this type of test, because JDO/JPA 
have many aspects. By this we mean that we separate our tests into what they test. When developing anything, the tests should be the guiding 
light as to whether you should be checking anything in to GitHub. __If your change breaks things, you shouldn't check things in.__
We have tests divided by the persistence API that they are testing; look under the directories
[jdo](https://github.com/datanucleus/tests/tree/master/jdo), [jpa](https://github.com/datanucleus/tests/tree/master/jpa) and 
[rest](https://github.com/datanucleus/tests/tree/master/rest).

### framework

All DataNucleus end-to-end tests are based around a framework and this requires building first before running any tests. 
Navigate into the [framework](https://github.com/datanucleus/tests/tree/master/framework) directory, and build and install it by typing

	mvn clean install

This builds the jar under "target" and installs it into your Maven repository.


### framework.maven

This is a Maven plugin that allows some of the tests to be run with different configurations. You should build and install it by typing

	mvn clean install

This builds the jar under "target" and installs it into your Maven repository.


### samples

The [samples](https://github.com/datanucleus/tests/tree/master/samples) project provides typical model classes 
to be persisted, with all different types of relations. This project doesn't define _how_ the classes are persisted, 
just what the classes are. They are then usable by all persistence APIs. You should build and install it by typing

	mvn clean install

This builds the jar under "target" and installs it into your Maven repository.


### End-to-End Test Scenarios

So we have now built the _framework_, _framework.maven_ and _samples_ projects and are ready to run any of the "scenarios". 
There are many scenarios including

* Tests for JDO API
	+ __jdo/general__ - General tests for JDO
	+ __jdo/identity__ - Tests for JDO that run with both application and datastore identity types
	+ __jdo/jta__ - Tests for using JTA transactions with JDO
	+ __jdo/geospatial__ - Tests for use spatial types with JDO
	+ __jdo/rdbms__ - Tests specific to RDBMS, using JDO
	+ __jdo/ldap__ - Tests specific to LDAP, using JDO
	+ __jdo/spreadsheet__ - Tests specific to Excel and ODF, using JDO
	+ __jdo/hbase__ - Tests for basic handling with HBase, using JDO
	+ __jdo/mongodb__ - Tests for basic handling with MongoDB, using JDO
* Tests for JPA API
	+ __jpa/general__ - General tests for JPA
	+ __jpa/jta__ - Tests for using JTA transaction with JPA
	+ __jpa/geospatial__ - Tests for using spatial types with JPA
	+ __jpa/rdbms__ - Tests specific to RDBMS, using JPA
* Tests for REST API
	+ __rest/general__ - Tests using the REST API

To run a test scenario, go into the scenario project and type

	mvn clean test

This then runs the tests for that scenario. There are also occasionally additional tests under _org.datanucleus.tests.knownbugs_ and 
_org.datanucleus.tests.newfeatures_ intended for incorporation into the test scenario at some later point; these are not run by default.

__To run the tests on a different datastore (default=H2)__ type

	mvn clean test -Pmysql

or replace "mysql" with "postgresql", "oracle", "mongodb", "hbase" etc

Long term strategy is to just have the overall test scenarios that apply just to JDO or JPA and drop the datastore-specific scenarios 
except where providing some feature specific to that datastore. Reality is that we don't have resource to do this yet, so typically 
run such as _test.jdo.mongodb_ for testing MongoDB, which obviously only tests a small subset of what ought to be tested. 
__Offering your time to make all store plugins more feature complete is the only way this task will be performed.__

<a name="new_unit_test"/>
### Adding Unit Tests

Where you feel that our unit tests do not adequately cover functionality, you should add a test. Please follow the following process

1. Decide which scenario your test fits into (e.g jdo/general, jpa/general)
2. Look at the available model samples and choose one.
3. Write your unit test, extending one of the common base classes, for example __JDOPersistenceTestCase__, or __JPAPersistenceTestCase__
4. Run your test.
5. Raise a JIRA and attach your testcase to the issue


<a name="test_configs"/>
### Alternate Test Configurations

All tests run with a default test configuration (see the files in _framework_ under 
[src/conf](https://github.com/datanucleus/tests/tree/master/framework/src/conf)).
You can, with some test suites, run alternate test configurations. This is achieved using the _framework.maven_ Maven plugin.

1. Look for a configuration file under _src/conf_ of _framework_ such as _optimistic-conf.properties_. These properties are 
used to override the default properties
2. Run the tests with _-Dtest.configs=optimistic_ or _-Dtest.configs=optimistic,pessimistic_ for example


## Databases Notes
<a name="database_notes"/>

### Database setup for running tests

Each test project is run against a datastore (as defined above). The configuration of the datastores is stored under framework 
[src/conf](https://github.com/datanucleus/tests/tree/master/framework/src/conf). Some tests require two database instances, 
which is why for every database there exist two files, e.g. "maven.datanucleus.datastore=hsql" refers to both

* framework/src/conf/datanucleus-hsql.__1__.properties, and
* framework/src/conf/datanucleus-hsql.__2__.properties

The default database configured in the test projects is H2.

Following are notes about running the DataNucleus unit tests with particular databases.

### Oracle 10.2.0

If you face the issue _ORA-12519, TNS:no appropriate service handler_, try increasing the parameters _sessions_ and _processes_ to 300 and 
_open_cursors_ to 1000. To change these values in Oracle, issue the following statements.


	alter system set open_cursors = 1000 scope=spfile
	alter system set sessions = 300 scope=spfile
	alter system set processes = 300 scope=spfile

Refer also to the Oracle spfile (see also _initXE.ora_ or _init.ora_)

	*.processes=300
	*.sessions=300
	*.open_cursors=1000


If you face the issue _ORA-01000: maximum open cursors exceeded_, try increasing the parameter
_open_cursors_ to 1000 in the file _initXE.ora_ or _init.ora_.

	*.open_cursors=1000


If you face OutOfMemory errors, increase the <i>Xms</i> and <i>Xmx</i> JVM args for running the junit tests.
