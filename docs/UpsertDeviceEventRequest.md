# UpsertDeviceEventRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the device event occurred. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the device involved in the event. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier. | [optional] 
**eventType** | [**DeviceEventType**](DeviceEventType.md) | The type of device event (e.g. site change, sensor start, pump resume). | [optional] 
**notes** | **String** | Free-text notes associated with the event (capped at 10,000 characters). | [optional] 
**syncIdentifier** | **String** | Upstream sync identifier for deduplication. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


