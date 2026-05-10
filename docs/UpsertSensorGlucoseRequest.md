# UpsertSensorGlucoseRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the sensor reading was taken. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the CGM transmitter or receiver. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier. | [optional] 
**mgdl** | **Double** | Glucose reading in mg/dL (validated 0-10,000). | [optional] 
**direction** | [**GlucoseDirection**](GlucoseDirection.md) | Glucose trend direction (rising, falling, stable, etc.). | [optional] 
**trendRate** | **Double** | Rate of glucose change in mg/dL per minute. | [optional] 
**noise** | **Int** | Sensor noise level indicator (device-specific scale). | [optional] 
**filtered** | **Double** | Raw filtered sensor value (scaled ADC) | [optional] 
**unfiltered** | **Double** | Raw unfiltered sensor value (scaled ADC) | [optional] 
**delta** | **Double** | Glucose delta in mg/dL over the last 5 minutes | [optional] 
**glucoseProcessing** | **String** | Whether this glucose value is smoothed or unsmoothed. Accepted values: \&quot;Smoothed\&quot;, \&quot;Unsmoothed\&quot;. Case-insensitive. Null for unknown. | [optional] 
**smoothedMgdl** | **Double** | Smoothed glucose value in mg/dL, when known. | [optional] 
**unsmoothedMgdl** | **Double** | Unsmoothed (raw) glucose value in mg/dL, when known. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


