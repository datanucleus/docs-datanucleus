<head><title>Extensions : Connection Pooling</title></head>

## Extensions : Persistence Properties
![Plugin](../../images/nucleus_plugin.gif)

DataNucleus is developed as a plugin-driven framework and one of the components that is 
pluggable is to allow definition of persistence properties. These properties are used by plugins
and allow configurability of behaviour. Any plugin can define its own properties.

You can define persistence properties using the plugin extension _org.datanucleus.persistence_properties_.

### Plugin Specification

The only thing required is to register the persistence property with DataNucleus via the _plugin.xml_. Here's an example

	<?xml version="1.0"?>
	<plugin id="mydomain" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.persistence_properties
        	<persistence-property name="datanucleus.magicBehaviour" value="false"
            	validator="org.datanucleus.properties.BooleanPropertyValidator"/>">
    	</extension>
	</plugin>

Note that you also require a MANIFEST.MF file as per the [Extensions Guide](index.html).
Note also

* If you specify the attribute __datastore__ as _true_ in the plugin.xml then your property will be stored with the StoreManager (instead of 
NucleusContext where it would normally be stored).
* If you specify the attribute __manager-overrideable__ as _true_ in the plugin.xml then the user can specify this property 
additionally on the PM/EM (rather than just on the PMF/EMF)
* The __validator__ attribute is optional but allows you to define a class that validates the values it can be set to.

### Plugin Usage

Now you can access this property from within your DataNucleus plugin via

	boolean magic = nucleusCtx.getPersistenceConfiguration().getBooleanProperty("datanucleus.magicBehaviour");

	// or from the StoreManager
	boolean magic = storeMgr.getBooleanProperty("datanucleus.magicBehaviour");

