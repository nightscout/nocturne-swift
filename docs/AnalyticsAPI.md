# AnalyticsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analyticsClearAnalyticsData**](AnalyticsAPI.md#analyticsclearanalyticsdata) | **DELETE** /api/v4/Analytics/data | Clears all locally stored analytics data. This action cannot be undone.
[**analyticsGetAnalyticsStatus**](AnalyticsAPI.md#analyticsgetanalyticsstatus) | **GET** /api/v4/Analytics/status | Gets the current analytics configuration and collection status.
[**analyticsGetPendingAnalyticsData**](AnalyticsAPI.md#analyticsgetpendinganalyticsdata) | **GET** /api/v4/Analytics/data/pending | Gets any pending analytics data queued for collection, returned for transparency. Since data is stored locally only, this is informational.
[**analyticsGetPerformanceMetrics**](AnalyticsAPI.md#analyticsgetperformancemetrics) | **GET** /api/v4/Analytics/metrics/performance | Gets current system performance metrics such as request latencies and memory usage.
[**analyticsGetPrivacyInformation**](AnalyticsAPI.md#analyticsgetprivacyinformation) | **GET** /api/v4/Analytics/privacy | Get information about what data is collected and privacy policy
[**analyticsGetUsageStatistics**](AnalyticsAPI.md#analyticsgetusagestatistics) | **GET** /api/v4/Analytics/metrics/usage | Gets current usage statistics such as endpoint hit counts and feature usage.
[**analyticsTrackCustomEvent**](AnalyticsAPI.md#analyticstrackcustomevent) | **POST** /api/v4/Analytics/events | Tracks a custom AnalyticsEvent. Useful for integration testing or manually recording discrete events. Returns 400 Bad Request if analytics collection is disabled.
[**analyticsUpdateAnalyticsConfig**](AnalyticsAPI.md#analyticsupdateanalyticsconfig) | **PUT** /api/v4/Analytics/config | Updates analytics collection configuration.


# **analyticsClearAnalyticsData**
```swift
    open class func analyticsClearAnalyticsData(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Clears all locally stored analytics data. This action cannot be undone.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Clears all locally stored analytics data. This action cannot be undone.
AnalyticsAPI.analyticsClearAnalyticsData() { (response, error) in
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

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **analyticsGetAnalyticsStatus**
```swift
    open class func analyticsGetAnalyticsStatus(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Gets the current analytics configuration and collection status.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets the current analytics configuration and collection status.
AnalyticsAPI.analyticsGetAnalyticsStatus() { (response, error) in
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

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **analyticsGetPendingAnalyticsData**
```swift
    open class func analyticsGetPendingAnalyticsData(completion: @escaping (_ data: AnalyticsBatch?, _ error: Error?) -> Void)
```

Gets any pending analytics data queued for collection, returned for transparency. Since data is stored locally only, this is informational.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets any pending analytics data queued for collection, returned for transparency. Since data is stored locally only, this is informational.
AnalyticsAPI.analyticsGetPendingAnalyticsData() { (response, error) in
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

[**AnalyticsBatch**](AnalyticsBatch.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **analyticsGetPerformanceMetrics**
```swift
    open class func analyticsGetPerformanceMetrics(completion: @escaping (_ data: PerformanceMetrics?, _ error: Error?) -> Void)
```

Gets current system performance metrics such as request latencies and memory usage.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets current system performance metrics such as request latencies and memory usage.
AnalyticsAPI.analyticsGetPerformanceMetrics() { (response, error) in
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

[**PerformanceMetrics**](PerformanceMetrics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **analyticsGetPrivacyInformation**
```swift
    open class func analyticsGetPrivacyInformation(completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Get information about what data is collected and privacy policy

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get information about what data is collected and privacy policy
AnalyticsAPI.analyticsGetPrivacyInformation() { (response, error) in
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

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **analyticsGetUsageStatistics**
```swift
    open class func analyticsGetUsageStatistics(completion: @escaping (_ data: UsageStatistics?, _ error: Error?) -> Void)
```

Gets current usage statistics such as endpoint hit counts and feature usage.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets current usage statistics such as endpoint hit counts and feature usage.
AnalyticsAPI.analyticsGetUsageStatistics() { (response, error) in
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

[**UsageStatistics**](UsageStatistics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **analyticsTrackCustomEvent**
```swift
    open class func analyticsTrackCustomEvent(analyticsEvent: AnalyticsEvent, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Tracks a custom AnalyticsEvent. Useful for integration testing or manually recording discrete events. Returns 400 Bad Request if analytics collection is disabled.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let analyticsEvent = AnalyticsEvent(sessionId: "sessionId_example", eventType: "eventType_example", category: "category_example", action: "action_example", label: "label_example", value: 123, timestamp: 123, metadata: "TODO") // AnalyticsEvent | The custom AnalyticsEvent to record.

// Tracks a custom AnalyticsEvent. Useful for integration testing or manually recording discrete events. Returns 400 Bad Request if analytics collection is disabled.
AnalyticsAPI.analyticsTrackCustomEvent(analyticsEvent: analyticsEvent) { (response, error) in
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
 **analyticsEvent** | [**AnalyticsEvent**](AnalyticsEvent.md) | The custom AnalyticsEvent to record. | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **analyticsUpdateAnalyticsConfig**
```swift
    open class func analyticsUpdateAnalyticsConfig(analyticsCollectionConfig: AnalyticsCollectionConfig, completion: @escaping (_ data: AnalyticsCollectionConfig?, _ error: Error?) -> Void)
```

Updates analytics collection configuration.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let analyticsCollectionConfig = AnalyticsCollectionConfig(collectApiUsage: false, collectUiUsage: false, collectPerformanceMetrics: false, collectHealthMetrics: false, collectFeatureUsage: false, excludedEndpoints: ["excludedEndpoints_example"], maxLocalEvents: 123) // AnalyticsCollectionConfig | The new AnalyticsCollectionConfig to persist.

// Updates analytics collection configuration.
AnalyticsAPI.analyticsUpdateAnalyticsConfig(analyticsCollectionConfig: analyticsCollectionConfig) { (response, error) in
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
 **analyticsCollectionConfig** | [**AnalyticsCollectionConfig**](AnalyticsCollectionConfig.md) | The new AnalyticsCollectionConfig to persist. | 

### Return type

[**AnalyticsCollectionConfig**](AnalyticsCollectionConfig.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

