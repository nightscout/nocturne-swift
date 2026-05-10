# SystemEventsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**systemEventsCreateSystemEvent**](SystemEventsAPI.md#systemeventscreatesystemevent) | **POST** /api/v4/system-events | Create a new system event (manual entry or import).
[**systemEventsDeleteSystemEvent**](SystemEventsAPI.md#systemeventsdeletesystemevent) | **DELETE** /api/v4/system-events/{id} | Delete a system event.
[**systemEventsGetSystemEvent**](SystemEventsAPI.md#systemeventsgetsystemevent) | **GET** /api/v4/system-events/{id} | Get a specific system event by ID.
[**systemEventsGetSystemEvents**](SystemEventsAPI.md#systemeventsgetsystemevents) | **GET** /api/v4/system-events | Query system events with optional filtering.


# **systemEventsCreateSystemEvent**
```swift
    open class func systemEventsCreateSystemEvent(createSystemEventRequest: CreateSystemEventRequest, completion: @escaping (_ data: SystemEvent?, _ error: Error?) -> Void)
```

Create a new system event (manual entry or import).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createSystemEventRequest = CreateSystemEventRequest(eventType: SystemEventType(), category: SystemEventCategory(), code: "code_example", description: "description_example", mills: 123, source: "source_example", metadata: "TODO", originalId: "originalId_example") // CreateSystemEventRequest | 

// Create a new system event (manual entry or import).
SystemEventsAPI.systemEventsCreateSystemEvent(createSystemEventRequest: createSystemEventRequest) { (response, error) in
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
 **createSystemEventRequest** | [**CreateSystemEventRequest**](CreateSystemEventRequest.md) |  | 

### Return type

[**SystemEvent**](SystemEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **systemEventsDeleteSystemEvent**
```swift
    open class func systemEventsDeleteSystemEvent(id: String, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Delete a system event.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a system event.
SystemEventsAPI.systemEventsDeleteSystemEvent(id: id) { (response, error) in
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

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **systemEventsGetSystemEvent**
```swift
    open class func systemEventsGetSystemEvent(id: String, completion: @escaping (_ data: SystemEvent?, _ error: Error?) -> Void)
```

Get a specific system event by ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a specific system event by ID.
SystemEventsAPI.systemEventsGetSystemEvent(id: id) { (response, error) in
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

[**SystemEvent**](SystemEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **systemEventsGetSystemEvents**
```swift
    open class func systemEventsGetSystemEvents(type: SystemEventsGetSystemEventsTypeParameter? = nil, category: SystemEventsGetSystemEventsCategoryParameter? = nil, from: Date? = nil, to: Date? = nil, source: String? = nil, count: Int? = nil, skip: Int? = nil, completion: @escaping (_ data: [SystemEvent]?, _ error: Error?) -> Void)
```

Query system events with optional filtering.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let type = SystemEvents_GetSystemEvents_type_parameter() // SystemEventsGetSystemEventsTypeParameter |  (optional)
let category = SystemEvents_GetSystemEvents_category_parameter() // SystemEventsGetSystemEventsCategoryParameter |  (optional)
let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let source = "source_example" // String |  (optional)
let count = 987 // Int |  (optional) (default to 100)
let skip = 987 // Int |  (optional) (default to 0)

// Query system events with optional filtering.
SystemEventsAPI.systemEventsGetSystemEvents(type: type, category: category, from: from, to: to, source: source, count: count, skip: skip) { (response, error) in
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
 **type** | [**SystemEventsGetSystemEventsTypeParameter**](.md) |  | [optional] 
 **category** | [**SystemEventsGetSystemEventsCategoryParameter**](.md) |  | [optional] 
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **source** | **String** |  | [optional] 
 **count** | **Int** |  | [optional] [default to 100]
 **skip** | **Int** |  | [optional] [default to 0]

### Return type

[**[SystemEvent]**](SystemEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

