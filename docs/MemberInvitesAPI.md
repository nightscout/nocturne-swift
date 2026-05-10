# MemberInvitesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**memberInviteAcceptInvite**](MemberInvitesAPI.md#memberinviteacceptinvite) | **POST** /api/v4/member-invites/{token}/accept | Accept an invite and join the tenant.
[**memberInviteGetEffectivePermissions**](MemberInvitesAPI.md#memberinvitegeteffectivepermissions) | **GET** /api/v4/member-invites/members/{id}/effective-permissions | Get effective permissions for a member (union of role permissions + direct permissions).
[**memberInviteGetFollowers**](MemberInvitesAPI.md#memberinvitegetfollowers) | **GET** /api/v4/member-invites/members/followers | List followers of the current tenant (members with the follower role).
[**memberInviteGetInviteInfo**](MemberInvitesAPI.md#memberinvitegetinviteinfo) | **GET** /api/v4/member-invites/{token}/info | Get invite info for the accept page (anonymous).
[**memberInviteGetMembers**](MemberInvitesAPI.md#memberinvitegetmembers) | **GET** /api/v4/member-invites/members | List all members of the current tenant.
[**memberInviteSetMemberPermissions**](MemberInvitesAPI.md#memberinvitesetmemberpermissions) | **PUT** /api/v4/member-invites/members/{id}/permissions | Set direct permissions for a member.
[**memberInviteSetMemberRoles**](MemberInvitesAPI.md#memberinvitesetmemberroles) | **PUT** /api/v4/member-invites/members/{id}/roles | Set roles for a member (replaces all role assignments).


# **memberInviteAcceptInvite**
```swift
    open class func memberInviteAcceptInvite(token: String, completion: @escaping (_ data: AcceptMemberInviteResult?, _ error: Error?) -> Void)
```

Accept an invite and join the tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let token = "token_example" // String | 

// Accept an invite and join the tenant.
MemberInvitesAPI.memberInviteAcceptInvite(token: token) { (response, error) in
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

[**AcceptMemberInviteResult**](AcceptMemberInviteResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **memberInviteGetEffectivePermissions**
```swift
    open class func memberInviteGetEffectivePermissions(id: String, completion: @escaping (_ data: [String]?, _ error: Error?) -> Void)
```

Get effective permissions for a member (union of role permissions + direct permissions).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get effective permissions for a member (union of role permissions + direct permissions).
MemberInvitesAPI.memberInviteGetEffectivePermissions(id: id) { (response, error) in
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

**[String]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **memberInviteGetFollowers**
```swift
    open class func memberInviteGetFollowers(completion: @escaping (_ data: [TenantMemberDto]?, _ error: Error?) -> Void)
```

List followers of the current tenant (members with the follower role).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List followers of the current tenant (members with the follower role).
MemberInvitesAPI.memberInviteGetFollowers() { (response, error) in
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

[**[TenantMemberDto]**](TenantMemberDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **memberInviteGetInviteInfo**
```swift
    open class func memberInviteGetInviteInfo(token: String, completion: @escaping (_ data: MemberInviteInfo?, _ error: Error?) -> Void)
```

Get invite info for the accept page (anonymous).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let token = "token_example" // String | 

// Get invite info for the accept page (anonymous).
MemberInvitesAPI.memberInviteGetInviteInfo(token: token) { (response, error) in
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

[**MemberInviteInfo**](MemberInviteInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **memberInviteGetMembers**
```swift
    open class func memberInviteGetMembers(completion: @escaping (_ data: [TenantMemberDto]?, _ error: Error?) -> Void)
```

List all members of the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List all members of the current tenant.
MemberInvitesAPI.memberInviteGetMembers() { (response, error) in
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

[**[TenantMemberDto]**](TenantMemberDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **memberInviteSetMemberPermissions**
```swift
    open class func memberInviteSetMemberPermissions(id: String, setMemberPermissionsRequest: SetMemberPermissionsRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Set direct permissions for a member.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let setMemberPermissionsRequest = SetMemberPermissionsRequest(directPermissions: ["directPermissions_example"]) // SetMemberPermissionsRequest | 

// Set direct permissions for a member.
MemberInvitesAPI.memberInviteSetMemberPermissions(id: id, setMemberPermissionsRequest: setMemberPermissionsRequest) { (response, error) in
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
 **setMemberPermissionsRequest** | [**SetMemberPermissionsRequest**](SetMemberPermissionsRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **memberInviteSetMemberRoles**
```swift
    open class func memberInviteSetMemberRoles(id: String, setMemberRolesRequest: SetMemberRolesRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Set roles for a member (replaces all role assignments).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let setMemberRolesRequest = SetMemberRolesRequest(roleIds: ["roleIds_example"]) // SetMemberRolesRequest | 

// Set roles for a member (replaces all role assignments).
MemberInvitesAPI.memberInviteSetMemberRoles(id: id, setMemberRolesRequest: setMemberRolesRequest) { (response, error) in
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
 **setMemberRolesRequest** | [**SetMemberRolesRequest**](SetMemberRolesRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

