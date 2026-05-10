# RetrospectiveAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**retrospectiveGetBasalTimeline**](RetrospectiveAPI.md#retrospectivegetbasaltimeline) | **GET** /api/v4/Retrospective/basal-timeline | Get basal rate timeline for a day Returns basal rate data points showing scheduled and temp basal changes
[**retrospectiveGetRetrospectiveData**](RetrospectiveAPI.md#retrospectivegetretrospectivedata) | **GET** /api/v4/Retrospective/at | Get retrospective data at a specific point in time Returns IOB, COB, glucose, basal rate, and recent treatments
[**retrospectiveGetRetrospectiveTimeline**](RetrospectiveAPI.md#retrospectivegetretrospectivetimeline) | **GET** /api/v4/Retrospective/timeline | Get retrospective data for an entire day at specified interval Returns IOB, COB, glucose, and basal data for every interval throughout the day


# **retrospectiveGetBasalTimeline**
```swift
    open class func retrospectiveGetBasalTimeline(date: String? = nil, intervalMinutes: Int? = nil, completion: @escaping (_ data: BasalTimelineResponse?, _ error: Error?) -> Void)
```

Get basal rate timeline for a day Returns basal rate data points showing scheduled and temp basal changes

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let date = "date_example" // String | Date in YYYY-MM-DD format (optional)
let intervalMinutes = 987 // Int | Interval in minutes between data points (default: 5) (optional) (default to 5)

// Get basal rate timeline for a day Returns basal rate data points showing scheduled and temp basal changes
RetrospectiveAPI.retrospectiveGetBasalTimeline(date: date, intervalMinutes: intervalMinutes) { (response, error) in
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
 **date** | **String** | Date in YYYY-MM-DD format | [optional] 
 **intervalMinutes** | **Int** | Interval in minutes between data points (default: 5) | [optional] [default to 5]

### Return type

[**BasalTimelineResponse**](BasalTimelineResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrospectiveGetRetrospectiveData**
```swift
    open class func retrospectiveGetRetrospectiveData(time: Int64? = nil, completion: @escaping (_ data: RetrospectiveDataResponse?, _ error: Error?) -> Void)
```

Get retrospective data at a specific point in time Returns IOB, COB, glucose, basal rate, and recent treatments

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let time = 987 // Int64 | Unix timestamp in milliseconds for the retrospective point (optional)

// Get retrospective data at a specific point in time Returns IOB, COB, glucose, basal rate, and recent treatments
RetrospectiveAPI.retrospectiveGetRetrospectiveData(time: time) { (response, error) in
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
 **time** | **Int64** | Unix timestamp in milliseconds for the retrospective point | [optional] 

### Return type

[**RetrospectiveDataResponse**](RetrospectiveDataResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrospectiveGetRetrospectiveTimeline**
```swift
    open class func retrospectiveGetRetrospectiveTimeline(date: String? = nil, intervalMinutes: Int? = nil, completion: @escaping (_ data: RetrospectiveTimelineResponse?, _ error: Error?) -> Void)
```

Get retrospective data for an entire day at specified interval Returns IOB, COB, glucose, and basal data for every interval throughout the day

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let date = "date_example" // String | Date in YYYY-MM-DD format (optional)
let intervalMinutes = 987 // Int | Interval in minutes between data points (default: 5) (optional) (default to 5)

// Get retrospective data for an entire day at specified interval Returns IOB, COB, glucose, and basal data for every interval throughout the day
RetrospectiveAPI.retrospectiveGetRetrospectiveTimeline(date: date, intervalMinutes: intervalMinutes) { (response, error) in
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
 **date** | **String** | Date in YYYY-MM-DD format | [optional] 
 **intervalMinutes** | **Int** | Interval in minutes between data points (default: 5) | [optional] [default to 5]

### Return type

[**RetrospectiveTimelineResponse**](RetrospectiveTimelineResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

