# GlucoseProcessingSettingsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**glucoseProcessingSettingsGetPreference**](GlucoseProcessingSettingsAPI.md#glucoseprocessingsettingsgetpreference) | **GET** /api/v4/settings/glucose-processing/preference | 
[**glucoseProcessingSettingsGetSourceDefaults**](GlucoseProcessingSettingsAPI.md#glucoseprocessingsettingsgetsourcedefaults) | **GET** /api/v4/settings/glucose-processing/source-defaults | 
[**glucoseProcessingSettingsSetPreference**](GlucoseProcessingSettingsAPI.md#glucoseprocessingsettingssetpreference) | **PUT** /api/v4/settings/glucose-processing/preference | 
[**glucoseProcessingSettingsSetSourceDefaults**](GlucoseProcessingSettingsAPI.md#glucoseprocessingsettingssetsourcedefaults) | **PUT** /api/v4/settings/glucose-processing/source-defaults | 


# **glucoseProcessingSettingsGetPreference**
```swift
    open class func glucoseProcessingSettingsGetPreference(completion: @escaping (_ data: GlucoseProcessingPreferenceResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


GlucoseProcessingSettingsAPI.glucoseProcessingSettingsGetPreference() { (response, error) in
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

[**GlucoseProcessingPreferenceResponse**](GlucoseProcessingPreferenceResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **glucoseProcessingSettingsGetSourceDefaults**
```swift
    open class func glucoseProcessingSettingsGetSourceDefaults(completion: @escaping (_ data: GlucoseProcessingSourceDefaultsResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


GlucoseProcessingSettingsAPI.glucoseProcessingSettingsGetSourceDefaults() { (response, error) in
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

[**GlucoseProcessingSourceDefaultsResponse**](GlucoseProcessingSourceDefaultsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **glucoseProcessingSettingsSetPreference**
```swift
    open class func glucoseProcessingSettingsSetPreference(setGlucoseProcessingPreferenceRequest: SetGlucoseProcessingPreferenceRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let setGlucoseProcessingPreferenceRequest = SetGlucoseProcessingPreferenceRequest(preferredGlucoseProcessing: "preferredGlucoseProcessing_example") // SetGlucoseProcessingPreferenceRequest | 

GlucoseProcessingSettingsAPI.glucoseProcessingSettingsSetPreference(setGlucoseProcessingPreferenceRequest: setGlucoseProcessingPreferenceRequest) { (response, error) in
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
 **setGlucoseProcessingPreferenceRequest** | [**SetGlucoseProcessingPreferenceRequest**](SetGlucoseProcessingPreferenceRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **glucoseProcessingSettingsSetSourceDefaults**
```swift
    open class func glucoseProcessingSettingsSetSourceDefaults(setGlucoseProcessingSourceDefaultsRequest: SetGlucoseProcessingSourceDefaultsRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let setGlucoseProcessingSourceDefaultsRequest = SetGlucoseProcessingSourceDefaultsRequest(rules: [GlucoseProcessingSourceDefault(match: "match_example", field: "field_example", processing: GlucoseProcessing())]) // SetGlucoseProcessingSourceDefaultsRequest | 

GlucoseProcessingSettingsAPI.glucoseProcessingSettingsSetSourceDefaults(setGlucoseProcessingSourceDefaultsRequest: setGlucoseProcessingSourceDefaultsRequest) { (response, error) in
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
 **setGlucoseProcessingSourceDefaultsRequest** | [**SetGlucoseProcessingSourceDefaultsRequest**](SetGlucoseProcessingSourceDefaultsRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

