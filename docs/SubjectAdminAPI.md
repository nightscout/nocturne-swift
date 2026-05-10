# SubjectAdminAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**subjectAdminSetPlatformAdmin**](SubjectAdminAPI.md#subjectadminsetplatformadmin) | **PUT** /api/v4/admin/subjects/{id}/platform-admin | Grant or revoke platform admin for a subject. Blocks self-demotion if the caller is the last platform admin.


# **subjectAdminSetPlatformAdmin**
```swift
    open class func subjectAdminSetPlatformAdmin(id: String, setPlatformAdminRequest: SetPlatformAdminRequest, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Grant or revoke platform admin for a subject. Blocks self-demotion if the caller is the last platform admin.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let setPlatformAdminRequest = SetPlatformAdminRequest(isPlatformAdmin: false) // SetPlatformAdminRequest | 

// Grant or revoke platform admin for a subject. Blocks self-demotion if the caller is the last platform admin.
SubjectAdminAPI.subjectAdminSetPlatformAdmin(id: id, setPlatformAdminRequest: setPlatformAdminRequest) { (response, error) in
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
 **id** | **String** |  | 
 **setPlatformAdminRequest** | [**SetPlatformAdminRequest**](SetPlatformAdminRequest.md) |  | 

### Return type

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

