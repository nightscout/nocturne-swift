# WebhookSettingsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**webhookSettingsGetWebhookSettings**](WebhookSettingsAPI.md#webhooksettingsgetwebhooksettings) | **GET** /api/v4/ui-settings/notifications/webhooks | Gets the webhook notification settings for the current tenant.
[**webhookSettingsSaveWebhookSettings**](WebhookSettingsAPI.md#webhooksettingssavewebhooksettings) | **PUT** /api/v4/ui-settings/notifications/webhooks | Saves webhook notification settings.
[**webhookSettingsTestWebhookSettings**](WebhookSettingsAPI.md#webhooksettingstestwebhooksettings) | **POST** /api/v4/ui-settings/notifications/webhooks/test | Tests webhook settings by sending test payloads to configured URLs.


# **webhookSettingsGetWebhookSettings**
```swift
    open class func webhookSettingsGetWebhookSettings(completion: @escaping (_ data: WebhookNotificationSettings?, _ error: Error?) -> Void)
```

Gets the webhook notification settings for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets the webhook notification settings for the current tenant.
WebhookSettingsAPI.webhookSettingsGetWebhookSettings() { (response, error) in
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

[**WebhookNotificationSettings**](WebhookNotificationSettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhookSettingsSaveWebhookSettings**
```swift
    open class func webhookSettingsSaveWebhookSettings(webhookNotificationSettings: WebhookNotificationSettings, completion: @escaping (_ data: WebhookNotificationSettings?, _ error: Error?) -> Void)
```

Saves webhook notification settings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let webhookNotificationSettings = WebhookNotificationSettings(enabled: false, urls: ["urls_example"], secret: "secret_example", hasSecret: false, signatureVersion: "signatureVersion_example") // WebhookNotificationSettings | 

// Saves webhook notification settings.
WebhookSettingsAPI.webhookSettingsSaveWebhookSettings(webhookNotificationSettings: webhookNotificationSettings) { (response, error) in
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
 **webhookNotificationSettings** | [**WebhookNotificationSettings**](WebhookNotificationSettings.md) |  | 

### Return type

[**WebhookNotificationSettings**](WebhookNotificationSettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhookSettingsTestWebhookSettings**
```swift
    open class func webhookSettingsTestWebhookSettings(webhookTestRequest: WebhookTestRequest, completion: @escaping (_ data: WebhookTestResult?, _ error: Error?) -> Void)
```

Tests webhook settings by sending test payloads to configured URLs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let webhookTestRequest = WebhookTestRequest(urls: ["urls_example"], secret: "secret_example") // WebhookTestRequest | 

// Tests webhook settings by sending test payloads to configured URLs.
WebhookSettingsAPI.webhookSettingsTestWebhookSettings(webhookTestRequest: webhookTestRequest) { (response, error) in
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
 **webhookTestRequest** | [**WebhookTestRequest**](WebhookTestRequest.md) |  | 

### Return type

[**WebhookTestResult**](WebhookTestResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

