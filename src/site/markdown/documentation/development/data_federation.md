<head><title>Data Federation</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## Data Federation

DataNucleus has a starting point for providing Data Federation (sharding, polyglot persistence). In simple terms you have a primary "store" and several secondary "store"s.
You define the _persistence.xml_ as you normally would but would include properties like the following to define the secondary stores.

    datanucleus.datastore.SecondStore=secondstore.properties
    datanucleus.datastore.ThirdStore=thirdstore.properties
    
and the specified files contain the details for those secondary stores. Internally there is a single controlling __FederatedStoreManager__ which internally
references a primary __XXXStoreManager__ and secondary ___XXXStoreManager__ (where XXX should be replaced by the datastore type in question). This means
that there is a single MetaDataManager, and hence you cannot have different metadata for the secondary stores.

The current handling should provide basic persistence and querying.


To take this forward, we need to consider having the MetaDataManager (optionally) hanging off the StoreManager rather than the NucleusContext.
