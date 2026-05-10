# NotificationsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**notificationsCreateNotification**](NotificationsAPI.md#notificationscreatenotification) | **POST** /api/v4/notifications | Create a notification programmatically (for integrations and services)
[**notificationsDismissNotification**](NotificationsAPI.md#notificationsdismissnotification) | **DELETE** /api/v4/notifications/{id} | 
[**notificationsExecuteAction**](NotificationsAPI.md#notificationsexecuteaction) | **POST** /api/v4/notifications/{id}/actions/{actionId} | 
[**notificationsGetNotifications**](NotificationsAPI.md#notificationsgetnotifications) | **GET** /api/v4/notifications | 


# **notificationsCreateNotification**
```swift
    open class func notificationsCreateNotification(createNotificationRequest: CreateNotificationRequest, completion: @escaping (_ data: InAppNotificationDto?, _ error: Error?) -> Void)
```

Create a notification programmatically (for integrations and services)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createNotificationRequest = CreateNotificationRequest(type: "type_example", title: "title_example", category: NotificationCategory(), urgency: NotificationUrgency(), subtitle: "subtitle_example", sourceId: "sourceId_example", icon: "icon_example", source: "source_example", actions: [NotificationActionDto(actionId: "actionId_example", label: "label_example", icon: "icon_example", variant: "variant_example")], resolutionConditions: ResolutionConditions(expiresAt: Date(), sourceDeletedType: "sourceDeletedType_example", glucose: GlucoseCondition(aboveMgDl: 123, belowMgDl: 123, sustainedMinutes: 123)), metadata: "TODO") // CreateNotificationRequest | 

// Create a notification programmatically (for integrations and services)
NotificationsAPI.notificationsCreateNotification(createNotificationRequest: createNotificationRequest) { (response, error) in
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
 **createNotificationRequest** | [**CreateNotificationRequest**](CreateNotificationRequest.md) |  | 

### Return type

[**InAppNotificationDto**](InAppNotificationDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **notificationsDismissNotification**
```swift
    open class func notificationsDismissNotification(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

NotificationsAPI.notificationsDismissNotification(id: id) { (response, error) in
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

# **notificationsExecuteAction**
```swift
    open class func notificationsExecuteAction(id: String, actionId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let actionId = "actionId_example" // String | 

NotificationsAPI.notificationsExecuteAction(id: id, actionId: actionId) { (response, error) in
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
 **actionId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **notificationsGetNotifications**
```swift
    open class func notificationsGetNotifications(completion: @escaping (_ data: [InAppNotificationDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


NotificationsAPI.notificationsGetNotifications() { (response, error) in
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

[**[InAppNotificationDto]**](InAppNotificationDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

