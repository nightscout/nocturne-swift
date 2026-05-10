# CorrelationAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**correlationGetCorrelated**](CorrelationAPI.md#correlationgetcorrelated) | **GET** /api/v4/correlated/{correlationId} | Retrieves all records that share the given correlation ID across every V4 data type.


# **correlationGetCorrelated**
```swift
    open class func correlationGetCorrelated(correlationId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Retrieves all records that share the given correlation ID across every V4 data type.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let correlationId = "correlationId_example" // String | The shared correlation ID to look up.

// Retrieves all records that share the given correlation ID across every V4 data type.
CorrelationAPI.correlationGetCorrelated(correlationId: correlationId) { (response, error) in
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
 **correlationId** | **String** | The shared correlation ID to look up. | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

