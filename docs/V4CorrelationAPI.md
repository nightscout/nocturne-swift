# V4CorrelationAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**correlationGetCorrelated**](V4CorrelationAPI.md#correlationgetcorrelated) | **GET** /api/v4/correlated/{correlationId} | Get all data correlated by a shared correlation ID across all V4 data types


# **correlationGetCorrelated**
```swift
    open class func correlationGetCorrelated(correlationId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Get all data correlated by a shared correlation ID across all V4 data types

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let correlationId = "correlationId_example" // String | 

// Get all data correlated by a shared correlation ID across all V4 data types
V4CorrelationAPI.correlationGetCorrelated(correlationId: correlationId) { (response, error) in
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

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

