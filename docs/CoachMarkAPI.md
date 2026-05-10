# CoachMarkAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**coachMarkDeleteAll**](CoachMarkAPI.md#coachmarkdeleteall) | **DELETE** /api/v4/coach-marks | Delete all coach mark states for the current user, resetting all tutorials.
[**coachMarkGetAll**](CoachMarkAPI.md#coachmarkgetall) | **GET** /api/v4/coach-marks | Get all coach mark states for the current user.
[**coachMarkUpdateStatus**](CoachMarkAPI.md#coachmarkupdatestatus) | **PATCH** /api/v4/coach-marks/{key} | Update a coach mark&#39;s status.


# **coachMarkDeleteAll**
```swift
    open class func coachMarkDeleteAll(completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Delete all coach mark states for the current user, resetting all tutorials.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Delete all coach mark states for the current user, resetting all tutorials.
CoachMarkAPI.coachMarkDeleteAll() { (response, error) in
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

# **coachMarkGetAll**
```swift
    open class func coachMarkGetAll(completion: @escaping (_ data: [CoachMarkState]?, _ error: Error?) -> Void)
```

Get all coach mark states for the current user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all coach mark states for the current user.
CoachMarkAPI.coachMarkGetAll() { (response, error) in
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

[**[CoachMarkState]**](CoachMarkState.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **coachMarkUpdateStatus**
```swift
    open class func coachMarkUpdateStatus(key: String, updateCoachMarkRequest: UpdateCoachMarkRequest, completion: @escaping (_ data: CoachMarkState?, _ error: Error?) -> Void)
```

Update a coach mark's status.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let key = "key_example" // String | The coach mark key to update.
let updateCoachMarkRequest = UpdateCoachMarkRequest(status: "status_example") // UpdateCoachMarkRequest | The new status value.

// Update a coach mark's status.
CoachMarkAPI.coachMarkUpdateStatus(key: key, updateCoachMarkRequest: updateCoachMarkRequest) { (response, error) in
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
 **key** | **String** | The coach mark key to update. | 
 **updateCoachMarkRequest** | [**UpdateCoachMarkRequest**](UpdateCoachMarkRequest.md) | The new status value. | 

### Return type

[**CoachMarkState**](CoachMarkState.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

