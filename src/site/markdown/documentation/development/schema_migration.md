<head><title>Schema Migration</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## Schema Migration Scenarios That We Intend To Support

During the lifecycle of a class, the user can do the following

1. Add a field. Need to cater for data in the datastore which doesn't have this field, still allowing it to be readable, and add the data when possible
2. Update the type of a field. Need to provide for data migration.
3. Delete a field. Need to cater for removing redundant data from the existent records
4. Add a class.
5. Rename a class. Need to migrate data across
6. Delete a class. Remove redundant data from the datastore

The aim has to be for all store plugins to support these operations (when we have resource to do so). Some support would be at runtime, but some could be in SchemaTool