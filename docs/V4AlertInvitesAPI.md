# V4AlertInvitesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**alertInvitesCreateInvite**](V4AlertInvitesAPI.md#alertinvitescreateinvite) | **POST** /api/v4/alert-invites | Generate an invite link for a follower to join an escalation step.
[**alertInvitesRedeemInvite**](V4AlertInvitesAPI.md#alertinvitesredeeminvite) | **POST** /api/v4/alert-invites/{token}/redeem | Redeem an invite token.
[**alertInvitesRevokeInvite**](V4AlertInvitesAPI.md#alertinvitesrevokeinvite) | **DELETE** /api/v4/alert-invites/{id} | Revoke an unredeemed invite.
[**alertInvitesValidateInvite**](V4AlertInvitesAPI.md#alertinvitesvalidateinvite) | **GET** /api/v4/alert-invites/{token} | Validate an invite token (public endpoint for redemption flow).


# **alertInvitesCreateInvite**
```swift
    open class func alertInvitesCreateInvite(createAlertInviteRequest: CreateAlertInviteRequest, completion: @escaping (_ data: AlertInviteResponse?, _ error: Error?) -> Void)
```

Generate an invite link for a follower to join an escalation step.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createAlertInviteRequest = CreateAlertInviteRequest(escalationStepId: "escalationStepId_example", permissionScope: "permissionScope_example") // CreateAlertInviteRequest | 

// Generate an invite link for a follower to join an escalation step.
V4AlertInvitesAPI.alertInvitesCreateInvite(createAlertInviteRequest: createAlertInviteRequest) { (response, error) in
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
 **createAlertInviteRequest** | [**CreateAlertInviteRequest**](CreateAlertInviteRequest.md) |  | 

### Return type

[**AlertInviteResponse**](AlertInviteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertInvitesRedeemInvite**
```swift
    open class func alertInvitesRedeemInvite(token: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Redeem an invite token.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let token = "token_example" // String | 

// Redeem an invite token.
V4AlertInvitesAPI.alertInvitesRedeemInvite(token: token) { (response, error) in
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

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertInvitesRevokeInvite**
```swift
    open class func alertInvitesRevokeInvite(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Revoke an unredeemed invite.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Revoke an unredeemed invite.
V4AlertInvitesAPI.alertInvitesRevokeInvite(id: id) { (response, error) in
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
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertInvitesValidateInvite**
```swift
    open class func alertInvitesValidateInvite(token: String, completion: @escaping (_ data: AlertInviteResponse?, _ error: Error?) -> Void)
```

Validate an invite token (public endpoint for redemption flow).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let token = "token_example" // String | 

// Validate an invite token (public endpoint for redemption flow).
V4AlertInvitesAPI.alertInvitesValidateInvite(token: token) { (response, error) in
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

[**AlertInviteResponse**](AlertInviteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

