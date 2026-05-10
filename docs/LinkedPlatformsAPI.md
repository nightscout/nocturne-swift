# LinkedPlatformsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**linkedPlatformsGetLinkedPlatforms**](LinkedPlatformsAPI.md#linkedplatformsgetlinkedplatforms) | **GET** /api/v4/chat-identity/linked-platforms | 


# **linkedPlatformsGetLinkedPlatforms**
```swift
    open class func linkedPlatformsGetLinkedPlatforms(completion: @escaping (_ data: LinkedPlatformsResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


LinkedPlatformsAPI.linkedPlatformsGetLinkedPlatforms() { (response, error) in
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

[**LinkedPlatformsResponse**](LinkedPlatformsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

