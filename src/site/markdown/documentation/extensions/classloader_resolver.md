<head><title>Extensions : ClassLoaderResolver</title></head>

# Section : [Documentation](../index.html) > [Extensions](index.html)

## Extensions : ClassLoader Resolvers
![Plugin](../../images/nucleus_plugin.gif)

DataNucleus is developed as a plugin-driven framework and one of the components that is pluggable is the class-loading resolution. 
DataNucleus provides its own internal class-loader resolver that matches the requirements of the JDO specification, but also allows you to plugin 
your own class loading policy. This class loader resolver is used for runtime operation. The plugin mechanism always operates 
using an instance of ClassLoaderResolverImpl since we need a class loading process to discover the plugins in the first place.

DataNucleus has to resolve classes at runtime. The JDO specification defines a strict process for 
resolving classes using specific class loaders. DataNucleus provides a plugin for this JDO process.
You can extend DataNucleus's capabilities using the plugin extension *org.datanucleus.classloader_resolver*.

<table>
    <tr>
    <th>Plugin extension-point</th>
    <th>Key</th>
    <th>Description</th>
    <th width="80">Location</th>
    </tr>
    <tr>
    <td>org.datanucleus.classloader_resolver</td>
    <td>jdo</td>
    <td>ClassLoaderResolver using JDO definition</td>
    <td>datanucleus-core</td>
    </tr>
</table>


### JDO Implementation

At runtime, DataNucleus will need to load the classes being persisted. To do this it needs to 
utilise a particular class loading mechanism. The JDO specification defines how class-loading is 
to operate in a JDO implementation and this is what DataNucleus uses by default. In brief the 
JDO class-loading mechanism utilises 3 class loaders

* When creating the PersistenceManagerFactory you can specify a class loader. This is used first if specified
* The second class loader to try is the class loader for the current thread.
* The third class loader to try is the class loader for the PMF context.

If a class cannot be loaded using these three loaders then an exception is typically thrown depending on the operation.

### Interface

