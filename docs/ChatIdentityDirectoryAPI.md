# ChatIdentityDirectoryAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatIdentityDirectoryCreatePending**](ChatIdentityDirectoryAPI.md#chatidentitydirectorycreatepending) | **POST** /api/v4/chat-identity/directory/pending-links | 
[**chatIdentityDirectoryResolve**](ChatIdentityDirectoryAPI.md#chatidentitydirectoryresolve) | **GET** /api/v4/chat-identity/directory/resolve | Returns ALL directory candidates for a (platform, platformUserId). Caller is responsible for label disambiguation. Each candidate includes the tenantSlug (joined from tenants table).
[**chatIdentityDirectoryRevokeByPlatformUser**](ChatIdentityDirectoryAPI.md#chatidentitydirectoryrevokebyplatformuser) | **DELETE** /api/v4/chat-identity/directory/links/{id} | Revoke a link by id, verifying the (platform, platformUserId) on the row matches the body. Used by /disconnect from the bot.


# **chatIdentityDirectoryCreatePending**
```swift
    open class func chatIdentityDirectoryCreatePending(createPendingLinkRequest: CreatePendingLinkRequest, completion: @escaping (_ data: PendingLinkResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createPendingLinkRequest = CreatePendingLinkRequest(platform: "platform_example", platformUserId: "platformUserId_example", tenantSlug: "tenantSlug_example", source: "source_example") // CreatePendingLinkRequest | 

ChatIdentityDirectoryAPI.chatIdentityDirectoryCreatePending(createPendingLinkRequest: createPendingLinkRequest) { (response, error) in
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
 **createPendingLinkRequest** | [**CreatePendingLinkRequest**](CreatePendingLinkRequest.md) |  | 

### Return type

[**PendingLinkResponse**](PendingLinkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatIdentityDirectoryResolve**
```swift
    open class func chatIdentityDirectoryResolve(platform: String? = nil, platformUserId: String? = nil, completion: @escaping (_ data: DirectoryCandidatesResponse?, _ error: Error?) -> Void)
```

Returns ALL directory candidates for a (platform, platformUserId). Caller is responsible for label disambiguation. Each candidate includes the tenantSlug (joined from tenants table).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let platform = "platform_example" // String | Chat platform identifier (e.g., \"discord\", \"telegram\"). (optional)
let platformUserId = "platformUserId_example" // String | Unique user identifier on the specified platform. (optional)

// Returns ALL directory candidates for a (platform, platformUserId). Caller is responsible for label disambiguation. Each candidate includes the tenantSlug (joined from tenants table).
ChatIdentityDirectoryAPI.chatIdentityDirectoryResolve(platform: platform, platformUserId: platformUserId) { (response, error) in
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
 **platform** | **String** | Chat platform identifier (e.g., \&quot;discord\&quot;, \&quot;telegram\&quot;). | [optional] 
 **platformUserId** | **String** | Unique user identifier on the specified platform. | [optional] 

### Return type

[**DirectoryCandidatesResponse**](DirectoryCandidatesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatIdentityDirectoryRevokeByPlatformUser**
```swift
    open class func chatIdentityDirectoryRevokeByPlatformUser(id: String, revokeByPlatformUserRequest: RevokeByPlatformUserRequest, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Revoke a link by id, verifying the (platform, platformUserId) on the row matches the body. Used by /disconnect from the bot.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let revokeByPlatformUserRequest = RevokeByPlatformUserRequest(platform: "platform_example", platformUserId: "platformUserId_example") // RevokeByPlatformUserRequest | 

// Revoke a link by id, verifying the (platform, platformUserId) on the row matches the body. Used by /disconnect from the bot.
ChatIdentityDirectoryAPI.chatIdentityDirectoryRevokeByPlatformUser(id: id, revokeByPlatformUserRequest: revokeByPlatformUserRequest) { (response, error) in
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
 **revokeByPlatformUserRequest** | [**RevokeByPlatformUserRequest**](RevokeByPlatformUserRequest.md) |  | 

### Return type

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

