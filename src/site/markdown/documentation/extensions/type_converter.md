<head><title>Extensions : Type Converter</title></head>

## Extensions : Type Converter
![Plugin](../../images/nucleus_plugin.gif)

DataNucleus allows you to provide alternate ways of persisting Java types. Whilst it includes the majority of normal converters built-in, 
you can extend DataNucleus's capabilities using the plugin extension _org.datanucleus.type_converter_.

### Interface

Any value generator plugin will need to implement _org.datanucleus.store.types.converters.TypeConverter_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/store/types/converters/TypeConverter.html).
So you need to implement the following interface

	public interface TypeConverter<X, Y> extends Serializable
	{
    	/**
    	 * Method to convert the passed member value to the datastore type.
    	 * @param memberValue Value from the member
    	 * @return Value for the datastore
    	 */
    	Y toDatastoreType(X memberValue);
	
    	/**
    	 * Method to convert the passed datastore value to the member type.
    	 * @param datastoreValue Value from the datastore
    	 * @return Value for the member
    	 */
    	X toMemberType(Y datastoreValue);
	}


### Implementation

Let's take an example. If we look at the Java type URI we want to persist it as a String since a native URI type isn't present in datastores. We define our class as

	public class URIStringConverter implements TypeConverter<URI, String>
	{
    	public URI toMemberType(String str)
    	{
        	if (str == null)
        	{
            	return null;
        	}

        	return java.net.URI.create(str.trim());
    	}

    	public String toDatastoreType(URI uri)
    	{
        	return uri != null ? uri.toString() : null;
    	}
	}

So when converting it for the datastore it will use the _toString()_ form of the URI,
and will be converted back to a URI (on retrieval from the datastore) using the _URI.create_ method. 
Obviously this particular TypeConverter is included in DataNucleus, but hopefully it gives an idea of what to do to provide your own.

### Plugin Specification

So we now have our custom "value generator" and we just need to make this into a DataNucleus plugin. To do this you simply add a file 
_plugin.xml_ to your JAR at the root. The file _plugin.xml_ should look like this

	<?xml version="1.0"?>
	<plugin id="mydomain" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.type_converter">
        	<type-converter name="dn.uri-string" member-type="java.net.URI" datastore-type="java.lang.String"
            	converter-class="mydomain.converters.URIStringConverter"/>
    	</extension>
	</plugin>

Note that you also require a MANIFEST.MF file as per the [Extensions Guide](index.html).

The name "dn.uri-string" can be used to refer to this converter from within a [java_types extension point](java_types.html) definition 
for the default converter to use for a Java type.