Any identifier factory plugin will need to implement _org.datanucleus.ClassLoaderResolver_.
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/ClassLoaderResolver.html).
So you need to implement the following interface

	package org.datanucleus;
	...
	public interface ClassLoaderResolver
	{
	    /**
	     * Class loading method, allowing specification of a primary loader. 
	     * This method does not initialize the class
	     * @param name Name of the Class to be loaded
	     * @param primary the primary ClassLoader to use (or null)
	     * @return The Class given the name, using the specified ClassLoader
	     * @throws ClassNotResolvedException if the class can't be found in the classpath
	     */
	    public Class classForName(String name, ClassLoader primary);

            /**
         * Class loading method, allowing specification of a primary loader
         * and whether the class should be initialised or not.
         * @param name Name of the Class to be loaded
         * @param primary the primary ClassLoader to use (or null)
         * @param initialize whether to initialize the class or not.
         * @return The Class given the name, using the specified ClassLoader
         * @throws ClassNotResolvedException if the class can't be found in the classpath
         */
        public Class classForName(String name, ClassLoader primary, boolean initialize);
    
        /**
         * Class loading method. This method does not initialize the class
         * @param name Name of the Class to be loaded
         * @return The Class given the name, using the specified ClassLoader
         */
        public Class classForName(String name);
    
        /**
         * Class loading method, allowing for initialisation of the class.
         * @param name Name of the Class to be loaded
         * @param initialize whether to initialize the class or not.
         * @return The Class given the name, using the specified ClassLoader
         */
        public Class classForName(String name, boolean initialize);

        /**
         * Method to test whether the type represented by the specified class_2 
         * parameter can be converted to the type represented by class_name_1 parameter.
         * @param class_name_1 Class name
         * @param class_2 Class to compare against
         * @return Whether they are assignable
         */
        public boolean isAssignableFrom(String class_name_1, Class class_2);

        /**
         * Method to test whether the type represented by the specified class_name_2 
         * parameter can be converted to the type represented by class_1 parameter.
         * @param class_1 First class
         * @param class_name_2 Class name to compare against
         * @return Whether they are assignable
         */
        public boolean isAssignableFrom(Class class_1, String class_name_2);

        /**
         * Method to test whether the type represented by the specified class_name_2 
         * parameter can be converted to the type represented by class_name_1 parameter.
         * @param class_name_1 Class name
         * @param class_name_2 Class name to compare against
         * @return Whether they are assignable
         */
        public boolean isAssignableFrom(String class_name_1, String class_name_2);
        
        /**
         * ClassLoader registered to load classes created at runtime. One ClassLoader can
         * be registered, and if one ClassLoader is already registered, the registered ClassLoader
         * is replaced by <code>loader</code>.
         * @param loader The ClassLoader in which classes are defined
         */
        public void registerClassLoader(ClassLoader loader);
    
        /**
         * ClassLoader registered by users to load classes. One ClassLoader can
         * be registered, and if one ClassLoader is already registered, the registered ClassLoader
         * is replaced by <code>loader</code>.
         * @param loader The ClassLoader in which classes are loaded
         */
        public void registerUserClassLoader(ClassLoader loader);

        /**
         * Finds all the resources with the given name.
         * @param resourceName the resource name. If <code>resourceName</code> starts with "/", 
         *           remove it before searching.
         * @param primary the primary ClassLoader to use (or null)
         * @return An enumeration of URL objects for the resource. If no resources could be found,
         *           the enumeration will be empty. 
         * Resources that the class loader doesn't have access to will not be in the enumeration.
         * @throws IOException If I/O errors occur
         * @see ClassLoader#getResources(java.lang.String)
         */
        public Enumeration getResources(String resourceName, ClassLoader primary) throws IOException;
        
        /**
         * Finds the resource with the given name.
         * @param resourceName the path to resource name relative to the classloader root path. 
         *        If <code>resourceName</code> starts with "/", remove it.   
         * @param primary the primary ClassLoader to use (or null)
         * @return A URL object for reading the resource, or null if the resource could not be found or 
         *         the invoker doesn't have adequate privileges to get the resource. 
         * @throws IOException If I/O errors occur
         * @see ClassLoader#getResource(java.lang.String)
         */
        public URL getResource(String resourceName, ClassLoader primary);
    
        /**
         * Sets the primary classloader for the current thread.
         * The primary should be kept in a ThreadLocal variable.
         * @param primary the primary classloader
         */
        void setPrimary(ClassLoader primary);

        /**
         * Unsets the primary classloader for the current thread
         */
        void unsetPrimary();
    
	}

Be aware that you can extend <i>org.datanucleus.JDOClassLoaderResolver</i> if you just want to change 
some behaviour of the default loader process. Your class loader resolver should provide a 
constructor taking an argument of type <i>ClassLoader</i> which will be the loader that the 
PersistenceManager is using at initialisation (your class can opt to not use this, but must provide the constructor)

### Implementation

Let's suppose you want to provide your own resolver _MyClassLoaderResolver_

	package mydomain;
	
	import org.datanucleus.ClassLoaderResolver;
    
	public class MyClassLoaderResolver implements ClassLoaderResolver
	{
	    /**
	     * Constructor for PersistenceManager cases.
	     * @param pmLoader Loader from PM initialisation time.
	     */
	    public MyClassLoaderResolver(ClassLoader pmLoader)
	    {
	         ...
	    }
	
	    .. (implement the interface)
	}

### Plugin Specification

When we have defined our "IdentifierFactory" we just need to make it into a DataNucleus plugin.
To do this you simply add a file _plugin.xml_ to your JAR at the root. The file _plugin.xml_ should look like this


	<?xml version="1.0"?>
	<plugin id="mydomain" name="DataNucleus plug-ins" provider-name="My Company">
    	<extension point="org.datanucleus.classloader_resolver">
        	<class-loader-resolver name="myloader" class-name="mydomain.MyClassLoaderResolver"/>
    	</extension>
	</plugin>

Note that you also require a MANIFEST.MF file as per the [Extensions Guide](index.html).

### Plugin Usage

The only thing remaining is to use your new _ClassLoaderResolver_ plugin. You do this by having your plugin in the CLASSPATH at runtime, 
and setting the PMF property __datanucleus.classLoaderResolverName__ to _myloader_ (the name you specified in the plugin.xml file).

