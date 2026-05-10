# V4DebugAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**debugCreateSimpleTestNotification**](V4DebugAPI.md#debugcreatesimpletestnotification) | **GET** /api/v4/debug/test/notification | Simple test endpoint for creating in-app notifications without authentication Creates a test notification to verify the real-time notification system is working
[**debugCreateTestNotification**](V4DebugAPI.md#debugcreatetestnotification) | **POST** /api/v4/debug/test/inappnotification | Test endpoint for creating in-app notifications (development only) Creates a test notification for the current user to verify the notification system
[**debugEchoQuery**](V4DebugAPI.md#debugechoquery) | **GET** /api/v4/debug/echo/{echo} | Echo endpoint for debugging MongoDB queries Returns information about how REST API parameters translate into MongoDB queries
[**debugEchoQueryWithModel**](V4DebugAPI.md#debugechoquerywithmodel) | **GET** /api/v4/debug/echo/{echo}/{model} | Echo endpoint for debugging MongoDB queries with model Returns information about how REST API parameters translate into MongoDB queries
[**debugEchoQueryWithModelAndSpec**](V4DebugAPI.md#debugechoquerywithmodelandspec) | **GET** /api/v4/debug/echo/{echo}/{model}/{spec} | Echo endpoint for debugging MongoDB queries with model and spec Returns information about how REST API parameters translate into MongoDB queries
[**debugPreviewEntries**](V4DebugAPI.md#debugpreviewentries) | **POST** /api/v4/debug/entries/preview | Preview endpoint for entry creation without persistence Allows previewing entry data without actually storing it in the database
[**debugTestSignalRBroadcast**](V4DebugAPI.md#debugtestsignalrbroadcast) | **GET** /api/v4/debug/test/signalr-broadcast | Test endpoint to broadcast a raw SignalR notification event This bypasses the database and directly tests the SignalR broadcast


# **debugCreateSimpleTestNotification**
```swift
    open class func debugCreateSimpleTestNotification(type: String? = nil, title: String? = nil, completion: @escaping (_ data: InAppNotificationDto?, _ error: Error?) -> Void)
```

Simple test endpoint for creating in-app notifications without authentication Creates a test notification to verify the real-time notification system is working

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let type = "type_example" // String | Notification type (info, warn, hazard, urgent) (optional) (default to "info")
let title = "title_example" // String | Optional notification title (optional)

// Simple test endpoint for creating in-app notifications without authentication Creates a test notification to verify the real-time notification system is working
V4DebugAPI.debugCreateSimpleTestNotification(type: type, title: title) { (response, error) in
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
 **type** | **String** | Notification type (info, warn, hazard, urgent) | [optional] [default to &quot;info&quot;]
 **title** | **String** | Optional notification title | [optional] 

### Return type

[**InAppNotificationDto**](InAppNotificationDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugCreateTestNotification**
```swift
    open class func debugCreateTestNotification(testNotificationRequest: TestNotificationRequest, completion: @escaping (_ data: InAppNotificationDto?, _ error: Error?) -> Void)
```

Test endpoint for creating in-app notifications (development only) Creates a test notification for the current user to verify the notification system

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let testNotificationRequest = TestNotificationRequest(type: InAppNotificationType(), urgency: NotificationUrgency(), title: "title_example", subtitle: "subtitle_example", sourceId: "sourceId_example", actions: [NotificationActionDto(actionId: "actionId_example", label: "label_example", icon: "icon_example", variant: "variant_example")], resolutionConditions: ResolutionConditions(expiresAt: Date(), sourceDeletedType: "sourceDeletedType_example", glucose: GlucoseCondition(aboveMgDl: 123, belowMgDl: 123, sustainedMinutes: 123)), metadata: "TODO") // TestNotificationRequest | The test notification parameters

// Test endpoint for creating in-app notifications (development only) Creates a test notification for the current user to verify the notification system
V4DebugAPI.debugCreateTestNotification(testNotificationRequest: testNotificationRequest) { (response, error) in
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
 **testNotificationRequest** | [**TestNotificationRequest**](TestNotificationRequest.md) | The test notification parameters | 

### Return type

[**InAppNotificationDto**](InAppNotificationDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugEchoQuery**
```swift
    open class func debugEchoQuery(echo: String, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Echo endpoint for debugging MongoDB queries Returns information about how REST API parameters translate into MongoDB queries

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let echo = "echo_example" // String | Storage type to query (entries, treatments, devicestatus, activity)

// Echo endpoint for debugging MongoDB queries Returns information about how REST API parameters translate into MongoDB queries
V4DebugAPI.debugEchoQuery(echo: echo) { (response, error) in
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
 **echo** | **String** | Storage type to query (entries, treatments, devicestatus, activity) | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugEchoQueryWithModel**
```swift
    open class func debugEchoQueryWithModel(echo: String, model: String, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Echo endpoint for debugging MongoDB queries with model Returns information about how REST API parameters translate into MongoDB queries

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let echo = "echo_example" // String | Storage type to query (entries, treatments, devicestatus, activity)
let model = "model_example" // String | Model specification

// Echo endpoint for debugging MongoDB queries with model Returns information about how REST API parameters translate into MongoDB queries
V4DebugAPI.debugEchoQueryWithModel(echo: echo, model: model) { (response, error) in
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
 **echo** | **String** | Storage type to query (entries, treatments, devicestatus, activity) | 
 **model** | **String** | Model specification | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugEchoQueryWithModelAndSpec**
```swift
    open class func debugEchoQueryWithModelAndSpec(echo: String, model: String, spec: String, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Echo endpoint for debugging MongoDB queries with model and spec Returns information about how REST API parameters translate into MongoDB queries

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let echo = "echo_example" // String | Storage type to query (entries, treatments, devicestatus, activity)
let model = "model_example" // String | Model specification
let spec = "spec_example" // String | Specification parameter

// Echo endpoint for debugging MongoDB queries with model and spec Returns information about how REST API parameters translate into MongoDB queries
V4DebugAPI.debugEchoQueryWithModelAndSpec(echo: echo, model: model, spec: spec) { (response, error) in
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
 **echo** | **String** | Storage type to query (entries, treatments, devicestatus, activity) | 
 **model** | **String** | Model specification | 
 **spec** | **String** | Specification parameter | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugPreviewEntries**
```swift
    open class func debugPreviewEntries(body: JSONValue, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Preview endpoint for entry creation without persistence Allows previewing entry data without actually storing it in the database

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let body =  // JSONValue | Entry data to preview (single object or array)

// Preview endpoint for entry creation without persistence Allows previewing entry data without actually storing it in the database
V4DebugAPI.debugPreviewEntries(body: body) { (response, error) in
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
 **body** | **JSONValue** | Entry data to preview (single object or array) | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugTestSignalRBroadcast**
```swift
    open class func debugTestSignalRBroadcast(completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Test endpoint to broadcast a raw SignalR notification event This bypasses the database and directly tests the SignalR broadcast

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Test endpoint to broadcast a raw SignalR notification event This bypasses the database and directly tests the SignalR broadcast
V4DebugAPI.debugTestSignalRBroadcast() { (response, error) in
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

