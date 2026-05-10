# StatusAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**statusGetHealthStatus**](StatusAPI.md#statusgethealthstatus) | **GET** /api/v4/Status/health | Get a simple health check status
[**statusGetStatus**](StatusAPI.md#statusgetstatus) | **GET** /api/v4/Status | Get detailed system status information


# **statusGetHealthStatus**
```swift
    open class func statusGetHealthStatus(completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Get a simple health check status

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get a simple health check status
StatusAPI.statusGetHealthStatus() { (response, error) in
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

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statusGetStatus**
```swift
    open class func statusGetStatus(completion: @escaping (_ data: StatusResponse?, _ error: Error?) -> Void)
```

Get detailed system status information

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get detailed system status information
StatusAPI.statusGetStatus() { (response, error) in
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

[**StatusResponse**](StatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

