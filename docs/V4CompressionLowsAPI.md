# V4CompressionLowsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**compressionLowAcceptSuggestion**](V4CompressionLowsAPI.md#compressionlowacceptsuggestion) | **POST** /api/v4/compression-lows/suggestions/{id}/accept | Accept a suggestion with adjusted bounds
[**compressionLowDeleteSuggestion**](V4CompressionLowsAPI.md#compressionlowdeletesuggestion) | **DELETE** /api/v4/compression-lows/suggestions/{id} | Delete a suggestion and its associated state span
[**compressionLowDismissSuggestion**](V4CompressionLowsAPI.md#compressionlowdismisssuggestion) | **POST** /api/v4/compression-lows/suggestions/{id}/dismiss | Dismiss a suggestion
[**compressionLowGetSuggestion**](V4CompressionLowsAPI.md#compressionlowgetsuggestion) | **GET** /api/v4/compression-lows/suggestions/{id} | Get a single suggestion with glucose entries for charting
[**compressionLowGetSuggestions**](V4CompressionLowsAPI.md#compressionlowgetsuggestions) | **GET** /api/v4/compression-lows/suggestions | Get compression low suggestions with optional filtering
[**compressionLowTriggerDetection**](V4CompressionLowsAPI.md#compressionlowtriggerdetection) | **POST** /api/v4/compression-lows/detect | Manually trigger detection for a date range (for testing)


# **compressionLowAcceptSuggestion**
```swift
    open class func compressionLowAcceptSuggestion(id: String, acceptSuggestionRequest: AcceptSuggestionRequest, completion: @escaping (_ data: StateSpan?, _ error: Error?) -> Void)
```

Accept a suggestion with adjusted bounds

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let acceptSuggestionRequest = AcceptSuggestionRequest(startMills: 123, endMills: 123) // AcceptSuggestionRequest | 

// Accept a suggestion with adjusted bounds
V4CompressionLowsAPI.compressionLowAcceptSuggestion(id: id, acceptSuggestionRequest: acceptSuggestionRequest) { (response, error) in
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
 **acceptSuggestionRequest** | [**AcceptSuggestionRequest**](AcceptSuggestionRequest.md) |  | 

### Return type

[**StateSpan**](StateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compressionLowDeleteSuggestion**
```swift
    open class func compressionLowDeleteSuggestion(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a suggestion and its associated state span

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a suggestion and its associated state span
V4CompressionLowsAPI.compressionLowDeleteSuggestion(id: id) { (response, error) in
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

# **compressionLowDismissSuggestion**
```swift
    open class func compressionLowDismissSuggestion(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Dismiss a suggestion

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Dismiss a suggestion
V4CompressionLowsAPI.compressionLowDismissSuggestion(id: id) { (response, error) in
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

# **compressionLowGetSuggestion**
```swift
    open class func compressionLowGetSuggestion(id: String, completion: @escaping (_ data: CompressionLowSuggestionWithEntries?, _ error: Error?) -> Void)
```

Get a single suggestion with glucose entries for charting

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a single suggestion with glucose entries for charting
V4CompressionLowsAPI.compressionLowGetSuggestion(id: id) { (response, error) in
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

[**CompressionLowSuggestionWithEntries**](CompressionLowSuggestionWithEntries.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compressionLowGetSuggestions**
```swift
    open class func compressionLowGetSuggestions(status: CompressionLowGetSuggestionsStatusParameter? = nil, nightOf: String? = nil, completion: @escaping (_ data: [CompressionLowSuggestion]?, _ error: Error?) -> Void)
```

Get compression low suggestions with optional filtering

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let status = CompressionLow_GetSuggestions_status_parameter() // CompressionLowGetSuggestionsStatusParameter |  (optional)
let nightOf = "nightOf_example" // String |  (optional)

// Get compression low suggestions with optional filtering
V4CompressionLowsAPI.compressionLowGetSuggestions(status: status, nightOf: nightOf) { (response, error) in
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
 **status** | [**CompressionLowGetSuggestionsStatusParameter**](.md) |  | [optional] 
 **nightOf** | **String** |  | [optional] 

### Return type

[**[CompressionLowSuggestion]**](CompressionLowSuggestion.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compressionLowTriggerDetection**
```swift
    open class func compressionLowTriggerDetection(triggerDetectionRequest: TriggerDetectionRequest, completion: @escaping (_ data: DetectionResult?, _ error: Error?) -> Void)
```

Manually trigger detection for a date range (for testing)

Provide either a single `nightOf` date or a range with `startDate` and `endDate`. When using a range, detection runs for each night in the range (inclusive).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let triggerDetectionRequest = TriggerDetectionRequest(nightOf: "nightOf_example", startDate: "startDate_example", endDate: "endDate_example") // TriggerDetectionRequest | 

// Manually trigger detection for a date range (for testing)
V4CompressionLowsAPI.compressionLowTriggerDetection(triggerDetectionRequest: triggerDetectionRequest) { (response, error) in
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
 **triggerDetectionRequest** | [**TriggerDetectionRequest**](TriggerDetectionRequest.md) |  | 

### Return type

[**DetectionResult**](DetectionResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

