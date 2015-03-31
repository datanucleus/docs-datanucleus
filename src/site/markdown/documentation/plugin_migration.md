<head><title>Plugin Migration</title></head>

# Section : [Documentation](index.html) 

## Migration Guide for DataNucleus plugins

If developing plugins for DataNucleus, this page gives information on how to upgrade them to the latest version(s)


### 4.0 -> 4.1

* Updated the bytecode enhancement contract to have all classes in _org.datanucleus.enhancement_ and use ExecutionContextReference in the enhancement contract 
rather than ExecutionContext, to minimise class loading requirements.


### 3.x -> 4.0

* _MetaDataManager_ changed to interface
* _TypeManager_ changed to interface
* _NucleusContext_ changed to interface, and _PersistenceNucleusContext_ used throughout main persistence code
* _PersistenceConfiguration_ renamed to _Configuration_
* _StoreManager_ addClass, addClasses, removeAllClasses methods have been renamed
* Plugin point "org.datanucleus":"store_mapping" changed to "org.datanucleus.store.rdbms":"java_mapping"
* Plugin point "org.datanucleus":"store_datastoreadapter" changed to "org.datanucleus.store.rdbms":"datastoreadapter"
* Plugin point "org.datanucleus":"store_identifierfactory" changed to "org.datanucleus.store.rdbms":"identifierfactory"
* Plugin point "org.datanucleus.store.rdbms":"rdbms_mapping" changed to "org.datanucleus.store.rdbms":"datastore_mapping"
* Many persistence properties changed, see migration notes for 4.0
* Majority of schema handling code is now moved from StoreManager to StoreSchemaHandler
* Refactor "org.datanucleus.query.evaluator.memory" to "org.datanucleus.query.inmemory"
* Change enhancement contract to use _org.datanucleus.enhancer.Persistable_
* Move identity generation to _org.datanucleus.identity.IdentityManager_


### 3.1 -> 3.2

* The enhancer is now part of core, but with org.datanucleus.enhancer package still. ASM is repackaged into core too (as org.datanucleus.asm).
* JDOClassLoaderResolver is renamed to ClassLoaderResolverImpl
* _org.datanucleus.store.types.sco_ is renamed to _org.datanucleus.store.types_
* _org.datanucleus.jta_ is renamed to _org.datanucleus.transaction.jta_
* _org.datanucleus.store.ObjectProvider_ moved to _org.datanucleus.state.ObjectProvider_ and removed _org.datanucleus.StateManager_ since redundant
* _org.datanucleus.store.ExecutionContext_ moved to _org.datanucleus.ExecutionContext_
* _ObjectManagerImpl_ renamed to _ExecutionContextImpl_
* _MultithreadedObjectManager_ renamed to _ExecutionContextThreadedImpl_
* _org.datanucleus.state.lock_ moved to _org.datanucleus.state_
* Removed attribute "persistent" from "java-type" extension (now in APIAdapter).
* _org.datanucleus.store.mapped_ is now moved into the RDBMS plugin as _org.datanucleus.store.rdbms.mapping_ (and other packages).
* Dropped ApiAdapter.isLoaded(ObjectProvider, fieldNum); just call ObjectProvider.isLoaded(fieldNum) instead.
* Dropped ApiAdapter.getVersion(ObjectProvider); just call ObjectProvider.getVersion() instead.
* StoreManager argument added to constructor of AbstractPersistenceHandler.
* package _org.datanucleus.query.typesafe_ is refactored from core to api.jdo.
* JavaTypeMapping/FieldManager arguments changed from Object to PreparedStatement/ResultSet in RDBMS plugin
* StoreManager should now set the "flushProcess" to be used (defaults to FlushNonReferential, but override if you want control of the flush ordering)


### 2.x -> 3.0

* In 2.x you have OMFContext. This is replaced by NucleusContext which also takes on the role of ObjectManagerFactoryImpl. You now create a NucleusContext by passing in the API name, its type and any startup properties.
* In 2.x the constructor to ConnectionFactoryImpl took an OMFContext. It now takes StoreManager. This is since the ConnectionFactory is specific to that datastore, and we need to allow a NucleusContext to manage multiple StoreManagers.
* StoreManager now takes in an additional argument with the persistence properties that it will manage. Just hand them to AbstractStoreManager constructor.
* The method DataNucleusDataSourceFactory.makePooledDataSource(OMFContext) is changed to DataNucleusDataSourceFactory.makePooledDataSource(StoreManager).
* When you want to access a persistence property, go via the StoreManager in general. This will then look whether the property is defined on the store, and if not will go to the NucleusContext (and if not specified by the user there, will use any available default).
* Some methods added/changed on DatastoreAdapter interface relating to name/version of product and driver
* StoreManager "valueGenerationMgr" is now lazy initialised, so always access it via getValueGenerationManager()
* StoreManager now owns the QueryManager, instead of NucleusContext
* If wanting to support SchemaTool, then your StoreManager must implement SchemaAwareStoreManager.
* If wanting to support Backed SCO wrappers, then your StoreManager must implement BackedSCOStoreManager.
* If wanting to support the datastore handing out object references (like in ODBMS), then your StoreManager must implement ObjectReferencingStoreManager
* You now have the ability to handle the insert of multiple objects at once, or the delete of multiple objects at once ... if your datastore doesn't have referential integrity (most except RDBMS). Look at StorePersistenceHandler and you can implement insertObjects(), deleteObjects().
* org.datanucleus.StateManager \-> org.datanucleus.state.StateManager
* org.datanucleus.metadata.VersionMetaData getNewVersion() moved to org.datanucleus.store.VersionHelper
* org.datanucleus.store.AbstractStoreManager performVersionCheck() moved to org.datanucleus.store.VersionHelper
* org.datanucleus.metadata.VersionMetaData and IdentityMetaData now only have 1 ColumnMetaData to reflect what we actually support
* org.datanucleus.store.mapped.scostore is now moved into the RDBMS plugin. If you were extending them you're advised to add your own variants in your plugin since those were RDBMS-based.
* XXXQuery constructors need to take in the StoreManager now too
