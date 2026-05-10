# UpsertActivityRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mills** | **Int64** | When the activity occurred, as a Unix millisecond timestamp. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**type** | **String** | Activity type or category (e.g., \&quot;exercise\&quot;, \&quot;walk\&quot;, \&quot;run\&quot;). | [optional] 
**description** | **String** | Activity description or notes. | [optional] 
**duration** | **Double** | Duration of the activity in minutes. | [optional] 
**intensity** | **String** | Intensity level of the activity. | [optional] 
**notes** | **String** | Additional notes about the activity. | [optional] 
**enteredBy** | **String** | Name of the application or person that submitted this record. | [optional] 
**distance** | **Double** | Distance covered during the activity. | [optional] 
**distanceUnits** | **String** | Units for distance (e.g., \&quot;meters\&quot;, \&quot;kilometers\&quot;, \&quot;miles\&quot;). | [optional] 
**energy** | **Double** | Energy expended during the activity (calories). | [optional] 
**energyUnits** | **String** | Units for energy (e.g., \&quot;calories\&quot;, \&quot;kilocalories\&quot;, \&quot;joules\&quot;). | [optional] 
**name** | **String** | Name or title of the activity. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


