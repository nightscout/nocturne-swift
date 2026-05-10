# V4ConnectorSettingsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**myFitnessPalSettingsGetSettings**](V4ConnectorSettingsAPI.md#myfitnesspalsettingsgetsettings) | **GET** /api/v4/connectors/myfitnesspal/settings | Get global MyFitnessPal matching settings.
[**myFitnessPalSettingsSaveSettings**](V4ConnectorSettingsAPI.md#myfitnesspalsettingssavesettings) | **PUT** /api/v4/connectors/myfitnesspal/settings | Update global MyFitnessPal matching settings.


# **myFitnessPalSettingsGetSettings**
```swift
    open class func myFitnessPalSettingsGetSettings(completion: @escaping (_ data: MyFitnessPalMatchingSettings?, _ error: Error?) -> Void)
```

Get global MyFitnessPal matching settings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get global MyFitnessPal matching settings.
V4ConnectorSettingsAPI.myFitnessPalSettingsGetSettings() { (response, error) in
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

[**MyFitnessPalMatchingSettings**](MyFitnessPalMatchingSettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **myFitnessPalSettingsSaveSettings**
```swift
    open class func myFitnessPalSettingsSaveSettings(myFitnessPalMatchingSettings: MyFitnessPalMatchingSettings, completion: @escaping (_ data: MyFitnessPalMatchingSettings?, _ error: Error?) -> Void)
```

Update global MyFitnessPal matching settings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let myFitnessPalMatchingSettings = MyFitnessPalMatchingSettings(matchTimeWindowMinutes: 123, matchCarbTolerancePercent: 123, matchCarbToleranceGrams: 123, enableMatchNotifications: false) // MyFitnessPalMatchingSettings | 

// Update global MyFitnessPal matching settings.
V4ConnectorSettingsAPI.myFitnessPalSettingsSaveSettings(myFitnessPalMatchingSettings: myFitnessPalMatchingSettings) { (response, error) in
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
 **myFitnessPalMatchingSettings** | [**MyFitnessPalMatchingSettings**](MyFitnessPalMatchingSettings.md) |  | 

### Return type

[**MyFitnessPalMatchingSettings**](MyFitnessPalMatchingSettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

