# ConnectedAppsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectedAppsList**](ConnectedAppsAPI.md#connectedappslist) | **GET** /api/v4/account/connected-apps | List all connected apps (OAuth app grants) for the authenticated user on the current tenant.
[**connectedAppsRevoke**](ConnectedAppsAPI.md#connectedappsrevoke) | **DELETE** /api/v4/account/connected-apps/{grantId} | Revoke a connected app. Soft-deletes the grant and invalidates all associated refresh tokens; previously-issued access tokens become unusable on next request via the revocation cache.


# **connectedAppsList**
```swift
    open class func connectedAppsList(completion: @escaping (_ data: [ConnectedAppDto]?, _ error: Error?) -> Void)
```

List all connected apps (OAuth app grants) for the authenticated user on the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List all connected apps (OAuth app grants) for the authenticated user on the current tenant.
ConnectedAppsAPI.connectedAppsList() { (response, error) in
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

[**[ConnectedAppDto]**](ConnectedAppDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **connectedAppsRevoke**
```swift
    open class func connectedAppsRevoke(grantId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Revoke a connected app. Soft-deletes the grant and invalidates all associated refresh tokens; previously-issued access tokens become unusable on next request via the revocation cache.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let grantId = "grantId_example" // String | 

// Revoke a connected app. Soft-deletes the grant and invalidates all associated refresh tokens; previously-issued access tokens become unusable on next request via the revocation cache.
ConnectedAppsAPI.connectedAppsRevoke(grantId: grantId) { (response, error) in
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
 **grantId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

