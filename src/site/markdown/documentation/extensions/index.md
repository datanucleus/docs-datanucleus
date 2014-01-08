<head><title>PluginPoints</title></head>

# Section : [Documentation](../index.html) > Extensions

## DataNucleus Extensions Guide

DataNucleus products are built using a plugin mechanism, allowing plugins to operate together.
This plugin mechanism is useful also from a user viewpoint in that you, the user, could provide
plugins that use these plugin points and extend the capabilities of DataNucleus.
Plugins are loaded by a plugin manager when DataNucleus is initialised at runtime, and this plugin manager uses a 
registry mechanism, inspecting jars in the CLASSPATH. The three steps necessary for creating a DataNucleus plugin are

1. Review the DataNucleus PluginPoint that you will need to implement to generate the plugin, and implement it.
2. Create a file _plugin.xml_ at the top level of your JAR defining the plugin details (see the actual PluginPoint docs).
3. Update the META-INF/MANIFEST.MF file contained in the jar so that it includes necessary information for OSGi.

A minimum _META-INF/MANIFEST.MF_ for a plugin jar should look like this

	Manifest-Version: 1.0
	Bundle-ManifestVersion: 2
	Bundle-Name: myplugin
	Bundle-SymbolicName: mydomain.myplugin
	Bundle-Version: 1.0.0
	Bundle-Vendor: My Company</source>

Each plugin extension has attributes. If you want to override an extension that is included in DataNucleus itself then you 
need to specify the __priority__ attribute, setting it to an integer (the default plugin has priority=0, so set to higher than this to override it).
__If you write a DataNucleus plugin and you either want it to be included in the DataNucleus distribution, or want it to be listed here then 
please contact us via the [Forum](http://forum.datanucleus.org)__

The current plugin points are :-

* [Java Types](java_types.html)
* [Type Converters](type_converter.html)
* [Persistence Properties](persistence_properties.html)
* [Store Manager](store_manager.html)
* [Connection Factory](connection_factory.html)
* [AutoStart Mechanisms](autostart_mechanism.html)
* [ClassLoader Resolvers](classloader_resolver.html)
* [Datastore Identity](datastoreidentity.html)
* [Identity String Translator](identity_string_translator.html)
* [Identity Key Translator](identity_key_translator.html)
* RDBMS PluginPoints
	+ [Java Type Mapping](rdbms_java_types.html)
	+ [Datastore Mapping](rdbms_datastore_types.html)
	+ [Datastore Adapter](rdbms_datastore_adapter.html)
	+ [Connection Pool](rdbms_connection_pool.html)
	+ [Connection Provider](rdbms_connection_provider.html)
	+ [Identifier Factory](rdbms_identifier_factory.html)
	+ [SQL Methods](rdbms_sql_methods.html)
	+ [SQL Expressions](rdbms_sql_expressions.html)
	+ [SQL Operations](rdbms_sql_operations.html)
	+ [SQL Table Namer](rdbms_sql_table_namer.html)
* [Annotations](annotations.html)
* [Class Annotation Handler](class_annotation_handler.html)
* [Member Annotation Handler](member_annotation_handler.html)
* [XML MetaData Handler](metadata_handler.html)
* [XML MetaData Entity Resolver](metadata_entityresolver.html)
* [Value Generator](value_generator.html)
* [Level 1 Cache](level1_cache.html)
* [Level 2 Cache](level2_cache.html)
* [Query Cache](query_cache.html)
* [Query Language](store_query_query.html)
* [Query Methods](store_query_methods.html)
* [JMX Management](management_server.html)
* [JTA Locator](jta_locator.html)


### Plugins in a Non-managed environment

Non-managed environment is a runtime environment where DataNucleus runs and plug-ins are not 
managed by a container. In this environment the plug-in discovery and lifecycle is managed by DataNucleus.

There is a 1 to N instance relationship from DataNucleus to a plug-in per PMF. More exactly, if only 
one PMF exists, there is only one Plug-in instance for a Connection Pool Plug-in, and if "N" 
PMF exist, there are "N" Plug-in instances for a Connection Pool Plug-in.

JavaSE and JavaEE runtimes are considered <i>non-managed</i> environments.
In non managed environments there is no lifecycle itself of plug-ins. Extensions implemented by 
plug-ins are instantiated on demand and terminated on PMF/EMF closing, PM/EM closing or in another 
form depending in what the extension is used for.

### Plugins in a Managed environment

Managed environment is a runtime environment where DataNucleus plug-ins are managed by a container. 
The discovery, registry and lifecycle of plug-ins are controlled by the container. 
There is no plug-in instance relationship from DataNucleus to a plug-in regarding PMF instances. In 
managed environments, there is only one plug-in instance for one or "N" PMFs. Again, this is managed by the container.

DataNucleus supports OSGi containers as managed environment. In OSGi managed environments plug-in lifecycle is determined by 
the OSGi specification. Once activated, a plug-in is only stopped when the OSGi container finishes its execution, or the 
plug-in is stopped by an OSGi command.

### Extensions and Plugins

A plugin owns an Extension. The behaviour is defined below :-

* __Lifecycle__ : Each extension is created by a segment of code during the runtime execution, and destroyed/released 
whenever they are no longer needed. This has no influence with the plug-in lifecycle.
* __Manageability__ : In non managed environments, the plug-ins are managed by DataNucleus and maintained with a composition 
relation to the PMF instance. This allows a plug-in "instance" per PMF. If multiple PMFs are created multiple extensions for an 
extension point are instantiated. In managed environments, more precisely in OSGi containers, the plug-ins are managed by the 
OSGi framework. Each plug-in will mostly be a singleton inside the OSGi container.
* __Registration__ : In non managed environments all plugins are registered using an instance of JDOClassLoaderResolver 
(so using the current ClassLoader of the PMF and the current thread). This means that the /plugin.xml and /META-INF/MANIFEST.MF files 
must be accessible to the classloader. In managed environment this is handled by the container.
* __ClassLoading__ : The classloading in non managed environments is usually made of one  single ClassLoader, while in managed 
environments each plug-in has it's own ClassLoader.
* __Configuration__ : Some Extensions needs to retrieve a configuration that was set in the PMF. This means that Plug-ins should 
not hold singleton / static configurations if they want to serve to multiple PMFs at the same time.
* __Constructors/Methods__ : In order of having consistent and avoid changes to extension-point interfaces, the Extension 
Constructors or Methods (either one) should have receive a PMFContext instance as argument. If by the time the Extension Point is designed 
clearly there is usage for a PMFContext, then the Extension-Point does not need to take the PMFContext as argument, but keep in mind that 
a 3rd Extension may need one due to different reasons.
* __Instantiation__ : Inside the DataNucleus Core, regardless if the runtime is OSGi managed or non managed, extension instances are 
created per PMF. DataNucleus Extensions should always be created through a PluginManager, regardless if the managed environment 
would allow you to instantiate using their own interfaces. This allows DataNucleus and its Plug-ins to run in non managed environments.
