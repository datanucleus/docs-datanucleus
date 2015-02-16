<head><title>Extensions : Identity Key Translators</title></head>

# Section : [Documentation](../index.html) > [Extensions](index.html)

## Extensions : Identity Key Translators
![Plugin](../../images/nucleus_plugin.gif)

DataNucleus is developed as a plugin-driven framework and one of the components that is pluggable is 
translation of identities. When you call <i>pm.getObjectById(cls, key)</i> you pass in the "key". 
This object can be the toString() form of an identity, or the key of a single-string form. 
Some store managers (e.g GAE/J) allow non-standard key input and this allows for the translation
into a standardised key form. Alternatively you could do this in your own code, but the facility 
is provided. This means that in your application you only use your own form of identities.


You can extend DataNucleus's capabilities using the plugin extension *org.datanucleus.identity_key_translator*.

### Interface

Any identifier factory plugin will need to implement <i>org.datanucleus.store.IdentifierKeyFactory</i>.
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/identity/IdentityKeyTranslator.html).
So you need to implement the following interface

	package org.datanucleus.identity;
	
	public interface IdentityKeyTranslator
	{
	    /**
	     * Method to translate the string into the identity.
	     * @param ec ExecutionContext
	     * @param cls The persistable class
	     * @param key The input key
	     * @return The returned key
	     */
	    Object getKey(ObjectManager om, Class cls, Object key);
	}

### Plugin Specification

When we have defined our "IdentityKeyTranslator" we just need to make it into a DataNucleus  plugin. To do this you simply add a file 
_plugin.xml_ to your JAR at the root. The file _plugin.xml_ should look like this


	<?xml version="1.0"?>
	<plugin id="mydomain" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.identity_key_translator">
        	<identitykeytranslator name="mytranslator" class-name="mydomain.MyIdKeyTranslator"/>
    	</extension>
	</plugin>

Note that you also require a MANIFEST.MF file as per the [Extensions Guide](index.html).

### Plugin Usage

The only thing remaining is to use your new _IdentityStringTranslator_ plugin. You do this by having your plugin in the CLASSPATH at runtime, 
and setting the persistence property __datanucleus.identityKeyTranslatorType__ to _mytranslator_ (the name you specified in the plugin.xml file).

