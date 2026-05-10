# UpsertBGCheckRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the BG check was performed. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the device that performed the check. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier. | [optional] 
**glucose** | **Double** | Blood glucose reading value (validated 0-10,000). | [optional] 
**units** | [**GlucoseUnit**](GlucoseUnit.md) | Unit of the glucose reading (mg/dL or mmol/L). | [optional] 
**glucoseType** | [**GlucoseType**](GlucoseType.md) | Origin of the glucose value (finger stick, sensor, manual, etc.). | [optional] 
**syncIdentifier** | **String** | Upstream sync identifier for deduplication. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


