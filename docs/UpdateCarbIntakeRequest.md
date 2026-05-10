# UpdateCarbIntakeRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the carbs were consumed. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the device that recorded the intake. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier; required when SyncIdentifier is supplied. | [optional] 
**carbs** | **Double** | Amount of carbohydrates consumed in grams. | [optional] 
**syncIdentifier** | **String** | Upstream sync identifier for deduplication, paired with DataSource. | [optional] 
**carbTime** | **Double** | Minutes from bolus time to expected carb absorption start (pre-bolus offset). | [optional] 
**absorptionTime** | **Int** | Expected carb absorption duration in minutes. | [optional] 
**correlationId** | **String** | Correlation identifier for grouping related events. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


