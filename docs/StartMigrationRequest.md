# StartMigrationRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mode** | [**MigrationMode**](MigrationMode.md) | Migration mode (API or MongoDB) | [optional] 
**nightscoutUrl** | **String** | Nightscout URL (for API mode) | [optional] 
**nightscoutApiSecret** | **String** | Nightscout API secret (for API mode) | [optional] 
**mongoConnectionString** | **String** | MongoDB connection string (for MongoDB mode) | [optional] 
**mongoDatabaseName** | **String** | MongoDB database name (for MongoDB mode) | [optional] 
**collections** | **[String]** | Collections to migrate. Empty means all. | [optional] 
**startDate** | **Date** | Start date for migration (optional) | [optional] 
**endDate** | **Date** | End date for migration (optional) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


