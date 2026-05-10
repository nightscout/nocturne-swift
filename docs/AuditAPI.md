# AuditAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auditGetAuditConfig**](AuditAPI.md#auditgetauditconfig) | **GET** /api/v4/audit/config | Get the audit configuration for the current tenant.
[**auditGetMutationAuditLog**](AuditAPI.md#auditgetmutationauditlog) | **GET** /api/v4/audit/mutations | Query mutation audit log entries for the current tenant.
[**auditGetReadAccessAuditLog**](AuditAPI.md#auditgetreadaccessauditlog) | **GET** /api/v4/audit/reads | Query read access audit log entries for the current tenant.
[**auditUpdateAuditConfig**](AuditAPI.md#auditupdateauditconfig) | **PUT** /api/v4/audit/config | Create or update the audit configuration for the current tenant.


# **auditGetAuditConfig**
```swift
    open class func auditGetAuditConfig(completion: @escaping (_ data: AuditConfigDto?, _ error: Error?) -> Void)
```

Get the audit configuration for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get the audit configuration for the current tenant.
AuditAPI.auditGetAuditConfig() { (response, error) in
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

[**AuditConfigDto**](AuditConfigDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auditGetMutationAuditLog**
```swift
    open class func auditGetMutationAuditLog(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, subjectId: String? = nil, entityType: String? = nil, action: String? = nil, entityId: String? = nil, completion: @escaping (_ data: PaginatedResponseOfMutationAuditDto?, _ error: Error?) -> Void)
```

Query mutation audit log entries for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "created_at_desc")
let subjectId = "subjectId_example" // String |  (optional)
let entityType = "entityType_example" // String |  (optional)
let action = "action_example" // String |  (optional)
let entityId = "entityId_example" // String |  (optional)

// Query mutation audit log entries for the current tenant.
AuditAPI.auditGetMutationAuditLog(from: from, to: to, limit: limit, offset: offset, sort: sort, subjectId: subjectId, entityType: entityType, action: action, entityId: entityId) { (response, error) in
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
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** |  | [optional] [default to &quot;created_at_desc&quot;]
 **subjectId** | **String** |  | [optional] 
 **entityType** | **String** |  | [optional] 
 **action** | **String** |  | [optional] 
 **entityId** | **String** |  | [optional] 

### Return type

[**PaginatedResponseOfMutationAuditDto**](PaginatedResponseOfMutationAuditDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auditGetReadAccessAuditLog**
```swift
    open class func auditGetReadAccessAuditLog(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, subjectId: String? = nil, entityType: String? = nil, endpoint: String? = nil, statusCode: Int? = nil, completion: @escaping (_ data: PaginatedResponseOfReadAccessAuditDto?, _ error: Error?) -> Void)
```

Query read access audit log entries for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "created_at_desc")
let subjectId = "subjectId_example" // String |  (optional)
let entityType = "entityType_example" // String |  (optional)
let endpoint = "endpoint_example" // String |  (optional)
let statusCode = 987 // Int |  (optional)

// Query read access audit log entries for the current tenant.
AuditAPI.auditGetReadAccessAuditLog(from: from, to: to, limit: limit, offset: offset, sort: sort, subjectId: subjectId, entityType: entityType, endpoint: endpoint, statusCode: statusCode) { (response, error) in
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
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** |  | [optional] [default to &quot;created_at_desc&quot;]
 **subjectId** | **String** |  | [optional] 
 **entityType** | **String** |  | [optional] 
 **endpoint** | **String** |  | [optional] 
 **statusCode** | **Int** |  | [optional] 

### Return type

[**PaginatedResponseOfReadAccessAuditDto**](PaginatedResponseOfReadAccessAuditDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auditUpdateAuditConfig**
```swift
    open class func auditUpdateAuditConfig(auditConfigDto: AuditConfigDto, completion: @escaping (_ data: AuditConfigDto?, _ error: Error?) -> Void)
```

Create or update the audit configuration for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let auditConfigDto = AuditConfigDto(readAuditEnabled: false, readAuditRetentionDays: 123, mutationAuditRetentionDays: 123) // AuditConfigDto | 

// Create or update the audit configuration for the current tenant.
AuditAPI.auditUpdateAuditConfig(auditConfigDto: auditConfigDto) { (response, error) in
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
 **auditConfigDto** | [**AuditConfigDto**](AuditConfigDto.md) |  | 

### Return type

[**AuditConfigDto**](AuditConfigDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

