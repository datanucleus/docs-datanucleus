<head><title>Source Code (SourceForge)</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## DataNucleus Source Code : Legacy Subversion Repository

__Note that source code for all versions after 3.3.5 is stored in [GitHub](sourcecode.html).__

DataNucleus used [Subversion (SVN)](http://subversion.tigris.org/) for housing source code for all versions __up to and including 3.3.5__. 
The legacy DataNucleus SVN repository is hosted by [SourceForge](http://www.sf.net/projects/datanucleus/).
__Note that this repository will not be updated with fixes etc now. You should use GitHub for that.__
You can check out from the SourceForge SVN repository using

	Read-Only :   svn checkout svn://svn.code.sf.net/p/datanucleus/code/ datanucleus-code

	Read-Write (committers) :   svn checkout --username={your-sf-login} svn+ssh://{your-sf-login}@svn.code.sf.net/p/datanucleus/code/ datanucleus-code

__Please note that this will check out ALL code and ALL branches!__ What would be better is to check out "trunk" of all plugins 
that you are interested in (see below). For example the following will just check out "core" and "api.jpa" plugins.

	svn checkout svn://svn.code.sf.net/p/datanucleus/code/platform/core/trunk datanucleus-core
	svn checkout svn://svn.code.sf.net/p/datanucleus/code/platform/api.jpa/trunk datanucleus-api-jpa

The SVN repository is also [browseable online](https://sourceforge.net/p/datanucleus/code/HEAD/tree/)
At the top level you will find

	platform/       <- Products and plugins
	test/           <- End-to-end testing
	tools/          <- Add on tools (Maven, Eclipse etc)
	documentation/  <- Docs
	samples/        <- Samples, tutorials etc

### Legacy Subversion : Platform

The "platform" directory contains all source code for the plugins comprising the different DataNucleus products. They are laid
out as follows. Please note that not all plugins are included here, this is simply to give an idea of the layout.

	platform/
	    core/                      <- "Core" plugin, the basis for all datastore access
	        trunk/
	        branches/
	    api.jdo/                   <- JDO API plugin
	        trunk/
	        branches/
	    api.jpa/                   <- JPA API plugin
	        trunk/
	        branches/
	    api.rest/                  <- REST API plugin
	        trunk/
	        branches/
	    store.neo4j/               <- Neo4j datastore plugin
	        trunk/
	        branches/
	    store.excel/               <- Excel datastore plugin
	        trunk/
	        branches/
	    store.odf/                 <- ODF datastore plugin
	        trunk/
	        branches/
	    store.json/                <- JSON datastore plugin
	        trunk/
	        branches/
	    store.ldap/                <- LDAP datastore plugin
	        trunk/
	        branches/
	    store.neodatis/            <- NeoDatis ODB datastore plugin
	        trunk/
	        branches/
	    store.xml/                 <- XML datastore plugin
	        trunk/
	        branches/
	    store.rdbms/               <- RDBMS datastore plugin
	        trunk/
	        branches/
	    store.types.spatial/       <- Spatial types plugin
	        trunk/
	        branches/
	    cache/                     <- Level 2 caching plugin
	        trunk/
	        branches/
	    jdo.connector/             <- JCA adaptor for JDO
	        trunk/
	 	    branches/
	    accessplatform/            <- AccessPlatform "product" bundle process
	        trunk/
	        branches/
	    local.repository/          <- Repository (in Maven1 layout) with all dependencies (for use when developing under Eclipse)
	        trunk/

All plugins are independently versioned (trunk is the latest, and branches are stored under the branches directory). 
This is because they have their own lifecycle, and plugins are bundled together into the "products" (AccessPlatform, etc). 
So we could have AccessPlatform using version X of a plugin, and some other product developing version Y of that plugin because 
it needs some new functionality.

### Legacy Subversion : Tests

The End-to-End test section is laid out as follows

	test/
	    accessplatform/
	        trunk/
	            test.jdo.general/
	            test.jdo.application/
	            test.jdo.datastore/
	            test.jpa.general/
	            ...
	        branches/

So we have separated tests for "AccessPlatform" from other products and we branch <i>all</i> tests for each product.

### Legacy Subversion : Tools

The tools section contains anything that aids third party software operate with DataNucleus. It is laid out like this


	tools/
	    ide.eclipse/
	        trunk/
	        branches/
	    maven2/
	        trunk/
	        branches/

Like with all plugins, the tools are independently versioned since they have their own lifecycle.

### Legacy Subversion : Documentation

Finally the documentation area in Subversion is as follows

	documentation/
	    datanucleus.org/
	        trunk/
	        branches/
	    accessplatform/
	        trunk/
	        branches/

So we have a main website ("datanucleus.org"), and a website for each product.
