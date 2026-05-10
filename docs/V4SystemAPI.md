# V4SystemAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**systemHeartbeat**](V4SystemAPI.md#systemheartbeat) | **POST** /api/v4/system/heartbeat | Accept a heartbeat from an external service (e.g. bot adapter). Returns 200 OK. Actual health tracking will be added later.


# **systemHeartbeat**
```swift
    open class func systemHeartbeat(heartbeatRequest: HeartbeatRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Accept a heartbeat from an external service (e.g. bot adapter). Returns 200 OK. Actual health tracking will be added later.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let heartbeatRequest = HeartbeatRequest(platforms: ["platforms_example"], service: "service_example") // HeartbeatRequest | 

// Accept a heartbeat from an external service (e.g. bot adapter). Returns 200 OK. Actual health tracking will be added later.
V4SystemAPI.systemHeartbeat(heartbeatRequest: heartbeatRequest) { (response, error) in
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
 **heartbeatRequest** | [**HeartbeatRequest**](HeartbeatRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

