# GlucosePredictionResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | Timestamp when predictions were calculated | [optional] 
**currentBg** | **Double** | Current blood glucose (mg/dL) | [optional] 
**delta** | **Double** | Rate of glucose change (mg/dL per 5 min) | [optional] 
**eventualBg** | **Double** | Eventual blood glucose if trend continues (mg/dL) | [optional] 
**iob** | **Double** | Current insulin on board (U) | [optional] 
**cob** | **Double** | Current carbs on board (g) | [optional] 
**sensitivityRatio** | **Double** | Sensitivity ratio used (1.0 &#x3D; normal) | [optional] 
**intervalMinutes** | **Int** | Prediction interval in minutes | [optional] 
**predictions** | [**PredictionCurves**](PredictionCurves.md) | Prediction curves with different scenarios | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


