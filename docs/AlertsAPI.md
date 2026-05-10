# AlertsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**alertsAcknowledge**](AlertsAPI.md#alertsacknowledge) | **POST** /api/v4/alerts/acknowledge | 
[**alertsGetActiveAlerts**](AlertsAPI.md#alertsgetactivealerts) | **GET** /api/v4/alerts/active | List active (unresolved) excursions for the current tenant.
[**alertsGetAlertHistory**](AlertsAPI.md#alertsgetalerthistory) | **GET** /api/v4/alerts/history | Get paginated history of resolved excursions.
[**alertsGetPendingDeliveries**](AlertsAPI.md#alertsgetpendingdeliveries) | **GET** /api/v4/alerts/deliveries/pending | Get pending deliveries for the specified channel types. Used by bot/adapter services to poll for work.
[**alertsMarkDelivered**](AlertsAPI.md#alertsmarkdelivered) | **POST** /api/v4/alerts/deliveries/{deliveryId}/delivered | 
[**alertsMarkFailed**](AlertsAPI.md#alertsmarkfailed) | **POST** /api/v4/alerts/deliveries/{deliveryId}/failed | 
[**alertsSnoozeInstance**](AlertsAPI.md#alertssnoozeinstance) | **POST** /api/v4/alerts/instances/{instanceId}/snooze | Snooze an alert instance for the specified duration.


# **alertsAcknowledge**
```swift
    open class func alertsAcknowledge(acknowledgeRequest: AcknowledgeRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let acknowledgeRequest = AcknowledgeRequest(acknowledgedBy: "acknowledgedBy_example") // AcknowledgeRequest | 

AlertsAPI.alertsAcknowledge(acknowledgeRequest: acknowledgeRequest) { (response, error) in
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
 **acknowledgeRequest** | [**AcknowledgeRequest**](AcknowledgeRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertsGetActiveAlerts**
```swift
    open class func alertsGetActiveAlerts(completion: @escaping (_ data: [ActiveExcursionResponse]?, _ error: Error?) -> Void)
```

List active (unresolved) excursions for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List active (unresolved) excursions for the current tenant.
AlertsAPI.alertsGetActiveAlerts() { (response, error) in
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

[**[ActiveExcursionResponse]**](ActiveExcursionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertsGetAlertHistory**
```swift
    open class func alertsGetAlertHistory(page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: AlertHistoryResponse?, _ error: Error?) -> Void)
```

Get paginated history of resolved excursions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 20)

// Get paginated history of resolved excursions.
AlertsAPI.alertsGetAlertHistory(page: page, pageSize: pageSize) { (response, error) in
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
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 20]

### Return type

[**AlertHistoryResponse**](AlertHistoryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertsGetPendingDeliveries**
```swift
    open class func alertsGetPendingDeliveries(channelType: [ChannelType]? = nil, completion: @escaping (_ data: [PendingDeliveryResponse]?, _ error: Error?) -> Void)
```

Get pending deliveries for the specified channel types. Used by bot/adapter services to poll for work.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let channelType = [ChannelType()] // [ChannelType] |  (optional)

// Get pending deliveries for the specified channel types. Used by bot/adapter services to poll for work.
AlertsAPI.alertsGetPendingDeliveries(channelType: channelType) { (response, error) in
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
 **channelType** | [**[ChannelType]**](ChannelType.md) |  | [optional] 

### Return type

[**[PendingDeliveryResponse]**](PendingDeliveryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertsMarkDelivered**
```swift
    open class func alertsMarkDelivered(deliveryId: String, markDeliveredRequest: MarkDeliveredRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let deliveryId = "deliveryId_example" // String | 
let markDeliveredRequest = MarkDeliveredRequest(platformMessageId: "platformMessageId_example", platformThreadId: "platformThreadId_example") // MarkDeliveredRequest | 

AlertsAPI.alertsMarkDelivered(deliveryId: deliveryId, markDeliveredRequest: markDeliveredRequest) { (response, error) in
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
 **deliveryId** | **String** |  | 
 **markDeliveredRequest** | [**MarkDeliveredRequest**](MarkDeliveredRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertsMarkFailed**
```swift
    open class func alertsMarkFailed(deliveryId: String, markFailedRequest: MarkFailedRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let deliveryId = "deliveryId_example" // String | 
let markFailedRequest = MarkFailedRequest(error: "error_example") // MarkFailedRequest | 

AlertsAPI.alertsMarkFailed(deliveryId: deliveryId, markFailedRequest: markFailedRequest) { (response, error) in
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
 **deliveryId** | **String** |  | 
 **markFailedRequest** | [**MarkFailedRequest**](MarkFailedRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertsSnoozeInstance**
```swift
    open class func alertsSnoozeInstance(instanceId: String, snoozeRequest: SnoozeRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Snooze an alert instance for the specified duration.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let instanceId = "instanceId_example" // String | 
let snoozeRequest = SnoozeRequest(minutes: 123) // SnoozeRequest | 

// Snooze an alert instance for the specified duration.
AlertsAPI.alertsSnoozeInstance(instanceId: instanceId, snoozeRequest: snoozeRequest) { (response, error) in
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
 **instanceId** | **String** |  | 
 **snoozeRequest** | [**SnoozeRequest**](SnoozeRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

