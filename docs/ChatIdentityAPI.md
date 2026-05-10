# ChatIdentityAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatIdentityClaimLink**](ChatIdentityAPI.md#chatidentityclaimlink) | **POST** /api/v4/chat-identity/links/claim | Claim a pending link token after /connect slash command auth.
[**chatIdentityCreateDirectLink**](ChatIdentityAPI.md#chatidentitycreatedirectlink) | **POST** /api/v4/chat-identity/links/direct | Directly create a link for the current tenant (used by OAuth2 finalize hop).
[**chatIdentityGetLinks**](ChatIdentityAPI.md#chatidentitygetlinks) | **GET** /api/v4/chat-identity | List active chat identity links for the current tenant.
[**chatIdentityGetPending**](ChatIdentityAPI.md#chatidentitygetpending) | **GET** /api/v4/chat-identity/links/pending/{token} | Read-only lookup of a pending link token, used by the authorize page to validate and render the confirmation step.
[**chatIdentityRevokeLink**](ChatIdentityAPI.md#chatidentityrevokelink) | **DELETE** /api/v4/chat-identity/links/{id} | 
[**chatIdentitySetDefault**](ChatIdentityAPI.md#chatidentitysetdefault) | **POST** /api/v4/chat-identity/links/{id}/set-default | 
[**chatIdentityUpdateLink**](ChatIdentityAPI.md#chatidentityupdatelink) | **PATCH** /api/v4/chat-identity/links/{id} | 


# **chatIdentityClaimLink**
```swift
    open class func chatIdentityClaimLink(claimChatIdentityLinkRequest: ClaimChatIdentityLinkRequest, completion: @escaping (_ data: ChatIdentityLinkResponse?, _ error: Error?) -> Void)
```

Claim a pending link token after /connect slash command auth.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let claimChatIdentityLinkRequest = ClaimChatIdentityLinkRequest(token: "token_example") // ClaimChatIdentityLinkRequest | 

// Claim a pending link token after /connect slash command auth.
ChatIdentityAPI.chatIdentityClaimLink(claimChatIdentityLinkRequest: claimChatIdentityLinkRequest) { (response, error) in
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
 **claimChatIdentityLinkRequest** | [**ClaimChatIdentityLinkRequest**](ClaimChatIdentityLinkRequest.md) |  | 

### Return type

[**ChatIdentityLinkResponse**](ChatIdentityLinkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatIdentityCreateDirectLink**
```swift
    open class func chatIdentityCreateDirectLink(createDirectLinkRequest: CreateDirectLinkRequest, completion: @escaping (_ data: ChatIdentityLinkResponse?, _ error: Error?) -> Void)
```

Directly create a link for the current tenant (used by OAuth2 finalize hop).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createDirectLinkRequest = CreateDirectLinkRequest(platform: "platform_example", platformUserId: "platformUserId_example") // CreateDirectLinkRequest | 

// Directly create a link for the current tenant (used by OAuth2 finalize hop).
ChatIdentityAPI.chatIdentityCreateDirectLink(createDirectLinkRequest: createDirectLinkRequest) { (response, error) in
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
 **createDirectLinkRequest** | [**CreateDirectLinkRequest**](CreateDirectLinkRequest.md) |  | 

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
ChatIdentityAPI.chatIdentityGetLinks() { (response, error) in
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

# **chatIdentityGetPending**
```swift
    open class func chatIdentityGetPending(token: String, completion: @escaping (_ data: PendingLinkViewResponse?, _ error: Error?) -> Void)
```

Read-only lookup of a pending link token, used by the authorize page to validate and render the confirmation step.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let token = "token_example" // String | 

// Read-only lookup of a pending link token, used by the authorize page to validate and render the confirmation step.
ChatIdentityAPI.chatIdentityGetPending(token: token) { (response, error) in
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
 **token** | **String** |  | 

### Return type

[**PendingLinkViewResponse**](PendingLinkViewResponse.md)

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

ChatIdentityAPI.chatIdentityRevokeLink(id: id) { (response, error) in
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

# **chatIdentitySetDefault**
```swift
    open class func chatIdentitySetDefault(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

ChatIdentityAPI.chatIdentitySetDefault(id: id) { (response, error) in
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

# **chatIdentityUpdateLink**
```swift
    open class func chatIdentityUpdateLink(id: String, updateChatIdentityLinkRequest: UpdateChatIdentityLinkRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateChatIdentityLinkRequest = UpdateChatIdentityLinkRequest(label: "label_example", displayName: "displayName_example") // UpdateChatIdentityLinkRequest | 

ChatIdentityAPI.chatIdentityUpdateLink(id: id, updateChatIdentityLinkRequest: updateChatIdentityLinkRequest) { (response, error) in
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
 **updateChatIdentityLinkRequest** | [**UpdateChatIdentityLinkRequest**](UpdateChatIdentityLinkRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

