<head><title>Development : Persistence Process</title></head>

<a name="pessimistic"/>
##Pessimistic Transactions

All persist, remove, field update calls go to the datastore straight away. 
Flush() doesn't have the same significance here as it does for optimistic, except in that it will queue "update" requests until there are more than say 3 objects waiting.
This means that multiple setters can be called on a single object and we get one UPDATE statement.


###persist
Calls ExecutionContext.persistObject which calls EC.persistObjectWork.  
Creates an ObjectProvider (StateManagerImpl - SM). Adds the object to EC.dirtyOPs.  
Calls SM.makePersistent which calls SM.internalMakePersistent which will pass the persist through to the datastore plugin.  
Calls PersistenceHandler.insertObject, which will do any necessary cascade persist (coming back through EC.persistObjectInternal, EC.indirectDirtyOPs).  


###remove
Calls ExecutionContext.deleteObject, which calls ExecutionContext.deleteObjectWork.  
This will add the object to EC.dirtyOPs.  
Calls SM.deletePersistent.  
Calls SM.internalDeletePersistent which will pass the delete through to the datastore plugin.  
Calls PersistenceHandler.deleteObject, which will do any necessary cascade delete (coming back through EC.deleteObjectInternal, EC.indirectDirtyOPs).  


###update field
Calls SM.setXXXField which calls SM.updateField and, in turn, EC.makeDirty.  
The update is then queued internally until EC.flushInternal is triggered (e.g 3 changes waiting).  


###Collection.add
Calls SCO wrapper.add which will add the element locally.  
If a backing store is present (RDBMS) then passes it through to the backingStore.add().  


###Collection.remove/clear
Calls SCO wrapper.remove/clear which will add the element locally.  
If a backing store is present (RDBMS) then passes it through to the backingStore.remove()/clear().  
If no backing store is present and cascade delete is true then does the cascade delete, via EC.deleteObjectInternal.  


<a name="optimistic"/>
##Optimistic Transactions

All persist, remove, field update calls are queued.
Flush() processes all remove/add/updates that have been queued.
Call ExecutionContext.getOperationQueue() to see the operations that are queued up waiting to flush.


###persist
Calls ExecutionContext.persistObject which calls EC.persistObjectWork.  
Creates an ObjectProvider (StateManagerImpl - SM). Adds the object to EC.dirtyOPs.  
Calls SM.makePersistent. Uses PersistFieldManager to process all reachable objects.  


###remove
Calls ExecutionContext.deleteObject, which calls ExecutionContext.deleteObjectWork.  
Creates an ObjectProvider as required. Adds the object to EC.dirtyOPs.  
Calls SM.deletePersistent. Uses DeleteFieldManager to process all reachable objects.


###update field
Calls SM.setXXXField which calls SM.updateField and, in turn, EC.makeDirty.  
The update is then queued internally until EC.flushInternal is triggered.  


###Collection.add
Calls SCO wrapper.add which will add the element locally.  
Adds a queued operation to the queue for addition of this element.  


###Collection.remove/clear
Calls SCO wrapper.remove/clear which will add the element locally.  
Adds a queued operation to the queue for removal of this element.  


