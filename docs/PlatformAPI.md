# PlatformAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**platformCreateTenant**](PlatformAPI.md#platformcreatetenant) | **POST** /api/v4/platform/tenants | Creates a new tenant with the authenticated subject as owner. Requires OperatorConfiguration.AllowSelfServiceCreation to be enabled.
[**platformGetTenants**](PlatformAPI.md#platformgettenants) | **GET** /api/v4/platform/tenants | Returns all tenants the authenticated subject is a member of.
[**platformGetTransitionStatus**](PlatformAPI.md#platformgettransitionstatus) | **GET** /api/v4/platform/transition-status | Returns the current multitenancy configuration status. Used by the frontend to display subdomain URLs and transition notices.


# **platformCreateTenant**
```swift
    open class func platformCreateTenant(createPlatformTenantRequest: CreatePlatformTenantRequest, completion: @escaping (_ data: TenantCreatedDto?, _ error: Error?) -> Void)
```

Creates a new tenant with the authenticated subject as owner. Requires OperatorConfiguration.AllowSelfServiceCreation to be enabled.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createPlatformTenantRequest = CreatePlatformTenantRequest(slug: "slug_example", displayName: "displayName_example") // CreatePlatformTenantRequest | 

// Creates a new tenant with the authenticated subject as owner. Requires OperatorConfiguration.AllowSelfServiceCreation to be enabled.
PlatformAPI.platformCreateTenant(createPlatformTenantRequest: createPlatformTenantRequest) { (response, error) in
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
 **createPlatformTenantRequest** | [**CreatePlatformTenantRequest**](CreatePlatformTenantRequest.md) |  | 

### Return type

[**TenantCreatedDto**](TenantCreatedDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformGetTenants**
```swift
    open class func platformGetTenants(completion: @escaping (_ data: [TenantDto]?, _ error: Error?) -> Void)
```

Returns all tenants the authenticated subject is a member of.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Returns all tenants the authenticated subject is a member of.
PlatformAPI.platformGetTenants() { (response, error) in
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

# **platformGetTransitionStatus**
```swift
    open class func platformGetTransitionStatus(completion: @escaping (_ data: TransitionStatusDto?, _ error: Error?) -> Void)
```

Returns the current multitenancy configuration status. Used by the frontend to display subdomain URLs and transition notices.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Returns the current multitenancy configuration status. Used by the frontend to display subdomain URLs and transition notices.
PlatformAPI.platformGetTransitionStatus() { (response, error) in
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

[**TransitionStatusDto**](TransitionStatusDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

