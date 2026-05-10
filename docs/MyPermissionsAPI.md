# MyPermissionsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**myPermissionsGetMyPermissions**](MyPermissionsAPI.md#mypermissionsgetmypermissions) | **GET** /api/v4/me/permissions | Get the current user&#39;s effective granted scopes for the current tenant.


# **myPermissionsGetMyPermissions**
```swift
    open class func myPermissionsGetMyPermissions(completion: @escaping (_ data: [String]?, _ error: Error?) -> Void)
```

Get the current user's effective granted scopes for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get the current user's effective granted scopes for the current tenant.
MyPermissionsAPI.myPermissionsGetMyPermissions() { (response, error) in
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

