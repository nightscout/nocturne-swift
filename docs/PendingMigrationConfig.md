# PendingMigrationConfig

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hasPendingConfig** | **Bool** | Whether there is a pending migration configuration in env vars | [optional] 
**mode** | [**MigrationMode**](MigrationMode.md) | Migration mode from MIGRATION_MODE env var | [optional] 
**nightscoutUrl** | **String** | Nightscout URL from MIGRATION_NS_URL env var | [optional] 
**hasApiSecret** | **Bool** | Whether MIGRATION_NS_API_SECRET is set (never returns the actual secret) | [optional] 
**hasMongoConnectionString** | **Bool** | Whether MIGRATION_MONGO_CONNECTION_STRING is set (never returns the actual string) | [optional] 
**mongoDatabaseName** | **String** | MongoDB database name from MIGRATION_MONGO_DATABASE_NAME env var | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


