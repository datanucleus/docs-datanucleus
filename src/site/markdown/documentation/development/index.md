<head><title>Development</title></head>

# Section : [Documentation](../index.html) > Development

## DataNucleus Development

DataNucleus is open source, released under the Apache 2 license. As a result you are welcome to develop it further. 
We require assistance on many areas of the project should you be interested. A few selected areas where work is needed are

* Development of JPA/JDO features
* Support for improved persistence to existing datastores (e.g Excel, LDAP, XML)
* Support for persistence to new datastores (e.g Cassandra)
* Development of DataNucleus tooling (Eclipse plugin, Maven plugin etc)
* Performance improvements
* Documenting the DataNucleus system

If you are interested, please go to the [DataNucleus Forum](http://forum.datanucleus.org/) and raise a thread in the __General Development__ forum. 
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
4. __Broken unit tests or JDO TCK tests must be fixed ASAP__. Others are using GitHub latest too and if you break either the build or the tests 
then it means they often cannot work effectively. __Breakage of unit tests or JDO TCK tests mean that your changes can be rolled back__.
5. Issues that involve many changes should be split, where appropriate, into smaller steps so that you can still pass point 3 above with each check in
6. Where changes are significant and you cannot split them into smaller check-ins (that pass the tests) should be checked in to your own GitHub branch 
and when complete they should be merged into GitHub 'master'. If help is needed at this point then other developers should help in merging large changes.
7. All check-ins should have a prefix in the description like _[NUCCORE-23]_ for the issue being worked on. Then they will be indexed by JIRA and so we can track changes.
8. Mark the JIRA issue as "Resolved" for the next release.

<a name="licensing"/>
### Licensing

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


The original contributor is the one who contributes the first version of the file. A contributor may be a person or an organisation - whoever 
owns the copyright. If the contributor is an organisation, the person may also be indicated. For each additional contributor, indicate the 
part of the code or contribution that came from the contributor, especially if it contains an interesting algorithm or data table etc. 
For clarity, also indicate the contributor in the actual section of contributed code. Also reference the JIRA ID if applicable. 
The basic principle is to clearly identify the contribution... especially if it is a separable block of code.

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

<a name="codingstandards"/>
### Coding Standards

Coding standards are more complicated to define so please look [here](coding_standards.html) for details.

<a name="mailinglists"/>
### Mailing Lists

DataNucleus has the following mailing lists to aid in tracking development. They are read-only.

* [datanucleus-issues](https://lists.sourceforge.net/lists/listinfo/datanucleus-issues) showing all changes in JIRA issues for the project
* [datanucleus-nightlybuilds](https://lists.sourceforge.net/lists/listinfo/datanucleus-nightlybuilds) showing the result of nightly builds (one mail per day)


In addition you can subscribe to commits for a particular repository on GitHub should you have interest in a plugin.


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
