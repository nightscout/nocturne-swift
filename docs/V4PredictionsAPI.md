# V4PredictionsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**predictionGetPredictions**](V4PredictionsAPI.md#predictiongetpredictions) | **GET** /api/v4/predictions | Get glucose predictions based on current data. Returns predicted glucose values for the next 4 hours in 5-minute intervals.
[**predictionGetStatus**](V4PredictionsAPI.md#predictiongetstatus) | **GET** /api/v4/predictions/status | Check the status of the prediction service.


# **predictionGetPredictions**
```swift
    open class func predictionGetPredictions(profileId: String? = nil, completion: @escaping (_ data: GlucosePredictionResponse?, _ error: Error?) -> Void)
```

Get glucose predictions based on current data. Returns predicted glucose values for the next 4 hours in 5-minute intervals.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let profileId = "profileId_example" // String | Optional profile ID to use for predictions (optional)

// Get glucose predictions based on current data. Returns predicted glucose values for the next 4 hours in 5-minute intervals.
V4PredictionsAPI.predictionGetPredictions(profileId: profileId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **profileId** | **String** | Optional profile ID to use for predictions | [optional] 

### Return type

[**GlucosePredictionResponse**](GlucosePredictionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **predictionGetStatus**
```swift
    open class func predictionGetStatus(completion: @escaping (_ data: PredictionStatusResponse?, _ error: Error?) -> Void)
```

Check the status of the prediction service.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Check the status of the prediction service.
V4PredictionsAPI.predictionGetStatus() { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PredictionStatusResponse**](PredictionStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

