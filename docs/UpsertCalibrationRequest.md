# UpsertCalibrationRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the calibration was performed. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the CGM device being calibrated. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier. | [optional] 
**slope** | **Double** | Linear calibration slope coefficient. | [optional] 
**intercept** | **Double** | Linear calibration intercept value. | [optional] 
**scale** | **Double** | Calibration scale factor. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


