# V4DeviceEventsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deviceEventCreate**](V4DeviceEventsAPI.md#deviceeventcreate) | **POST** /api/v4/observations/device-events | 
[**deviceEventDelete**](V4DeviceEventsAPI.md#deviceeventdelete) | **DELETE** /api/v4/observations/device-events/{id} | 
[**deviceEventGetAll**](V4DeviceEventsAPI.md#deviceeventgetall) | **GET** /api/v4/observations/device-events | 
[**deviceEventGetById**](V4DeviceEventsAPI.md#deviceeventgetbyid) | **GET** /api/v4/observations/device-events/{id} | 
[**deviceEventUpdate**](V4DeviceEventsAPI.md#deviceeventupdate) | **PUT** /api/v4/observations/device-events/{id} | 


# **deviceEventCreate**
```swift
    open class func deviceEventCreate(upsertDeviceEventRequest: UpsertDeviceEventRequest, completion: @escaping (_ data: DeviceEvent?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertDeviceEventRequest = UpsertDeviceEventRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", eventType: DeviceEventType(), notes: "notes_example", syncIdentifier: "syncIdentifier_example") // UpsertDeviceEventRequest | 

V4DeviceEventsAPI.deviceEventCreate(upsertDeviceEventRequest: upsertDeviceEventRequest) { (response, error) in
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
 **upsertDeviceEventRequest** | [**UpsertDeviceEventRequest**](UpsertDeviceEventRequest.md) |  | 

### Return type

[**DeviceEvent**](DeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceEventDelete**
```swift
    open class func deviceEventDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4DeviceEventsAPI.deviceEventDelete(id: id) { (response, error) in
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
 **id** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceEventGetAll**
```swift
    open class func deviceEventGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfDeviceEvent?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")
let device = "device_example" // String |  (optional)
let source = "source_example" // String |  (optional)

V4DeviceEventsAPI.deviceEventGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** |  | [optional] [default to &quot;timestamp_desc&quot;]
 **device** | **String** |  | [optional] 
 **source** | **String** |  | [optional] 

### Return type

[**PaginatedResponseOfDeviceEvent**](PaginatedResponseOfDeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceEventGetById**
```swift
    open class func deviceEventGetById(id: String, completion: @escaping (_ data: DeviceEvent?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4DeviceEventsAPI.deviceEventGetById(id: id) { (response, error) in
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
 **id** | **String** |  | 

### Return type

[**DeviceEvent**](DeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceEventUpdate**
```swift
    open class func deviceEventUpdate(id: String, upsertDeviceEventRequest: UpsertDeviceEventRequest, completion: @escaping (_ data: DeviceEvent?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertDeviceEventRequest = UpsertDeviceEventRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", eventType: DeviceEventType(), notes: "notes_example", syncIdentifier: "syncIdentifier_example") // UpsertDeviceEventRequest | 

V4DeviceEventsAPI.deviceEventUpdate(id: id, upsertDeviceEventRequest: upsertDeviceEventRequest) { (response, error) in
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
 **id** | **String** |  | 
 **upsertDeviceEventRequest** | [**UpsertDeviceEventRequest**](UpsertDeviceEventRequest.md) |  | 

### Return type

[**DeviceEvent**](DeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

