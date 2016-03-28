<head><title>Development Process</title></head>

# Section : [Documentation](../index.html) > Development

DataNucleus is an Open Source development. It is written by many people yet has a broad scope and so is in need of help. 
It is released under an Apache 2 license, so you are welcome to develop it further.
Since the software is free, you are benefiting from this work. You have a duty to contribute to the project, particularly if/when you have problems.
It should be noted that many people use open source software without the minor intention of contributing anything back to it; 
that's ok but then should everyone adopt that attitude then things will not get improved, and additionally those people are not in a position to
request/expect any improvements that they would like to see (without putting something back in).

__You can help the project in many ways__. Here are some examples

* __Answer questions on the [Forum](http://forum.datanucleus.org)__. New users need to learn somewhere just like you did when you first used DataNucleus.
You could monitor the forum when you have free time and attempt to answer people's questions. People will appreciate it even if you don't know all of the answers.
* __Debug problems in the code__ before reporting them on the Forum. You can isolate the issue to a particular area of code even if you don't know the solution, 
and post your findings on the Forum for one of the developers to pick up and progress further. __Better still, contribute updates__ so it saves our time in working 
out where the problem lies. These will be much more valuable to us. Since we use Git for source code repository the best way is to FORK/CLONE a particular 
GitHub project and submit a GitHub PULL REQUEST with your changes. Please see the [DataNucleus coding standards](sourcecode.html#Coding_Standards).
* __Volunteer to be a developer__ of DataNucleus. To do this you need to start off by contributing patches for issues, and demonstrate your commitment to the project.
Once you've done this for a while then we'll invite you to join the project. You then go to the "Recruitment" section of our Forum and post the developer agreement
(stored in one of the threads in that Forum). Thereafter you can push DataNucleus further yourself when you have time. Be aware though that once you have been given
commit rights, inactivity for a period of time (e.g 6 months or more) will mean that you can lose these rights. Being a committer implies responsibility. 
You could volunteer to work on a particular part of DataNucleus (e.g RDBMS) or all of it, up to you.
* __[Donate to the project](../donations.html)__. This will help to fund the time of one of the main developers and will mean that DataNucleus functionality 
will be expanded faster due to your help.
* __Contribute documentation or worked examples__ that can be included in the online documentation. If you think there is something missing from our documents 
then you can write it and contribute it and others will benefit from your work just like you have benefited from our DataNucleus product. The easiest way to
contribute is to FORK/CLONE the appropriate GitHub project and then raise a GitHub PULL REQUEST and we will process it asap. You can also contribute via either the 
[Forum](http://forum.datanucleus.org) or by raising an issue in [JIRA](http://issues.datanucleus.org).

Note that involvement in an open source project can significantly improve your employability, since potential employers can see the quality of your code, so this
is an opportunity to do something positive. Note also __if you contribute to the system in some way then we are more likely to answer your forum questions, or listen to your ideas, 
so it's in your interests to participate__. We hope that the above has given you some idea how your time can be used to benefit the common goal of having a quality 
Java persistence solution free for all to use.


## DataNucleus Development Process

DataNucleus uses Test Driven Development (TDD). It has [many test suites available](tests.html) and all should be run to provide stability in the codebase.

When you have DataNucleus commit rights (see [this forum thread](http://www.datanucleus.org/servlet/forum/viewthread_thread,75)), the 
development process should be as below. Please abide by these simple rules

1. Identify [an issue](http://issues.datanucleus.org) to work on. Raise a JIRA issue if it doesn't yet exist, and allocate to yourself
2. Develop code, unit tests (as appropriate), and documentation for the issue. DataNucleus is developed using JDK1.8+ (DataNucleus 3.x is developed with JDK1.7+).
3. Run all DataNucleus tests and the (public) JDO TCK, and when all pass to the same level as before then you can check your code into GitHub. 
__Broken unit tests or JDO TCK tests must be fixed ASAP__. Others are using GitHub latest too and if you break either the build or the tests 
then it means they often cannot work effectively. __Breakage of unit tests or JDO TCK tests mean that your changes can be rolled back__.
4. Issues that involve many changes should be split, where appropriate, into smaller steps so that you can still pass point 3 above with each check in
5. Where changes are significant and you cannot split them into smaller check-ins (that pass the tests) should be checked in to your own GitHub branch 
and when complete they should be merged into GitHub 'master'. If help is needed at this point then other developers should help in merging large changes.
6. All check-ins should have a prefix in the description like _[NUCCORE-23]_ for the issue being worked on. Then they will be indexed by JIRA and so we can track changes.
7. Mark the JIRA issue as "Resolved" for the next release.


<a name="codingstandards"/>
### Coding Standards

Coding standards are more complicated to define so please look [here](sourcecode.html#Coding_Standards) for details.


<a name="mailinglists"/>
### Mailing Lists

DataNucleus has the following mailing lists to aid in tracking development. They are read-only.

* [datanucleus-issues](https://lists.sourceforge.net/lists/listinfo/datanucleus-issues) showing all changes in JIRA issues for the project
* [datanucleus-nightlybuilds](https://lists.sourceforge.net/lists/listinfo/datanucleus-nightlybuilds) showing the result of nightly builds (one mail per day)

In addition you can subscribe to commits for a particular repository on GitHub should you have interest in a plugin.


<a name="licensing"/>
### Licensing

All contributions to the DataNucleus project must adhere to the Apache 2 license. Notwithstanding that, at the discretion of the administrators of the project, 
DataNucleus project downloads may include separately licensed code from third parties as a convenience and where permitted by the third party license, 
provided this is clearly indicated.


### Branching

As a general rule, we branch when we're at a point of changing internal/external DataNucleus APIs of a plugin. So, for example, we're developing
_datanucleus-core_ and want to change some API. The process is as follows

1. Create branch with name "{version}" where the _version_ is the version that is stored in that branch (so the current version).
2. Update _pom.xml_ of __master__ branch to the next version number (so if we have just created a branch for 3.2 then this will be 3.3.0-SNAPSHOT).

If you are developing a new feature then you can optionally develop it in its own branch, so choose a branch name that is _not a version_ (so doesn't
conflict with the naming convention above). When you have fully implemented the feature and merged it into master and it is fully tested then you
should delete the old branch.


### Tagging

Tagging is performed when we release a plugin, and the Maven _release_ plugin automatically creates tags with names of `{artifact_id}_{version}`
(e.g datanucleus-core-3.2.11). Developers shouldn't have any need for adding other _tags_.


<a name="versioning"/>
### Versioning

There are many different versioning systems in use by software. All typically use _major.minor.revision_ 
(occasionally with finer grain below that). Some use suffix _alpha_ or _beta_ to reflect how close the software is to full release. 
Some use versioning starting at say 1.0.0, and going up from that until some release e.g 1.0.4 that is considered the full release. 
__DataNucleus uses the following versioning policy__

* When we start a release lifecycle for a product it starts typically at __Milestone__ 1 (e.g 1.0.0.M1). 
If we are developing a new plugin that will be used from DataNucleus v5.0 then we will start at 5.0 Milestone 1 (5.0.0.M1) for the new plugin.
* Subsequent releases increment the milestone ... e.g 1.0.0.M2, 1.0.0.M3 etc
* When we feel we are close to a full release we can optionally have __Release Candidate__ (e.g 1.0.0.RC1)
* We have as many release candidates as necessary to get everything feature complete
* The full release is __Release__ (e.g 1.0.0.Release)
* Any subsequent releases (after the full release) in that lifecycle increment the revision number, e.g 1.0.1, 1.0.2 etc

The use of "Milestone" rather than "alpha" or "beta" is because all DataNucleus releases are run against all unit tests and TCKs and so stability is typically inherent.

We increment the <i>minor</i> version number when we are changing internal APIs (but not client facing APIs).
We increment the <i>major</i> version number when we are changing external (client-facing) APIs.


<a name="productrelease"/>
### Product Release Process

DataNucleus AccessPlatform is simply a bundled distribution and is typically released at intervals every 1-2 months, usually taking the 
latest release of each related plugin and packaging it. When there is a DataNucleus product to be released (e.g AccessPlatform), the following is 
the release process (administrator role)

* Make sure that all required plugin versions are released. See the [plugin release process](#pluginrelease) below for details.
* Go to the product that needs releasing update _build.properties_ so that versions of all required plugins are set, and the 
version of the product is set. Check this change in.
* Generate the required product archives (zips), and the documentation.
* Release the archives and documentation on SourceForge


<a name="pluginrelease"/>
### Plugin Release Process

Since DataNucleus development policy is that all current tests should always pass for checked in code then a plugin is
always in a releasable state. In general changes don't sit in the source repo for more than a month without release.
If a commercial client requires a particular feature or bug fix then a release is expedited. If some upstream plugin
needs releasing first then it is released before the plugin in question. We try to avoid any changes in internal APIs
that would affect downstream plugins if not in a new release cycle. The following is the release process (administrator role)

* Check that there are no unresolved issues in JIRA marked against the release version in question and, if necessary complete 
the outstanding ones, or move them to a later version.
* Should a developer have a good reason for the release not happening (e.g wanting to get another fix in first) then the 
release could be delayed, but this is the exception not the norm.
* Use the Maven _release_ plugin as follows : _mvn clean release:clean release:prepare release:perform_. This updates the 
version to remove SNAPSHOT, builds source/javadocs/jar, creates a tag and finally copies it to Sonatype ready for release.
* Go to the DataNucleus Sonatype account and check/release/close the repository artifacts)


<a name="samplerelease"/>
### Sample Release Process

We try to make all samples use Maven and have the same release process, so then the released archive is consistent.
This is the release process for a sample

* Go to samples project and edit the pom.xml for version and dependencies
* Create the assembly using _mvn clean assembly:assembly_
* Copy the zip file on to SourceForge (or get an admin to do it)


### Metrics

DataNucleus originated as JPOX in 2003, becoming DataNucleus in 2008, and consequently many people have contributed to its development over the years and has been open source since the outset. 
In terms of metrics of the codebase you can get a measure of this by looking at the [DataNucleus page on OpenHub](http://www.openhub.net/p/datanucleus).


## Development Team

The management and direction of DataNucleus is provided by a small team of experienced individuals.

__Andy Jefferson__ : Founder of the DataNucleus project. Has worked on the project since its initiation as JPOX in 2003, and has worked on all plugins. 
Initiated the support for db4o, ODF, MongoDB, NeoDatis, Neo4j, OOXML, Cassandra, javax.cache, RDBMS connection pools, and much more. 
Also contributed to version 2 of the plugin for GAE/Datastore, subject to the constraints that Google put on it.

__Renato Garcia__ : worked on the migration to GitHub, test suite flexibility, auto-generation of MANIFESTs, Jenkins/Solar automation, and some more.

__Baris Ergun__ : Took over responsibility for the geospatial plugin. _Currently inactive_

__Erik Bengtson__ : Founder of the DataNucleus project. Worked on the project since its initiation
as JPOX in 2003, until around 2011. Initiated support for Excel, XML, JSON and HBase. _Currently inactive_

__Stefan Seelmann__ : Wrote the vast majority of the LDAP plugin. _Currently inactive_

__Thomas Marti__ : Wrote an amount of the spatial plugin (now renamed to _geospatial_). _Currently inactive_

__Stefan Schmid__ : Wrote an amount of the spatial plugin (now renamed to _geospatial_). _Currently inactive_

__Joerg von Frantzius__ : worked on the test suite, and RDBMS areas. _Currently inactive_


In addition to those above, other people have contributed to varying degrees in the development of this software or documentation.

DataNucleus tackles a wide range of problem areas - are you interested in contributing to the DataNucleus project and want to get involved? 
The best way is to become part of the DataNucleus community and start by contributing patches. From that, gain commit rights. Where you take the project to from there is up to you.
