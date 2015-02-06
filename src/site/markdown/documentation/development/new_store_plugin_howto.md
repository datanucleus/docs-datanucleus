<head><title>Schema Migration</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## HOWTO Support A New Datastore

The process of adding support for a new datastore is simple in concept. It has particular components that can be supported or not. 
You don't have to support everything at once. The following gives guidelines on how to do it

* Is there a supported datastore that is similar in terms of its access ? If so, copy the existing datastore plugin (renaming packages etc). 
For example to support another OODB, you could take the "datanucleus-db4o" plugin as a start point. Develop the XXXStoreManager class. 
__You are recommended to extend _org.datanucleus.store.AbstractStoreManager_. Make sure you specify the _getSupportedOptions()_ method specifying what is supported__
* Develop the ConnectionFactoryImpl. This provides connectivity to the datastore. If the datastore has a simple connection that you open then commit then this 
file will be very simple. Again, copy an existing one if there is something suitable. 
__You are recommended to extend _org.datanucleus.store.connection.AbstractConnectionFactory_ __
* Develop the PersistenceHandler. This provides the capability to do insert/update/delete/fetch/locate and so provides support for persistence to this datastore.
__You are recommended to extend _org.datanucleus.store.AbstractPersistenceHandler_ __
* Does your datastore support the concept of a "schema" ? i.e you need to create some "table" in the datastore to store objects in? If so then you should implement the SchemaHandler.
__You are recommended to extend _org.datanucleus.store.schema.AbstractStoreSchemaHandler_ __
* Develop the JDOQL support. Make use of the _org.datanucleus.query_ classes. You need to decide how much of the query can be embodied in the native query language 
of the datastore. If you can't support some feature in the datastore native language then use the in-memory query evaluation
* Add on support for other features like inheritance strategy, discriminators, version checks, type converters as they are required.

As a guide, the basic connection, persistence could maybe be done in 2-4 days supporting "complete-table" only. 
To provide JDOQL in-memory capability, you could do that in very short time also since the in-memory evaluator is done and the only thing you need to do is retrieve 
the candidate objects (of the candidate type). 
To provide JDOQL in-datastore capability would take longer, how much would depend on the native query language structure for your datastore. 
Supporting things like other inheritance strategies may take significantly longer depending in the datastore. 