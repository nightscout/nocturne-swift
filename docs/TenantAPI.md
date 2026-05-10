# TenantAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tenantAddMember**](TenantAPI.md#tenantaddmember) | **POST** /api/v4/admin/tenants/{id}/members | 
[**tenantAttachOidcIdentity**](TenantAPI.md#tenantattachoidcidentity) | **POST** /api/v4/admin/tenants/{id}/members/{subjectId}/credentials/oidc | Attaches an OIDC identity to a member subject.
[**tenantCreate**](TenantAPI.md#tenantcreate) | **POST** /api/v4/admin/tenants | 
[**tenantCreateInvite**](TenantAPI.md#tenantcreateinvite) | **POST** /api/v4/admin/tenants/{id}/invites | 
[**tenantDelete**](TenantAPI.md#tenantdelete) | **DELETE** /api/v4/admin/tenants/{id} | 
[**tenantGetAll**](TenantAPI.md#tenantgetall) | **GET** /api/v4/admin/tenants | 
[**tenantGetById**](TenantAPI.md#tenantgetbyid) | **GET** /api/v4/admin/tenants/{id} | 
[**tenantGetMemberCredentials**](TenantAPI.md#tenantgetmembercredentials) | **GET** /api/v4/admin/tenants/{id}/members/{subjectId}/credentials | Lists passkey credentials and OIDC identities for a member subject.
[**tenantListInvites**](TenantAPI.md#tenantlistinvites) | **GET** /api/v4/admin/tenants/{id}/invites | 
[**tenantProvision**](TenantAPI.md#tenantprovision) | **POST** /api/v4/admin/tenants/provision | 
[**tenantRemoveMember**](TenantAPI.md#tenantremovemember) | **DELETE** /api/v4/admin/tenants/{id}/members/{subjectId} | 
[**tenantRemoveOidcIdentity**](TenantAPI.md#tenantremoveoidcidentity) | **DELETE** /api/v4/admin/tenants/{id}/members/{subjectId}/credentials/oidc/{identityId} | Removes an OIDC identity from a member subject.
[**tenantRemovePasskeyCredential**](TenantAPI.md#tenantremovepasskeycredential) | **DELETE** /api/v4/admin/tenants/{id}/members/{subjectId}/credentials/passkey/{credentialId} | Removes a passkey credential from a member subject.
[**tenantRevokeInvite**](TenantAPI.md#tenantrevokeinvite) | **DELETE** /api/v4/admin/tenants/{id}/invites/{inviteId} | 
[**tenantUpdate**](TenantAPI.md#tenantupdate) | **PUT** /api/v4/admin/tenants/{id} | 


# **tenantAddMember**
```swift
    open class func tenantAddMember(id: String, addMemberRequest: AddMemberRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let addMemberRequest = AddMemberRequest(subjectId: "subjectId_example", roleIds: ["roleIds_example"], directPermissions: ["directPermissions_example"]) // AddMemberRequest | 

TenantAPI.tenantAddMember(id: id, addMemberRequest: addMemberRequest) { (response, error) in
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
 **addMemberRequest** | [**AddMemberRequest**](AddMemberRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantAttachOidcIdentity**
```swift
    open class func tenantAttachOidcIdentity(id: String, subjectId: String, adminAttachOidcRequest: AdminAttachOidcRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Attaches an OIDC identity to a member subject.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let subjectId = "subjectId_example" // String | 
let adminAttachOidcRequest = AdminAttachOidcRequest(providerId: "providerId_example", oidcSubjectId: "oidcSubjectId_example", issuer: "issuer_example", email: "email_example") // AdminAttachOidcRequest | 

// Attaches an OIDC identity to a member subject.
TenantAPI.tenantAttachOidcIdentity(id: id, subjectId: subjectId, adminAttachOidcRequest: adminAttachOidcRequest) { (response, error) in
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
 **subjectId** | **String** |  | 
 **adminAttachOidcRequest** | [**AdminAttachOidcRequest**](AdminAttachOidcRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantCreate**
```swift
    open class func tenantCreate(createTenantRequest: CreateTenantRequest, completion: @escaping (_ data: TenantCreatedDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createTenantRequest = CreateTenantRequest(slug: "slug_example", displayName: "displayName_example") // CreateTenantRequest | 

TenantAPI.tenantCreate(createTenantRequest: createTenantRequest) { (response, error) in
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
 **createTenantRequest** | [**CreateTenantRequest**](CreateTenantRequest.md) |  | 

### Return type

[**TenantCreatedDto**](TenantCreatedDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantCreateInvite**
```swift
    open class func tenantCreateInvite(id: String, createMemberInviteRequest: CreateMemberInviteRequest, completion: @escaping (_ data: MemberInviteResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let createMemberInviteRequest = CreateMemberInviteRequest(roleIds: ["roleIds_example"], directPermissions: ["directPermissions_example"], label: "label_example", expiresInDays: 123, maxUses: 123, limitTo24Hours: false) // CreateMemberInviteRequest | 

TenantAPI.tenantCreateInvite(id: id, createMemberInviteRequest: createMemberInviteRequest) { (response, error) in
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
 **createMemberInviteRequest** | [**CreateMemberInviteRequest**](CreateMemberInviteRequest.md) |  | 

### Return type

[**MemberInviteResult**](MemberInviteResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantDelete**
```swift
    open class func tenantDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

TenantAPI.tenantDelete(id: id) { (response, error) in
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

# **tenantGetAll**
```swift
    open class func tenantGetAll(completion: @escaping (_ data: [TenantDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


TenantAPI.tenantGetAll() { (response, error) in
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

[**[TenantDto]**](TenantDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantGetById**
```swift
    open class func tenantGetById(id: String, completion: @escaping (_ data: TenantDetailDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

TenantAPI.tenantGetById(id: id) { (response, error) in
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

[**TenantDetailDto**](TenantDetailDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantGetMemberCredentials**
```swift
    open class func tenantGetMemberCredentials(id: String, subjectId: String, completion: @escaping (_ data: SubjectCredentialsDto?, _ error: Error?) -> Void)
```

Lists passkey credentials and OIDC identities for a member subject.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let subjectId = "subjectId_example" // String | 

// Lists passkey credentials and OIDC identities for a member subject.
TenantAPI.tenantGetMemberCredentials(id: id, subjectId: subjectId) { (response, error) in
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
 **subjectId** | **String** |  | 

### Return type

[**SubjectCredentialsDto**](SubjectCredentialsDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantListInvites**
```swift
    open class func tenantListInvites(id: String, completion: @escaping (_ data: [MemberInviteInfo]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

TenantAPI.tenantListInvites(id: id) { (response, error) in
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

[**[MemberInviteInfo]**](MemberInviteInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantProvision**
```swift
    open class func tenantProvision(provisionRequest: ProvisionRequest, completion: @escaping (_ data: ProvisionResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let provisionRequest = ProvisionRequest(slug: "slug_example", displayName: "displayName_example", ownerUsername: "ownerUsername_example", ownerEmail: "ownerEmail_example", credential: ProvisionCredentialData(credentialId: "credentialId_example", publicKey: "publicKey_example", signCount: 123, transports: ["transports_example"], aaGuid: "aaGuid_example", subjectId: "subjectId_example"), oidcIdentity: ProvisionOidcIdentityData(provider: "provider_example", oidcSubjectId: "oidcSubjectId_example", issuer: "issuer_example", email: "email_example", subjectId: "subjectId_example")) // ProvisionRequest | 

TenantAPI.tenantProvision(provisionRequest: provisionRequest) { (response, error) in
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
 **provisionRequest** | [**ProvisionRequest**](ProvisionRequest.md) |  | 

### Return type

[**ProvisionResult**](ProvisionResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantRemoveMember**
```swift
    open class func tenantRemoveMember(id: String, subjectId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let subjectId = "subjectId_example" // String | 

TenantAPI.tenantRemoveMember(id: id, subjectId: subjectId) { (response, error) in
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
 **subjectId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantRemoveOidcIdentity**
```swift
    open class func tenantRemoveOidcIdentity(id: String, subjectId: String, identityId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Removes an OIDC identity from a member subject.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let subjectId = "subjectId_example" // String | 
let identityId = "identityId_example" // String | 

// Removes an OIDC identity from a member subject.
TenantAPI.tenantRemoveOidcIdentity(id: id, subjectId: subjectId, identityId: identityId) { (response, error) in
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
 **subjectId** | **String** |  | 
 **identityId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantRemovePasskeyCredential**
```swift
    open class func tenantRemovePasskeyCredential(id: String, subjectId: String, credentialId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Removes a passkey credential from a member subject.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let subjectId = "subjectId_example" // String | 
let credentialId = "credentialId_example" // String | 

// Removes a passkey credential from a member subject.
TenantAPI.tenantRemovePasskeyCredential(id: id, subjectId: subjectId, credentialId: credentialId) { (response, error) in
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
 **subjectId** | **String** |  | 
 **credentialId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantRevokeInvite**
```swift
    open class func tenantRevokeInvite(id: String, inviteId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let inviteId = "inviteId_example" // String | 

TenantAPI.tenantRevokeInvite(id: id, inviteId: inviteId) { (response, error) in
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
 **inviteId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tenantUpdate**
```swift
    open class func tenantUpdate(id: String, updateTenantRequest: UpdateTenantRequest, completion: @escaping (_ data: TenantDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateTenantRequest = UpdateTenantRequest(displayName: "displayName_example", isActive: false, allowAccessRequests: false) // UpdateTenantRequest | 

TenantAPI.tenantUpdate(id: id, updateTenantRequest: updateTenantRequest) { (response, error) in
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
 **updateTenantRequest** | [**UpdateTenantRequest**](UpdateTenantRequest.md) |  | 

### Return type

[**TenantDto**](TenantDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

