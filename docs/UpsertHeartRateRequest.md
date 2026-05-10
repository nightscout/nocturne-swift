# UpsertHeartRateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the heart rate measurement was taken. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**bpm** | **Int** | Heart rate in beats per minute. | [optional] 
**accuracy** | **Int** | Sensor accuracy indicator (device-specific scale). | [optional] 
**device** | **String** | Identifier of the wearable or sensor device. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


