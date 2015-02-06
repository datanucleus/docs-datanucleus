<head><title>Usage</title></head>

# Section : [Documentation](index.html) 

## Why Use DataNucleus ?

Choosing a Java data management platform will come down to your requirements in terms of cost, functionality, support, etc.

* __DataNucleus is Open Source__, meaning that you have full access to the source code for all versions of DataNucleus. 
With this you have the capability to correct any errors that you encounter, but also better understand the data management process, 
and you can potentially extend DataNucleus to suit your needs.
* __DataNucleus is free__. Our license is the [Apache 2 License](license.html), providing the code and executables (JARs) free of charge. 
You are free to use DataNucleus in your projects. Please refer to the license for the precise wording. DataNucleus will always remain
Open Source. Our license (Apache 2) is very flexible, much more than the license used for some other notable object/relational mapping 
software which use licenses like the LGPL.
* __DataNucleus is independent and unstoppable__. The source code is open, and is not owned exclusively by some company. 
As such it cannot be bought by a large organisation such as Versant or Oracle and the product terminated (as has happened to customers 
of Kodo, JDO Genie over the last few years) - do you want that to happen to you? FYI EclipseLink is Oracle-driven, Hibernate is RedHat-driven and
OpenJPA is IBM-driven (__Stop Press : [IBM is stopping working on OpenJPA now](https://developer.ibm.com/wasdev/2014/05/28/eclipselink-jpa-provider-liberty-profile/)__).
* __DataNucleus is standards driven and standards compliant__ implementing all JDO and JPA specifications, providing all 
mandatory items and the majority of optional items as well as providing several value-added extensions. Standards compliance safeguards
your applications future allowing you to swap between implementations.
* __DataNucleus supports data management for many different types of datastores__. These include 
[the vast majority of RDBMS databases on the market today](http://github.com/datanucleus/datanucleus-rdbms),
[MongoDB document store](http://github.com/datanucleus/datanucleus-mongodb),
[Neo4j graph store](http://github.com/datanucleus/datanucleus-neo4j),
[LDAP](http://github.com/datanucleus/datanucleus-ldap) and other datastores meaning that if you change your datastore in the future 
you don't need to change your data access layer.
* __DataNucleus provides outstanding performance__ when compared with the competing technologies.
* __DataNucleus does not bring in large numbers of dependencies__ unlike other persistence frameworks (for example, Hibernate) that have 
to provide a zip file just to package all of their requirements up. In fact DataNucleus could be run with just 1 third-party library 
(jdo-api.jar when using JDO, or persistence-api.jar when using JPA) - beat that!
* __DataNucleus is quality-driven__ being developed using a Test Driven Development methodology. We have more than 2000 unit tests that 
are run before any release guaranteeing a stable product. In addition we baseline our capabilities against standard Java TCKs (JDO, JPA)
the definition of specification compliance. In our [issue tracker](http://issues.datanucleus.org) you will not find large numbers of 
outstanding high priority items that you have to workaround (unlike what you find in the Hibernate, OpenJPA, EclipseLink issue trackers for example).
* __DataNucleus provides a level of free support__ by way of an [online Forum](http://forum.datanucleus.org) and also provides 
[commercial support arrangements](http://www.datanucleus.org/support.html#support) if you require it.
* __DataNucleus [consulting](http://www.datanucleus.org/support.html#timebased_consulting)__ can be arranged with the developers of DataNucleus.
* __DataNucleus is open to contributions/donations__ allowing individuals to help out and allowing companies to sponsor features that 
they require for their deployments of DataNucleus.
* __DataNucleus is plugin-driven__ using the OSGi standard mechanism, providing plugins to external caching software (Coherence, EHCache, etc), 
to external database-pooling software (DBCP, C3P0, etc), and much more.


DataNucleus is _not_ part of the Apache project because

* Apache is a loose collection of projects with no general direction or collaboration so DataNucleus would simply be an independent part of an organisation there, hence no benefit.
* DataNucleus infrastructure (website availability, Forum, JIRA, nightly builds, release policy etc) is way in advance of anything that Apache has and moving there would be a step 
backwards in this respect. The Apache website is often unavailable, they only use mailing lists, they don't have a general policy of providing nightly builds, nor has any Apache 
project got a Forum etc etc
* Being part of Apache would not guarantee any more committers as demonstrated by many projects that have moved to Apache (and often ended up in the Apache 'attic').




## Used By

DataNucleus is used by many companies and groups in their own software. Below are a short subset of those publicisable.

<table>
<tr>
<td width="33%"><a href="http://code.google.com/appengine/" target="_blank"><img src="../images/usage/appengine.gif" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.vmforce.com/" target="_blank"><img src="../images/usage/vmforce.png" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.redbooks.ibm.com/abstracts/REDP4512.html?Open" target="_blank"><img src="../images/usage/tivoli.gif" border="0" alt=""/></a></td>
</tr>

<tr>
<td width="33%"><a href="http://www.yahoo.com" target="_blank"><img src="../images/companies/yahoo.gif" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.romaframework.org" target="_blank"><img src="../images/usage/roma.jpg" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.projectocolibri.com/" target="_blank"><img src="../images/usage/colibri.jpg" border="0" alt=""/></a></td>
</tr>

<tr>
<td width="33%"><a href="http://www.jfire.org" target="_blank"><img src="../images/usage/jfire.png" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.metamicro.com" target="_blank"><img src="http://www.datanucleus.com/images/companies/metamicro.jpg" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.travelmuse.com" target="_blank"><img src="http://www.datanucleus.org/images/companies/travelmuse.png" border="0" alt=""/></a></td>
</tr>

<tr>
<td width="33%"><a href="http://www.hp.com" target="_blank"><img src="http://www.datanucleus.org/images/companies/hp.jpg" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.livestream.com" target="_blank"><img src="http://www.datanucleus.org/images/companies/livestream.jpg" border="0" alt=""/></a></td>
<td width="33%"><a href="http://ge.geglobalresearch.com/" target="_blank"><img src="http://www.datanucleus.org/images/companies/ge.png" border="0" alt=""/></a></td>
</tr>

<tr>
<td width="33%"><a href="http://www.stepaheadsoftware.com" target="_blank"><img src="../images/companies/stepahead.gif" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.ridgetop-group.com/" target="_blank"><img src="../images/companies/ridgetop.jpg" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.seismicexchange.com/" target="_blank"><img src="../images/companies/seismicexchange.gif" border="0" alt=""/></a></td>
</tr>

<tr>
<td width="33%"><a href="http://hive.apache.org/" target="_blank"><img src="../images/companies/apache_hive.jpg" border="0" alt=""/></a></td>
<td width="33%"><a href="http://isis.apache.org/" target="_blank"><img src="../images/companies/apache_isis.png" border="0" alt=""/></a></td>
<td width="33%"><a href="http://www.bmc.com" target="_blank"><img src="../images/companies/bmc.gif" border="0" alt=""/></a></td>
</tr>

<tr>
<td width="33%"><a href="http://www.lockheedmartin.com/" target="_blank"><img src="../images/companies/lockheed.png" border="0" alt=""/></a></td>
</tr>
</table>

## Publicise Your Usage

Have you benefited from DataNucleus and want to publicise your use of it ? You can do this in two ways

### Write a Testimonial

Why not write a short testimonal of your usage of DataNucleus. Maybe start by explaining the problem and what you needed to do. 
Then explain how DataNucleus addresses what you need, and how you solved any problems that came up. You don't need to go into
great detail. Then please contact us at __info [AT] datanucleus [DOT] org__


### Website links

You can also help by putting one of our logos on your site with a link back to our website. That way DataNucleus gets publicity and others 
can benefit. This way the project will flourish with only a small effort from you. Below are some logos for your use.
Should you have any particular requirements for logo sizes, please contact us.

### DataNucleus project logos

![Logo1](../images/logos/DataNucleus16-150.jpg)
![Logo2](../images/logos/DataNucleus16-300.jpg)


### DataNucleus AccessPlatform logos

![Logo1](../images/logos/DataNucleus_AccessPlatform_40.jpg)
![Logo2](../images/logos/DataNucleus_AccessPlatform_85.jpg)
