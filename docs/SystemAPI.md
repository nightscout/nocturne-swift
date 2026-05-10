# SystemAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**systemGetChannelStatuses**](SystemAPI.md#systemgetchannelstatuses) | **GET** /api/v4/system/channels | 
[**systemHeartbeat**](SystemAPI.md#systemheartbeat) | **POST** /api/v4/system/heartbeat | 


# **systemGetChannelStatuses**
```swift
    open class func systemGetChannelStatuses(completion: @escaping (_ data: ChannelStatusResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


SystemAPI.systemGetChannelStatuses() { (response, error) in
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

[**ChannelStatusResponse**](ChannelStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **systemHeartbeat**
```swift
    open class func systemHeartbeat(heartbeatRequest: HeartbeatRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let heartbeatRequest = HeartbeatRequest(platforms: ["platforms_example"], service: "service_example") // HeartbeatRequest | 

SystemAPI.systemHeartbeat(heartbeatRequest: heartbeatRequest) { (response, error) in
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

