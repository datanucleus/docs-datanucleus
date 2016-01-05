<head><title>Extensions</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## DataNucleus Extensions

DataNucleus products are built using a plugin mechanism, allowing plugins to operate together.
This plugin mechanism is useful also from a user viewpoint in that you, the user, could provide plugins that use these plugin points and 
extend the capabilities of DataNucleus. Plugins are loaded by a plugin manager when DataNucleus is initialised at runtime, and this plugin 
manager uses a registry mechanism, inspecting jars in the CLASSPATH. The three steps necessary for creating a DataNucleus plugin are

1. Review the DataNucleus PluginPoint that you will need to implement to generate the plugin, and implement it.
2. Create a file _plugin.xml_ at the top level of your JAR defining the plugin details (see the actual PluginPoint docs).
3. Update the META-INF/MANIFEST.MF file contained in the jar so that it includes necessary information for OSGi.

Plugin points differ from one version of DataNucleus to another, so you should consult the documentation of the version of DataNucleus
that you are using. The documentation for extensions in the latest version of DataNucleus can be found [here](http://www.datanucleus.org/products/accessplatform/extensions/index.html)
