# V4NotificationsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**notificationsDismissNotification**](V4NotificationsAPI.md#notificationsdismissnotification) | **DELETE** /api/v4/notifications/{id} | Dismiss a notification (archive with dismissed reason)
[**notificationsExecuteAction**](V4NotificationsAPI.md#notificationsexecuteaction) | **POST** /api/v4/notifications/{id}/actions/{actionId} | Execute an action on a notification
[**notificationsGetNotifications**](V4NotificationsAPI.md#notificationsgetnotifications) | **GET** /api/v4/notifications | Get all active notifications for the current user


# **notificationsDismissNotification**
```swift
    open class func notificationsDismissNotification(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Dismiss a notification (archive with dismissed reason)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The notification ID to dismiss

// Dismiss a notification (archive with dismissed reason)
V4NotificationsAPI.notificationsDismissNotification(id: id) { (response, error) in
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
 **id** | **String** | The notification ID to dismiss | 

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

Execute an action on a notification

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The notification ID
let actionId = "actionId_example" // String | The action ID to execute

// Execute an action on a notification
V4NotificationsAPI.notificationsExecuteAction(id: id, actionId: actionId) { (response, error) in
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
 **id** | **String** | The notification ID | 
 **actionId** | **String** | The action ID to execute | 

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

Get all active notifications for the current user

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all active notifications for the current user
V4NotificationsAPI.notificationsGetNotifications() { (response, error) in
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

