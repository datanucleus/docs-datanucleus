<head><title>Development Process</title></head>

# Section : [Documentation](../index.html) > Development

## DataNucleus Development Process

DataNucleus is open source, released under the Apache 2 license. As a result you are welcome to develop it further. 
We require assistance on many areas of the project should you be interested. A few selected areas where work is needed are

* Development of API (JPA/JDO/REST) features
* Support for improved persistence to existing datastores (e.g Excel, LDAP, XML)
* Support for persistence to new datastores (e.g Cassandra)
* Development of DataNucleus tooling (Eclipse plugin, IDEA plugin, JRebel plugin etc)
* Performance improvements
* Documenting the DataNucleus system (including samples/tutorials)

If you are interested, please go to the [DataNucleus Forum](http://forum.datanucleus.org/) and raise a thread in the 
[Volunteers forum](http://www.datanucleus.org/servlet/forum/listthreads?forum=21) forum. 
__Please make sure that you have time to spend on DataNucleus development__ before volunteering as this would only waste our time otherwise; we're not 
interested if you only have a week or so and then disappear off onto something else. There are many interesting parts of the system to work on so 
this is your chance to get aboard the project; and demonstrating to an employer an involvement in an open source project can be beneficial
to your career.

DataNucleus uses Test Driven Development (TDD). It has [many test suites available](tests.html) and all should be run to provide stability in the codebase.

When you have DataNucleus commit rights (see [this forum thread](http://www.datanucleus.org/servlet/forum/viewthread_thread,75)), the 
development process should be as below. Please abide by these simple rules

1. Identify [an issue](http://issues.datanucleus.org) to work on. Raise a JIRA issue if it doesn't yet exist, and allocate to yourself
2. Develop code, unit tests (as appropriate), and documentation for the issue. DataNucleus is developed using JDK1.6+.
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

Coding standards are more complicated to define so please look [here](coding_standards.html) for details.


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
(e.g datanucleus-core-3.2.11). Developers shouldn't have any need for adding other tags.


<a name="versioning"/>
### Versioning

There are many different versioning systems in use by software. All typically use _major.minor.revision_ 
(occasionally with finer grain below that). Some use suffix _alpha_ or _beta_ to reflect how close the software is to full release. 
Some use versioning starting at say 1.0.0, and going up from that until some release e.g 1.0.4 that is considered the full release. 
__DataNucleus uses the following versioning policy__

* When we start a release lifecycle for a product it starts at 1.0 Milestone 1 (1.0.0.M1)
* Subsequent releases increment the milestone ... 1.0.0.M2, 1.0.0.M3 etc
* When we feel we are close to a full release we can optionally have 1.0 Release Candidate 1 (1.0.0.RC1)
* We have as many release candidates as necessary to get everything feature complete
* The full release is 1.0.0(.Release)
* Any subsequent releases in that lifecycle increment the revision number, so 1.0.1, 1.0.2 etc

The use of "Milestone" rather than "alpha" or "beta" is because all DataNucleus releases are run against all unit tests 
and TCKs and so stability is typically inherent.

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

DataNucleus originated as JPOX in 2003 and consequently many people have contributed to its development over the years, 
and has been open source since the outset. In terms of metrics of the codebase you can get a measure of this by looking
at the [DataNucleus page on Ohloh](http://www.ohloh.net/projects/datanucleus).
