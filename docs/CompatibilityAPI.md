# CompatibilityAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**compatibilityGetAnalyses**](CompatibilityAPI.md#compatibilitygetanalyses) | **GET** /api/v4/compatibility/analyses | Get list of analyses with filtering and pagination
[**compatibilityGetAnalysisDetail**](CompatibilityAPI.md#compatibilitygetanalysisdetail) | **GET** /api/v4/compatibility/analyses/{id} | Get detailed analysis by ID
[**compatibilityGetConfiguration**](CompatibilityAPI.md#compatibilitygetconfiguration) | **GET** /api/v4/compatibility/config | Get current proxy configuration
[**compatibilityGetEndpointMetrics**](CompatibilityAPI.md#compatibilitygetendpointmetrics) | **GET** /api/v4/compatibility/endpoints | Get per-endpoint compatibility metrics
[**compatibilityGetMetrics**](CompatibilityAPI.md#compatibilitygetmetrics) | **GET** /api/v4/compatibility/metrics | Get overall compatibility metrics
[**compatibilityTestApiComparison**](CompatibilityAPI.md#compatibilitytestapicomparison) | **POST** /api/v4/compatibility/test | Test API compatibility by comparing responses from Nightscout and Nocturne


# **compatibilityGetAnalyses**
```swift
    open class func compatibilityGetAnalyses(requestPath: String? = nil, overallMatch: CompatibilityGetAnalysesOverallMatchParameter? = nil, requestMethod: String? = nil, fromDate: Date? = nil, toDate: Date? = nil, count: Int? = nil, skip: Int? = nil, completion: @escaping (_ data: AnalysesListResponse?, _ error: Error?) -> Void)
```

Get list of analyses with filtering and pagination

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let requestPath = "requestPath_example" // String |  (optional)
let overallMatch = Compatibility_GetAnalyses_overallMatch_parameter() // CompatibilityGetAnalysesOverallMatchParameter |  (optional)
let requestMethod = "requestMethod_example" // String |  (optional)
let fromDate = Date() // Date |  (optional)
let toDate = Date() // Date |  (optional)
let count = 987 // Int |  (optional) (default to 100)
let skip = 987 // Int |  (optional) (default to 0)

// Get list of analyses with filtering and pagination
CompatibilityAPI.compatibilityGetAnalyses(requestPath: requestPath, overallMatch: overallMatch, requestMethod: requestMethod, fromDate: fromDate, toDate: toDate, count: count, skip: skip) { (response, error) in
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
 **requestPath** | **String** |  | [optional] 
 **overallMatch** | [**CompatibilityGetAnalysesOverallMatchParameter**](.md) |  | [optional] 
 **requestMethod** | **String** |  | [optional] 
 **fromDate** | **Date** |  | [optional] 
 **toDate** | **Date** |  | [optional] 
 **count** | **Int** |  | [optional] [default to 100]
 **skip** | **Int** |  | [optional] [default to 0]

### Return type

[**AnalysesListResponse**](AnalysesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compatibilityGetAnalysisDetail**
```swift
    open class func compatibilityGetAnalysisDetail(id: String, completion: @escaping (_ data: AnalysisDetailDto?, _ error: Error?) -> Void)
```

Get detailed analysis by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get detailed analysis by ID
CompatibilityAPI.compatibilityGetAnalysisDetail(id: id) { (response, error) in
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

[**AnalysisDetailDto**](AnalysisDetailDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compatibilityGetConfiguration**
```swift
    open class func compatibilityGetConfiguration(completion: @escaping (_ data: ProxyConfigurationDto?, _ error: Error?) -> Void)
```

Get current proxy configuration

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get current proxy configuration
CompatibilityAPI.compatibilityGetConfiguration() { (response, error) in
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

[**ProxyConfigurationDto**](ProxyConfigurationDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compatibilityGetEndpointMetrics**
```swift
    open class func compatibilityGetEndpointMetrics(fromDate: Date? = nil, toDate: Date? = nil, completion: @escaping (_ data: [EndpointMetrics]?, _ error: Error?) -> Void)
```

Get per-endpoint compatibility metrics

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let fromDate = Date() // Date |  (optional)
let toDate = Date() // Date |  (optional)

// Get per-endpoint compatibility metrics
CompatibilityAPI.compatibilityGetEndpointMetrics(fromDate: fromDate, toDate: toDate) { (response, error) in
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
 **fromDate** | **Date** |  | [optional] 
 **toDate** | **Date** |  | [optional] 

### Return type

[**[EndpointMetrics]**](EndpointMetrics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compatibilityGetMetrics**
```swift
    open class func compatibilityGetMetrics(fromDate: Date? = nil, toDate: Date? = nil, completion: @escaping (_ data: CompatibilityMetrics?, _ error: Error?) -> Void)
```

Get overall compatibility metrics

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let fromDate = Date() // Date |  (optional)
let toDate = Date() // Date |  (optional)

// Get overall compatibility metrics
CompatibilityAPI.compatibilityGetMetrics(fromDate: fromDate, toDate: toDate) { (response, error) in
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
 **fromDate** | **Date** |  | [optional] 
 **toDate** | **Date** |  | [optional] 

### Return type

[**CompatibilityMetrics**](CompatibilityMetrics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **compatibilityTestApiComparison**
```swift
    open class func compatibilityTestApiComparison(manualTestRequest: ManualTestRequest, completion: @escaping (_ data: ManualTestResult?, _ error: Error?) -> Void)
```

Test API compatibility by comparing responses from Nightscout and Nocturne

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let manualTestRequest = ManualTestRequest(nightscoutUrl: "nightscoutUrl_example", apiSecret: "apiSecret_example", queryPath: "queryPath_example", method: "method_example", requestBody: "requestBody_example") // ManualTestRequest | 

// Test API compatibility by comparing responses from Nightscout and Nocturne
CompatibilityAPI.compatibilityTestApiComparison(manualTestRequest: manualTestRequest) { (response, error) in
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
 **manualTestRequest** | [**ManualTestRequest**](ManualTestRequest.md) |  | 

### Return type

[**ManualTestResult**](ManualTestResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

