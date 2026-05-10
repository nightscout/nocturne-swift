# V4ChatIdentityAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatIdentityCreateLink**](V4ChatIdentityAPI.md#chatidentitycreatelink) | **POST** /api/v4/chat-identity | Create a new chat identity link.
[**chatIdentityGetLinks**](V4ChatIdentityAPI.md#chatidentitygetlinks) | **GET** /api/v4/chat-identity | List active chat identity links for the current tenant.
[**chatIdentityResolve**](V4ChatIdentityAPI.md#chatidentityresolve) | **GET** /api/v4/chat-identity/resolve | Resolve a platform identity to a Nocturne user. Used by the bot service to look up which tenant/user a chat message belongs to.
[**chatIdentityRevokeLink**](V4ChatIdentityAPI.md#chatidentityrevokelink) | **DELETE** /api/v4/chat-identity/{id} | Revoke (soft-delete) a chat identity link.


# **chatIdentityCreateLink**
```swift
    open class func chatIdentityCreateLink(createChatIdentityLinkRequest: CreateChatIdentityLinkRequest, completion: @escaping (_ data: ChatIdentityLinkResponse?, _ error: Error?) -> Void)
```

Create a new chat identity link.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createChatIdentityLinkRequest = CreateChatIdentityLinkRequest(nocturneUserId: "nocturneUserId_example", platform: "platform_example", platformUserId: "platformUserId_example", platformChannelId: "platformChannelId_example") // CreateChatIdentityLinkRequest | 

// Create a new chat identity link.
V4ChatIdentityAPI.chatIdentityCreateLink(createChatIdentityLinkRequest: createChatIdentityLinkRequest) { (response, error) in
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
 **createChatIdentityLinkRequest** | [**CreateChatIdentityLinkRequest**](CreateChatIdentityLinkRequest.md) |  | 

### Return type

[**ChatIdentityLinkResponse**](ChatIdentityLinkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatIdentityGetLinks**
```swift
    open class func chatIdentityGetLinks(completion: @escaping (_ data: [ChatIdentityLinkResponse]?, _ error: Error?) -> Void)
```

List active chat identity links for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List active chat identity links for the current tenant.
V4ChatIdentityAPI.chatIdentityGetLinks() { (response, error) in
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

[**[ChatIdentityLinkResponse]**](ChatIdentityLinkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatIdentityResolve**
```swift
    open class func chatIdentityResolve(platform: String? = nil, platformUserId: String? = nil, completion: @escaping (_ data: ChatIdentityLinkResponse?, _ error: Error?) -> Void)
```

Resolve a platform identity to a Nocturne user. Used by the bot service to look up which tenant/user a chat message belongs to.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let platform = "platform_example" // String |  (optional)
let platformUserId = "platformUserId_example" // String |  (optional)

// Resolve a platform identity to a Nocturne user. Used by the bot service to look up which tenant/user a chat message belongs to.
V4ChatIdentityAPI.chatIdentityResolve(platform: platform, platformUserId: platformUserId) { (response, error) in
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
 **platform** | **String** |  | [optional] 
 **platformUserId** | **String** |  | [optional] 

### Return type

[**ChatIdentityLinkResponse**](ChatIdentityLinkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatIdentityRevokeLink**
```swift
    open class func chatIdentityRevokeLink(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Revoke (soft-delete) a chat identity link.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Revoke (soft-delete) a chat identity link.
V4ChatIdentityAPI.chatIdentityRevokeLink(id: id) { (response, error) in
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

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

