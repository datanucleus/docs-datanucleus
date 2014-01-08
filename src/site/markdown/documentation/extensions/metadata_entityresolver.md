<head><title>Extensions : MetaData Entity Resolver</title></head>

## Extensions : MetaData Entity Resolver
![Plugin](../../images/nucleus_plugin.gif)

DataNucleus provides a pluggable framework whereby you can plug in your own DTD or XSD schema support.
You can extend DataNucleus's capabilities using the plugin extension <i>org.datanucleus.metadata_entityresolver</i>.

An Entity Resolver extension point configuration is a list of XSDs schemas or DTDs.
For XSD schemas, it needs only the schema location (URL in classpath), since the XML parser will take care of association 
of XML elements and namespaces to the schemas types. For DTDs, it's a little less obvious since DTDs are not namespace aware, so
the configuration must contain the URL location (location in classpath), DTD DOCTYPE (PUBLIC or SYSTEM), and the DTD identity. 

An Entity Resolver has close relationship to the [MetaData Handler](metadata_handler.html) extension point, since
the MetaData Handler uses the Entity Resolvers to validate XML files. However, the Entity Resolvers configured via this plugin
are only applicable to the _org.datanucleus.metadata.xml.PluginEntityResolver_ instances, so the MetaData Handler must
use the _PluginEntityResolver_ Entity Resolver if it wants to use the schemas configured in this extension point. 

### Implementation

The Entity Resolver implementation must extend the _org.datanucleus.util.AbstractXMLEntityResolver_ class and must
have a public constructor that takes the _org.datanucleus.plugin.PluginManager_ class.  


	import org.datanucleus.plugin.PluginManager;
	import org.datanucleus.util.AbstractXMLEntityResolver;
	
	/**
	 * Implementation of an entity resolver for DTD/XSD files.
	 * Handles entity resolution for files configured via plugins.
	 */
	public class PluginEntityResolver extends AbstractXMLEntityResolver
	{
    	public PluginEntityResolver(PluginManager pm)
    	{
			publicIdEntities.put("identity...", "url....");
			...
			systemIdEntities.put("identity...", "url....");
			...
		}
	}	
