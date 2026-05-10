# CreateSystemEventRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**eventType** | [**SystemEventType**](SystemEventType.md) | Gets or sets the event type (alarm, warning, or info). | [optional] 
**category** | [**SystemEventCategory**](SystemEventCategory.md) | Gets or sets the event category. | [optional] 
**code** | **String** | Gets or sets an optional short code identifying the event. | [optional] 
**description** | **String** | Gets or sets a human-readable description of the event. | [optional] 
**mills** | **Int64** | Gets or sets the Unix millisecond timestamp of the event. | [optional] 
**source** | **String** | Gets or sets the data source identifier (defaults to \&quot;manual\&quot; when absent). | [optional] 
**metadata** | **[String: JSONValue]** | Gets or sets arbitrary metadata associated with the event. | [optional] 
**originalId** | **String** | Gets or sets the original MongoDB ObjectId, preserved for migration compatibility. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


