# DevAdminAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**devAdminCreateTenant**](DevAdminAPI.md#devadmincreatetenant) | **POST** /api/v4/dev-only/admin/tenants | Create a new tenant without authentication (dev-only). Used by the Aspire dashboard \&quot;Create Tenant\&quot; command.
[**devAdminDeleteTenant**](DevAdminAPI.md#devadmindeletetenant) | **DELETE** /api/v4/dev-only/admin/tenants/{id} | Delete a tenant and all associated data without authentication (dev-only).
[**devAdminExportSnapshot**](DevAdminAPI.md#devadminexportsnapshot) | **GET** /api/v4/dev-only/admin/snapshot | Export a full snapshot of all tenants and their identity/config data. Secrets are decrypted to plaintext for portability.
[**devAdminImportScopedSnapshot**](DevAdminAPI.md#devadminimportscopedsnapshot) | **POST** /api/v4/dev-only/admin/tenants/{id}/import-snapshot | Import snapshot data for a single tenant, matched by slug in the provided snapshot. Upserts referenced subjects and passkeys without affecting other tenants.
[**devAdminImportSnapshot**](DevAdminAPI.md#devadminimportsnapshot) | **POST** /api/v4/dev-only/admin/snapshot | Import a snapshot, replacing all identity/config data. Wraps the entire operation in a transaction.
[**devAdminListTenants**](DevAdminAPI.md#devadminlisttenants) | **GET** /api/v4/dev-only/admin/tenants | List all tenants with record counts and connector health (dev-only). Used by the Aspire dashboard \&quot;List Tenants\&quot; command.
[**devAdminSyncAll**](DevAdminAPI.md#devadminsyncall) | **POST** /api/v4/dev-only/admin/sync-all | Trigger a sync for every configured connector across all tenants.


# **devAdminCreateTenant**
```swift
    open class func devAdminCreateTenant(devCreateTenantRequest: DevCreateTenantRequest, completion: @escaping (_ data: TenantCreatedDto?, _ error: Error?) -> Void)
```

Create a new tenant without authentication (dev-only). Used by the Aspire dashboard \"Create Tenant\" command.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let devCreateTenantRequest = DevCreateTenantRequest(slug: "slug_example", displayName: "displayName_example") // DevCreateTenantRequest | 

// Create a new tenant without authentication (dev-only). Used by the Aspire dashboard \"Create Tenant\" command.
DevAdminAPI.devAdminCreateTenant(devCreateTenantRequest: devCreateTenantRequest) { (response, error) in
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
 **devCreateTenantRequest** | [**DevCreateTenantRequest**](DevCreateTenantRequest.md) |  | 

### Return type

[**TenantCreatedDto**](TenantCreatedDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **devAdminDeleteTenant**
```swift
    open class func devAdminDeleteTenant(id: String, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Delete a tenant and all associated data without authentication (dev-only).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a tenant and all associated data without authentication (dev-only).
DevAdminAPI.devAdminDeleteTenant(id: id) { (response, error) in
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

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **devAdminExportSnapshot**
```swift
    open class func devAdminExportSnapshot(completion: @escaping (_ data: DevSnapshotDto?, _ error: Error?) -> Void)
```

Export a full snapshot of all tenants and their identity/config data. Secrets are decrypted to plaintext for portability.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Export a full snapshot of all tenants and their identity/config data. Secrets are decrypted to plaintext for portability.
DevAdminAPI.devAdminExportSnapshot() { (response, error) in
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

[**DevSnapshotDto**](DevSnapshotDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **devAdminImportScopedSnapshot**
```swift
    open class func devAdminImportScopedSnapshot(id: String, tenantSnapshotDto: TenantSnapshotDto, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Import snapshot data for a single tenant, matched by slug in the provided snapshot. Upserts referenced subjects and passkeys without affecting other tenants.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let tenantSnapshotDto = TenantSnapshotDto(tenant: TenantEntityDto(id: "id_example", slug: "slug_example", displayName: "displayName_example", isActive: false, lastReadingAt: Date(), timezone: "timezone_example", subjectName: "subjectName_example", allowAccessRequests: false, sysCreatedAt: Date(), sysUpdatedAt: Date()), subjects: [SubjectEntityDto(id: "id_example", name: "name_example", username: "username_example", accessTokenHash: "accessTokenHash_example", accessTokenPrefix: "accessTokenPrefix_example", email: "email_example", notes: "notes_example", isActive: false, isSystemSubject: false, createdAt: Date(), updatedAt: Date(), lastLoginAt: Date(), originalId: "originalId_example", preferredLanguage: "preferredLanguage_example", approvalStatus: "approvalStatus_example", accessRequestMessage: "accessRequestMessage_example", isPlatformAdmin: false)], passkeyCredentials: [PasskeyCredentialEntityDto(id: "id_example", subjectId: "subjectId_example", credentialId: "credentialId_example", publicKey: "publicKey_example", signCount: 123, transports: ["transports_example"], label: "label_example", createdAt: Date(), lastUsedAt: Date(), aaGuid: "aaGuid_example")], roles: [TenantRoleEntityDto(id: "id_example", tenantId: "tenantId_example", name: "name_example", slug: "slug_example", description: "description_example", permissions: ["permissions_example"], isSystem: false, sysCreatedAt: Date(), sysUpdatedAt: Date())], members: [TenantMemberEntityDto(id: "id_example", tenantId: "tenantId_example", subjectId: "subjectId_example", sysCreatedAt: Date(), sysUpdatedAt: Date(), directPermissions: ["directPermissions_example"], label: "label_example", limitTo24Hours: false, createdFromInviteId: "createdFromInviteId_example", lastUsedAt: Date(), lastUsedIp: "lastUsedIp_example", lastUsedUserAgent: "lastUsedUserAgent_example", revokedAt: Date())], memberRoles: [TenantMemberRoleEntityDto(id: "id_example", tenantMemberId: "tenantMemberId_example", tenantRoleId: "tenantRoleId_example", sysCreatedAt: Date())], oAuthClients: [OAuthClientEntityDto(id: "id_example", tenantId: "tenantId_example", clientId: "clientId_example", softwareId: "softwareId_example", clientName: "clientName_example", clientUri: "clientUri_example", logoUri: "logoUri_example", createdFromIp: "createdFromIp_example", displayName: "displayName_example", isKnown: false, redirectUris: "redirectUris_example", createdAt: Date(), updatedAt: Date())], connectorConfigurations: [ConnectorConfigSnapshotDto(id: "id_example", tenantId: "tenantId_example", connectorName: "connectorName_example", configurationJson: "configurationJson_example", secretsPlaintext: "TODO", schemaVersion: 123, lastModified: Date(), modifiedBy: "modifiedBy_example", sysCreatedAt: Date(), sysUpdatedAt: Date(), lastSyncAttempt: Date(), lastSuccessfulSync: Date(), lastErrorMessage: "lastErrorMessage_example", lastErrorAt: Date(), isHealthy: false)]) // TenantSnapshotDto | 

// Import snapshot data for a single tenant, matched by slug in the provided snapshot. Upserts referenced subjects and passkeys without affecting other tenants.
DevAdminAPI.devAdminImportScopedSnapshot(id: id, tenantSnapshotDto: tenantSnapshotDto) { (response, error) in
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
 **tenantSnapshotDto** | [**TenantSnapshotDto**](TenantSnapshotDto.md) |  | 

### Return type

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **devAdminImportSnapshot**
```swift
    open class func devAdminImportSnapshot(devSnapshotDto: DevSnapshotDto, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Import a snapshot, replacing all identity/config data. Wraps the entire operation in a transaction.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let devSnapshotDto = DevSnapshotDto(exportedAt: Date(), tenants: [TenantSnapshotDto(tenant: TenantEntityDto(id: "id_example", slug: "slug_example", displayName: "displayName_example", isActive: false, lastReadingAt: Date(), timezone: "timezone_example", subjectName: "subjectName_example", allowAccessRequests: false, sysCreatedAt: Date(), sysUpdatedAt: Date()), subjects: [SubjectEntityDto(id: "id_example", name: "name_example", username: "username_example", accessTokenHash: "accessTokenHash_example", accessTokenPrefix: "accessTokenPrefix_example", email: "email_example", notes: "notes_example", isActive: false, isSystemSubject: false, createdAt: Date(), updatedAt: Date(), lastLoginAt: Date(), originalId: "originalId_example", preferredLanguage: "preferredLanguage_example", approvalStatus: "approvalStatus_example", accessRequestMessage: "accessRequestMessage_example", isPlatformAdmin: false)], passkeyCredentials: [PasskeyCredentialEntityDto(id: "id_example", subjectId: "subjectId_example", credentialId: "credentialId_example", publicKey: "publicKey_example", signCount: 123, transports: ["transports_example"], label: "label_example", createdAt: Date(), lastUsedAt: Date(), aaGuid: "aaGuid_example")], roles: [TenantRoleEntityDto(id: "id_example", tenantId: "tenantId_example", name: "name_example", slug: "slug_example", description: "description_example", permissions: ["permissions_example"], isSystem: false, sysCreatedAt: Date(), sysUpdatedAt: Date())], members: [TenantMemberEntityDto(id: "id_example", tenantId: "tenantId_example", subjectId: "subjectId_example", sysCreatedAt: Date(), sysUpdatedAt: Date(), directPermissions: ["directPermissions_example"], label: "label_example", limitTo24Hours: false, createdFromInviteId: "createdFromInviteId_example", lastUsedAt: Date(), lastUsedIp: "lastUsedIp_example", lastUsedUserAgent: "lastUsedUserAgent_example", revokedAt: Date())], memberRoles: [TenantMemberRoleEntityDto(id: "id_example", tenantMemberId: "tenantMemberId_example", tenantRoleId: "tenantRoleId_example", sysCreatedAt: Date())], oAuthClients: [OAuthClientEntityDto(id: "id_example", tenantId: "tenantId_example", clientId: "clientId_example", softwareId: "softwareId_example", clientName: "clientName_example", clientUri: "clientUri_example", logoUri: "logoUri_example", createdFromIp: "createdFromIp_example", displayName: "displayName_example", isKnown: false, redirectUris: "redirectUris_example", createdAt: Date(), updatedAt: Date())], connectorConfigurations: [ConnectorConfigSnapshotDto(id: "id_example", tenantId: "tenantId_example", connectorName: "connectorName_example", configurationJson: "configurationJson_example", secretsPlaintext: "TODO", schemaVersion: 123, lastModified: Date(), modifiedBy: "modifiedBy_example", sysCreatedAt: Date(), sysUpdatedAt: Date(), lastSyncAttempt: Date(), lastSuccessfulSync: Date(), lastErrorMessage: "lastErrorMessage_example", lastErrorAt: Date(), isHealthy: false)])]) // DevSnapshotDto | 

// Import a snapshot, replacing all identity/config data. Wraps the entire operation in a transaction.
DevAdminAPI.devAdminImportSnapshot(devSnapshotDto: devSnapshotDto) { (response, error) in
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
 **devSnapshotDto** | [**DevSnapshotDto**](DevSnapshotDto.md) |  | 

### Return type

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **devAdminListTenants**
```swift
    open class func devAdminListTenants(completion: @escaping (_ data: [DevTenantSummaryDto]?, _ error: Error?) -> Void)
```

List all tenants with record counts and connector health (dev-only). Used by the Aspire dashboard \"List Tenants\" command.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List all tenants with record counts and connector health (dev-only). Used by the Aspire dashboard \"List Tenants\" command.
DevAdminAPI.devAdminListTenants() { (response, error) in
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

[**[DevTenantSummaryDto]**](DevTenantSummaryDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **devAdminSyncAll**
```swift
    open class func devAdminSyncAll(completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Trigger a sync for every configured connector across all tenants.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Trigger a sync for every configured connector across all tenants.
DevAdminAPI.devAdminSyncAll() { (response, error) in
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

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

