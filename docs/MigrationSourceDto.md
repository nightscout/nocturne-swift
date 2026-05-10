# MigrationSourceDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Unique identifier for this source | [optional] 
**mode** | [**MigrationMode**](MigrationMode.md) | Migration mode (Api or MongoDb) | [optional] 
**nightscoutUrl** | **String** | Nightscout URL (for API mode) | [optional] 
**mongoDatabaseName** | **String** | MongoDB database name (for MongoDB mode) | [optional] 
**lastMigrationAt** | **Date** | When the last successful migration completed | [optional] 
**lastMigratedDataTimestamp** | **Date** | Newest data timestamp migrated (for \&quot;since last\&quot; default) | [optional] 
**createdAt** | **Date** | When this source was first added | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


