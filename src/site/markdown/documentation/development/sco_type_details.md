<head><title>SCO Type Details</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## Second-Class Objects

When a persistable class is persisted and has a field of a (mutable) second-class type (Collection, Map, Date, etc) then DataNucleus needs to know when the
user calls operations on it to change the contents of the object. To do this, at the first reference to the field once enlisted in a transaction, DataNucleus 
will replace the field value with a _proxy wrapper_ wrapping the real object. This has no effect for the user in that the field is still castable to 
the same type as they had in that field, but all operations are intercepted.


### Container fields : Caching of Values

By default when a container field is replaced by a second-class object (SCO) wrapper it will be enabled to cache the values in that field. This means that once 
the values are loaded in that field there will be no need to make any call to the datastore unless changing the container. This gives significant speed-up 
when compared to relaying all calls via the datastore. You can change to <b>not</b> use caching by setting either

* Globally for the PersistenceManagerFactory - this is controlled by setting the persistence property 
__org.datanucleus.cache.collections__. Set it to false to pass through to the datastore.
* For the specific Collection/Map - add a MetaData &lt;collection&gt; or &lt;map&gt; extension 
_cache_ setting it to false to pass through to the datastore.

This is implemented in a typical SCO proxy wrapper by using the SCOUtils method _useContainerCache()_ which determines if caching is required, and by having a 
method _load()_ on all proxy wrapper container classes.


### Container fields : Lazy Loading

JDO and JPA provide mechanisms for specifying whether fields are loaded lazily (when required) or whether they are loaded eagerly (when the object is first met). 
DataNucleus follows these specifications but also allows the user to override the lazy loading for a SCO container. For example if a collection field was marked 
as being part of the default fetch group it should be loaded eagerly which means that when the owning object is instantiated the collection is loaded up too. 
If the user overrides the lazy loading for that field in that situation to make it lazy, DataNucleus will instantiate the owning object and instantiate the 
collection but leave it marked as "to be loaded" and the elements will be loaded up when needed. You can change the lazy loading setting via

* Globally for the PMF/EMF - this is controlled by setting the persistence property __org.datanucleus.cache.collections.lazy__. 
Set it to true to use lazy loading, and set it to false to load the elements when the collection/map is initialised.
* For the specific Collection/Map - add a MetaData &lt;collection&gt; or &lt;map&gt; extension __cache-lazy-loading__. 
Set it to true to use lazy loading, and false to load once at initialisation.


### SCO fields : Queuing operations

When DataNucleus is using an optimistic transaction it attempts to delay all datastore operations until _commit_ is called on the transaction or _flush_ is 
called on the PersistenceManager/EntityManager. This implies a change to operation of SCO proxy wrappers in that they must __queue__ up all mutating operations 
(add, clear, remove etc) until such a time as they need to be sent to the datastore. The ExecutionContext has the queue for this purpose.

All code for the queued operations are stored under _org.datanucleus.flush_.


### Simple SCO interceptors

There are actually two sets of SCO wrappers in DataNucleus. The first set provide lazy loading, queueing, etc and have a "backing store" where the operations
can be fed through to the datastore as they are made (for RDBMS). The second set are simple wrappers that intercept operations and mark the field as dirty in 
the ObjectProvider. This second set are for use with datastores such as _neodatis_ that don't utilise backing stores and just want to know when the field is dirty
and hence should be written.

All code for the backed SCO wrappers are stored under _org.datanucleus.store.types.wrappers.backed_.
All code for the simple SCO wrappers are stored under _org.datanucleus.store.types.wrappers_.
