# ProcessingAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**processingGetProcessingStatus**](ProcessingAPI.md#processinggetprocessingstatus) | **GET** /api/v4/processing/status/{correlationId} | 
[**processingWaitForCompletion**](ProcessingAPI.md#processingwaitforcompletion) | **GET** /api/v4/processing/status/{correlationId}/wait | 


# **processingGetProcessingStatus**
```swift
    open class func processingGetProcessingStatus(correlationId: String, completion: @escaping (_ data: ProcessingStatusResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let correlationId = "correlationId_example" // String | 

ProcessingAPI.processingGetProcessingStatus(correlationId: correlationId) { (response, error) in
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
 **correlationId** | **String** |  | 

### Return type

[**ProcessingStatusResponse**](ProcessingStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **processingWaitForCompletion**
```swift
    open class func processingWaitForCompletion(correlationId: String, timeoutSeconds: Int? = nil, completion: @escaping (_ data: ProcessingStatusResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let correlationId = "correlationId_example" // String | 
let timeoutSeconds = 987 // Int |  (optional) (default to 30)

ProcessingAPI.processingWaitForCompletion(correlationId: correlationId, timeoutSeconds: timeoutSeconds) { (response, error) in
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
 **correlationId** | **String** |  | 
 **timeoutSeconds** | **Int** |  | [optional] [default to 30]

### Return type

[**ProcessingStatusResponse**](ProcessingStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

