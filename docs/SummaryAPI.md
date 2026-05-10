# SummaryAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**summaryGetSummary**](SummaryAPI.md#summarygetsummary) | **GET** /api/v4/summary | Get widget-friendly summary data including current glucose, IOB, COB, trackers, and alarm state.


# **summaryGetSummary**
```swift
    open class func summaryGetSummary(hours: Int? = nil, includePredictions: Bool? = nil, completion: @escaping (_ data: V4SummaryResponse?, _ error: Error?) -> Void)
```

Get widget-friendly summary data including current glucose, IOB, COB, trackers, and alarm state.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let hours = 987 // Int | Number of hours of glucose history to include (default 0 for current reading only) (optional) (default to 0)
let includePredictions = true // Bool | Whether to include predicted glucose values (default false) (optional) (default to false)

// Get widget-friendly summary data including current glucose, IOB, COB, trackers, and alarm state.
SummaryAPI.summaryGetSummary(hours: hours, includePredictions: includePredictions) { (response, error) in
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
 **hours** | **Int** | Number of hours of glucose history to include (default 0 for current reading only) | [optional] [default to 0]
 **includePredictions** | **Bool** | Whether to include predicted glucose values (default false) | [optional] [default to false]

### Return type

[**V4SummaryResponse**](V4SummaryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

