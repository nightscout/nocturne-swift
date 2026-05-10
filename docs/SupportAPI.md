# SupportAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**supportCreateIssue**](SupportAPI.md#supportcreateissue) | **POST** /api/v4/support/issues | 
[**supportGetFallbackUrl**](SupportAPI.md#supportgetfallbackurl) | **GET** /api/v4/support/issues/fallback-url | Returns a pre-filled GitHub new-issue URL for fallback when the API is unavailable.
[**supportGetSupportConfig**](SupportAPI.md#supportgetsupportconfig) | **GET** /api/v4/support/config | Returns operator support configuration for the frontend. When no operator is configured, accountBilling is null and the default GitHub flow applies.


# **supportCreateIssue**
```swift
    open class func supportCreateIssue(template: String? = nil, title: String? = nil, description: String? = nil, stepsToReproduce: String? = nil, expectedBehavior: String? = nil, actualBehavior: String? = nil, cgmSource: String? = nil, timeRange: String? = nil, diagnosticInfo: String? = nil, images: [URL]? = nil, completion: @escaping (_ data: CreateIssueResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let template = "template_example" // String |  (optional)
let title = "title_example" // String |  (optional)
let description = "description_example" // String |  (optional)
let stepsToReproduce = "stepsToReproduce_example" // String |  (optional)
let expectedBehavior = "expectedBehavior_example" // String |  (optional)
let actualBehavior = "actualBehavior_example" // String |  (optional)
let cgmSource = "cgmSource_example" // String |  (optional)
let timeRange = "timeRange_example" // String |  (optional)
let diagnosticInfo = "diagnosticInfo_example" // String |  (optional)
let images = [URL(string: "https://example.com")!] // [URL] |  (optional)

SupportAPI.supportCreateIssue(template: template, title: title, description: description, stepsToReproduce: stepsToReproduce, expectedBehavior: expectedBehavior, actualBehavior: actualBehavior, cgmSource: cgmSource, timeRange: timeRange, diagnosticInfo: diagnosticInfo, images: images) { (response, error) in
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
 **template** | **String** |  | [optional] 
 **title** | **String** |  | [optional] 
 **description** | **String** |  | [optional] 
 **stepsToReproduce** | **String** |  | [optional] 
 **expectedBehavior** | **String** |  | [optional] 
 **actualBehavior** | **String** |  | [optional] 
 **cgmSource** | **String** |  | [optional] 
 **timeRange** | **String** |  | [optional] 
 **diagnosticInfo** | **String** |  | [optional] 
 **images** | [**[URL]**](URL.md) |  | [optional] 

### Return type

[**CreateIssueResponse**](CreateIssueResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **supportGetFallbackUrl**
```swift
    open class func supportGetFallbackUrl(template: String? = nil, title: String? = nil, body: String? = nil, completion: @escaping (_ data: FallbackUrlResponse?, _ error: Error?) -> Void)
```

Returns a pre-filled GitHub new-issue URL for fallback when the API is unavailable.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let template = "template_example" // String |  (optional)
let title = "title_example" // String |  (optional)
let body = "body_example" // String |  (optional)

// Returns a pre-filled GitHub new-issue URL for fallback when the API is unavailable.
SupportAPI.supportGetFallbackUrl(template: template, title: title, body: body) { (response, error) in
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
 **template** | **String** |  | [optional] 
 **title** | **String** |  | [optional] 
 **body** | **String** |  | [optional] 

### Return type

[**FallbackUrlResponse**](FallbackUrlResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **supportGetSupportConfig**
```swift
    open class func supportGetSupportConfig(completion: @escaping (_ data: SupportConfigResponse?, _ error: Error?) -> Void)
```

Returns operator support configuration for the frontend. When no operator is configured, accountBilling is null and the default GitHub flow applies.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Returns operator support configuration for the frontend. When no operator is configured, accountBilling is null and the default GitHub flow applies.
SupportAPI.supportGetSupportConfig() { (response, error) in
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

[**SupportConfigResponse**](SupportConfigResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

