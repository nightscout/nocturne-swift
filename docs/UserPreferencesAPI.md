# UserPreferencesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**userPreferencesGetPreferences**](UserPreferencesAPI.md#userpreferencesgetpreferences) | **GET** /api/v4/user/preferences | Get the current user&#39;s preferences
[**userPreferencesUpdatePreferences**](UserPreferencesAPI.md#userpreferencesupdatepreferences) | **PATCH** /api/v4/user/preferences | Update the current user&#39;s preferences


# **userPreferencesGetPreferences**
```swift
    open class func userPreferencesGetPreferences(completion: @escaping (_ data: UserPreferencesResponse?, _ error: Error?) -> Void)
```

Get the current user's preferences

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get the current user's preferences
UserPreferencesAPI.userPreferencesGetPreferences() { (response, error) in
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

[**UserPreferencesResponse**](UserPreferencesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userPreferencesUpdatePreferences**
```swift
    open class func userPreferencesUpdatePreferences(updateUserPreferencesRequest: UpdateUserPreferencesRequest, completion: @escaping (_ data: UserPreferencesResponse?, _ error: Error?) -> Void)
```

Update the current user's preferences

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let updateUserPreferencesRequest = UpdateUserPreferencesRequest(preferredLanguage: "preferredLanguage_example") // UpdateUserPreferencesRequest | The preferences to update

// Update the current user's preferences
UserPreferencesAPI.userPreferencesUpdatePreferences(updateUserPreferencesRequest: updateUserPreferencesRequest) { (response, error) in
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
 **updateUserPreferencesRequest** | [**UpdateUserPreferencesRequest**](UpdateUserPreferencesRequest.md) | The preferences to update | 

### Return type

[**UserPreferencesResponse**](UserPreferencesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

