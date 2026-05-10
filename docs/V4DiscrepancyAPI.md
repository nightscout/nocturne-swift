# V4DiscrepancyAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**discrepancyGetCompatibilityMetrics**](V4DiscrepancyAPI.md#discrepancygetcompatibilitymetrics) | **GET** /api/v4/Discrepancy/metrics | Get overall compatibility metrics for dashboard overview
[**discrepancyGetCompatibilityStatus**](V4DiscrepancyAPI.md#discrepancygetcompatibilitystatus) | **GET** /api/v4/Discrepancy/status | Get real-time compatibility status summary
[**discrepancyGetDiscrepancyAnalyses**](V4DiscrepancyAPI.md#discrepancygetdiscrepancyanalyses) | **GET** /api/v4/Discrepancy/analyses | Get detailed discrepancy analyses with filtering and pagination
[**discrepancyGetDiscrepancyAnalysis**](V4DiscrepancyAPI.md#discrepancygetdiscrepancyanalysis) | **GET** /api/v4/Discrepancy/analyses/{id} | Get a specific discrepancy analysis by ID
[**discrepancyGetEndpointMetrics**](V4DiscrepancyAPI.md#discrepancygetendpointmetrics) | **GET** /api/v4/Discrepancy/endpoints | Get per-endpoint compatibility metrics
[**discrepancyIngestDiscrepancy**](V4DiscrepancyAPI.md#discrepancyingestdiscrepancy) | **POST** /api/v4/Discrepancy/ingest | Receive forwarded discrepancies from remote Nocturne instances


# **discrepancyGetCompatibilityMetrics**
```swift
    open class func discrepancyGetCompatibilityMetrics(fromDate: Date? = nil, toDate: Date? = nil, completion: @escaping (_ data: CompatibilityMetrics?, _ error: Error?) -> Void)
```

Get overall compatibility metrics for dashboard overview

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let fromDate = Date() // Date | Start date for metrics (optional) (optional)
let toDate = Date() // Date | End date for metrics (optional) (optional)

// Get overall compatibility metrics for dashboard overview
V4DiscrepancyAPI.discrepancyGetCompatibilityMetrics(fromDate: fromDate, toDate: toDate) { (response, error) in
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
 **fromDate** | **Date** | Start date for metrics (optional) | [optional] 
 **toDate** | **Date** | End date for metrics (optional) | [optional] 

### Return type

[**CompatibilityMetrics**](CompatibilityMetrics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **discrepancyGetCompatibilityStatus**
```swift
    open class func discrepancyGetCompatibilityStatus(completion: @escaping (_ data: CompatibilityStatus?, _ error: Error?) -> Void)
```

Get real-time compatibility status summary

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get real-time compatibility status summary
V4DiscrepancyAPI.discrepancyGetCompatibilityStatus() { (response, error) in
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

[**CompatibilityStatus**](CompatibilityStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **discrepancyGetDiscrepancyAnalyses**
```swift
    open class func discrepancyGetDiscrepancyAnalyses(requestPath: String? = nil, overallMatch: Int? = nil, fromDate: Date? = nil, toDate: Date? = nil, count: Int? = nil, skip: Int? = nil, completion: @escaping (_ data: [DiscrepancyAnalysisDto]?, _ error: Error?) -> Void)
```

Get detailed discrepancy analyses with filtering and pagination

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let requestPath = "requestPath_example" // String | Filter by request path (optional) (optional)
let overallMatch = 987 // Int | Filter by overall match type (optional) (optional)
let fromDate = Date() // Date | Start date for filter (optional) (optional)
let toDate = Date() // Date | End date for filter (optional) (optional)
let count = 987 // Int | Number of results to return (default: 100, max: 1000) (optional) (default to 100)
let skip = 987 // Int | Number of results to skip for pagination (default: 0) (optional) (default to 0)

// Get detailed discrepancy analyses with filtering and pagination
V4DiscrepancyAPI.discrepancyGetDiscrepancyAnalyses(requestPath: requestPath, overallMatch: overallMatch, fromDate: fromDate, toDate: toDate, count: count, skip: skip) { (response, error) in
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
 **requestPath** | **String** | Filter by request path (optional) | [optional] 
 **overallMatch** | **Int** | Filter by overall match type (optional) | [optional] 
 **fromDate** | **Date** | Start date for filter (optional) | [optional] 
 **toDate** | **Date** | End date for filter (optional) | [optional] 
 **count** | **Int** | Number of results to return (default: 100, max: 1000) | [optional] [default to 100]
 **skip** | **Int** | Number of results to skip for pagination (default: 0) | [optional] [default to 0]

### Return type

[**[DiscrepancyAnalysisDto]**](DiscrepancyAnalysisDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **discrepancyGetDiscrepancyAnalysis**
```swift
    open class func discrepancyGetDiscrepancyAnalysis(id: String, completion: @escaping (_ data: DiscrepancyAnalysisDto?, _ error: Error?) -> Void)
```

Get a specific discrepancy analysis by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Analysis ID

// Get a specific discrepancy analysis by ID
V4DiscrepancyAPI.discrepancyGetDiscrepancyAnalysis(id: id) { (response, error) in
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
 **id** | **String** | Analysis ID | 

### Return type

[**DiscrepancyAnalysisDto**](DiscrepancyAnalysisDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **discrepancyGetEndpointMetrics**
```swift
    open class func discrepancyGetEndpointMetrics(fromDate: Date? = nil, toDate: Date? = nil, completion: @escaping (_ data: [EndpointMetrics]?, _ error: Error?) -> Void)
```

Get per-endpoint compatibility metrics

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let fromDate = Date() // Date | Start date for metrics (optional) (optional)
let toDate = Date() // Date | End date for metrics (optional) (optional)

// Get per-endpoint compatibility metrics
V4DiscrepancyAPI.discrepancyGetEndpointMetrics(fromDate: fromDate, toDate: toDate) { (response, error) in
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
 **fromDate** | **Date** | Start date for metrics (optional) | [optional] 
 **toDate** | **Date** | End date for metrics (optional) | [optional] 

### Return type

[**[EndpointMetrics]**](EndpointMetrics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **discrepancyIngestDiscrepancy**
```swift
    open class func discrepancyIngestDiscrepancy(forwardedDiscrepancyDto: ForwardedDiscrepancyDto, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Receive forwarded discrepancies from remote Nocturne instances

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let forwardedDiscrepancyDto = ForwardedDiscrepancyDto(sourceId: "sourceId_example", receivedAt: Date(), analysis: DiscrepancyAnalysisDto(id: "id_example", correlationId: "correlationId_example", analysisTimestamp: Date(), requestMethod: "requestMethod_example", requestPath: "requestPath_example", overallMatch: 123, statusCodeMatch: false, bodyMatch: false, nightscoutStatusCode: 123, nocturneStatusCode: 123, nightscoutResponseTimeMs: 123, nocturneResponseTimeMs: 123, totalProcessingTimeMs: 123, summary: "summary_example", selectedResponseTarget: "selectedResponseTarget_example", selectionReason: "selectionReason_example", criticalDiscrepancyCount: 123, majorDiscrepancyCount: 123, minorDiscrepancyCount: 123, nightscoutMissing: false, nocturneMissing: false, errorMessage: "errorMessage_example", discrepancies: [DiscrepancyDetailDto(id: "id_example", discrepancyType: DiscrepancyType(), severity: DiscrepancySeverity(), field: "field_example", nightscoutValue: "nightscoutValue_example", nocturneValue: "nocturneValue_example", description: "description_example", recordedAt: Date())])) // ForwardedDiscrepancyDto | The forwarded discrepancy data

// Receive forwarded discrepancies from remote Nocturne instances
V4DiscrepancyAPI.discrepancyIngestDiscrepancy(forwardedDiscrepancyDto: forwardedDiscrepancyDto) { (response, error) in
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
 **forwardedDiscrepancyDto** | [**ForwardedDiscrepancyDto**](ForwardedDiscrepancyDto.md) | The forwarded discrepancy data | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

