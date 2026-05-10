# ChartDataAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chartDataGetDashboardChartData**](ChartDataAPI.md#chartdatagetdashboardchartdata) | **GET** /api/v4/ChartData/dashboard | Gets complete dashboard chart data in a single call. Returns pre-calculated IOB, COB, basal series, categorized treatment markers, state spans, system events, tracker markers, and glucose readings.


# **chartDataGetDashboardChartData**
```swift
    open class func chartDataGetDashboardChartData(startTime: Int64? = nil, endTime: Int64? = nil, intervalMinutes: Int? = nil, completion: @escaping (_ data: DashboardChartData?, _ error: Error?) -> Void)
```

Gets complete dashboard chart data in a single call. Returns pre-calculated IOB, COB, basal series, categorized treatment markers, state spans, system events, tracker markers, and glucose readings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startTime = 987 // Int64 | Start of the requested window as a Unix timestamp in milliseconds. (optional)
let endTime = 987 // Int64 | End of the requested window as a Unix timestamp in milliseconds.             Must be greater than startTime. (optional)
let intervalMinutes = 987 // Int | Granularity of the returned series in minutes (1–60, default 5). (optional) (default to 5)

// Gets complete dashboard chart data in a single call. Returns pre-calculated IOB, COB, basal series, categorized treatment markers, state spans, system events, tracker markers, and glucose readings.
ChartDataAPI.chartDataGetDashboardChartData(startTime: startTime, endTime: endTime, intervalMinutes: intervalMinutes) { (response, error) in
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
 **startTime** | **Int64** | Start of the requested window as a Unix timestamp in milliseconds. | [optional] 
 **endTime** | **Int64** | End of the requested window as a Unix timestamp in milliseconds.             Must be greater than startTime. | [optional] 
 **intervalMinutes** | **Int** | Granularity of the returned series in minutes (1–60, default 5). | [optional] [default to 5]

### Return type

[**DashboardChartData**](DashboardChartData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

