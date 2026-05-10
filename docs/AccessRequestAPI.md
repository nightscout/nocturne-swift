# AccessRequestAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accessRequestApprove**](AccessRequestAPI.md#accessrequestapprove) | **POST** /api/v4/admin/access-requests/{subjectId}/approve | 
[**accessRequestDeny**](AccessRequestAPI.md#accessrequestdeny) | **POST** /api/v4/admin/access-requests/{subjectId}/deny | 
[**accessRequestGetPendingRequests**](AccessRequestAPI.md#accessrequestgetpendingrequests) | **GET** /api/v4/admin/access-requests | 


# **accessRequestApprove**
```swift
    open class func accessRequestApprove(subjectId: String, approveAccessRequestRequest: ApproveAccessRequestRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let subjectId = "subjectId_example" // String | 
let approveAccessRequestRequest = ApproveAccessRequestRequest(roleIds: ["roleIds_example"], directPermissions: ["directPermissions_example"]) // ApproveAccessRequestRequest | 

AccessRequestAPI.accessRequestApprove(subjectId: subjectId, approveAccessRequestRequest: approveAccessRequestRequest) { (response, error) in
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
 **subjectId** | **String** |  | 
 **approveAccessRequestRequest** | [**ApproveAccessRequestRequest**](ApproveAccessRequestRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accessRequestDeny**
```swift
    open class func accessRequestDeny(subjectId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let subjectId = "subjectId_example" // String | 

AccessRequestAPI.accessRequestDeny(subjectId: subjectId) { (response, error) in
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
 **subjectId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accessRequestGetPendingRequests**
```swift
    open class func accessRequestGetPendingRequests(completion: @escaping (_ data: [AccessRequestDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


AccessRequestAPI.accessRequestGetPendingRequests() { (response, error) in
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

[**[AccessRequestDto]**](AccessRequestDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

