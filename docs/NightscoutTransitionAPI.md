# NightscoutTransitionAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**nightscoutTransitionGetTransitionStatus**](NightscoutTransitionAPI.md#nightscouttransitiongettransitionstatus) | **GET** /api/v4/nightscout-transition/status | Get the current Nightscout transition status including migration progress, write-back health, and disconnect readiness recommendation.


# **nightscoutTransitionGetTransitionStatus**
```swift
    open class func nightscoutTransitionGetTransitionStatus(completion: @escaping (_ data: NightscoutTransitionStatus?, _ error: Error?) -> Void)
```

Get the current Nightscout transition status including migration progress, write-back health, and disconnect readiness recommendation.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get the current Nightscout transition status including migration progress, write-back health, and disconnect readiness recommendation.
NightscoutTransitionAPI.nightscoutTransitionGetTransitionStatus() { (response, error) in
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

[**NightscoutTransitionStatus**](NightscoutTransitionStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

