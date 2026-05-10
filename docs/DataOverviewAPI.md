# DataOverviewAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**dataOverviewGetAvailableYears**](DataOverviewAPI.md#dataoverviewgetavailableyears) | **GET** /api/v4/year-overview/years | Gets the list of calendar years that contain glucose data and the available data sources.
[**dataOverviewGetDailySummary**](DataOverviewAPI.md#dataoverviewgetdailysummary) | **GET** /api/v4/year-overview/daily-summary | Get day-level aggregated counts and average glucose for a given year
[**dataOverviewGetGriTimeline**](DataOverviewAPI.md#dataoverviewgetgritimeline) | **GET** /api/v4/year-overview/gri-timeline | Get monthly GRI (Glycemic Risk Index) scores for a given year


# **dataOverviewGetAvailableYears**
```swift
    open class func dataOverviewGetAvailableYears(completion: @escaping (_ data: DataOverviewYearsResponse?, _ error: Error?) -> Void)
```

Gets the list of calendar years that contain glucose data and the available data sources.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets the list of calendar years that contain glucose data and the available data sources.
DataOverviewAPI.dataOverviewGetAvailableYears() { (response, error) in
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

[**DataOverviewYearsResponse**](DataOverviewYearsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **dataOverviewGetDailySummary**
```swift
    open class func dataOverviewGetDailySummary(year: Int? = nil, dataSources: [String]? = nil, completion: @escaping (_ data: DailySummaryResponse?, _ error: Error?) -> Void)
```

Get day-level aggregated counts and average glucose for a given year

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let year = 987 // Int | The year to aggregate (optional)
let dataSources = ["inner_example"] // [String] | Optional data source filters (multiple allowed) (optional)

// Get day-level aggregated counts and average glucose for a given year
DataOverviewAPI.dataOverviewGetDailySummary(year: year, dataSources: dataSources) { (response, error) in
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
 **year** | **Int** | The year to aggregate | [optional] 
 **dataSources** | [**[String]**](String.md) | Optional data source filters (multiple allowed) | [optional] 

### Return type

[**DailySummaryResponse**](DailySummaryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **dataOverviewGetGriTimeline**
```swift
    open class func dataOverviewGetGriTimeline(year: Int? = nil, dataSources: [String]? = nil, completion: @escaping (_ data: GriTimelineResponse?, _ error: Error?) -> Void)
```

Get monthly GRI (Glycemic Risk Index) scores for a given year

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let year = 987 // Int | The year to compute GRI timeline for (optional)
let dataSources = ["inner_example"] // [String] | Optional data source filters (multiple allowed) (optional)

// Get monthly GRI (Glycemic Risk Index) scores for a given year
DataOverviewAPI.dataOverviewGetGriTimeline(year: year, dataSources: dataSources) { (response, error) in
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
 **year** | **Int** | The year to compute GRI timeline for | [optional] 
 **dataSources** | [**[String]**](String.md) | Optional data source filters (multiple allowed) | [optional] 

### Return type

[**GriTimelineResponse**](GriTimelineResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

