# TrackerAlertsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**trackerAlertsGetAvailableSounds**](TrackerAlertsAPI.md#trackeralertsgetavailablesounds) | **GET** /api/v4/trackers/alerts/sounds | Get available alert sounds
[**trackerAlertsGetPendingAlerts**](TrackerAlertsAPI.md#trackeralertsgetpendingalerts) | **GET** /api/v4/trackers/alerts/pending | 


# **trackerAlertsGetAvailableSounds**
```swift
    open class func trackerAlertsGetAvailableSounds(completion: @escaping (_ data: [String]?, _ error: Error?) -> Void)
```

Get available alert sounds

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get available alert sounds
TrackerAlertsAPI.trackerAlertsGetAvailableSounds() { (response, error) in
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

**[String]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackerAlertsGetPendingAlerts**
```swift
    open class func trackerAlertsGetPendingAlerts(completion: @escaping (_ data: [TrackerAlertDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


TrackerAlertsAPI.trackerAlertsGetPendingAlerts() { (response, error) in
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

[**[TrackerAlertDto]**](TrackerAlertDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

