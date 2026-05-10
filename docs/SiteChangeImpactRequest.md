# SiteChangeImpactRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entries** | [SensorGlucose] | Collection of sensor glucose readings | [optional] 
**deviceEvents** | [DeviceEvent] | Collection of device events (must include site changes) | [optional] 
**hoursBeforeChange** | **Int** | Hours before site change to analyze (default: 12) | [optional] 
**hoursAfterChange** | **Int** | Hours after site change to analyze (default: 24) | [optional] 
**bucketSizeMinutes** | **Int** | Time bucket size for averaging in minutes (default: 30) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


