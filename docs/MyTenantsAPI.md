# MyTenantsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**myTenantsCreateTenant**](MyTenantsAPI.md#mytenantscreatetenant) | **POST** /api/v4/me/tenants | 
[**myTenantsGetMyTenants**](MyTenantsAPI.md#mytenantsgetmytenants) | **GET** /api/v4/me/tenants | 
[**myTenantsValidateSlug**](MyTenantsAPI.md#mytenantsvalidateslug) | **GET** /api/v4/me/tenants/validate-slug | 


# **myTenantsCreateTenant**
```swift
    open class func myTenantsCreateTenant(createMyTenantRequest: CreateMyTenantRequest, completion: @escaping (_ data: TenantCreatedDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createMyTenantRequest = CreateMyTenantRequest(slug: "slug_example", displayName: "displayName_example") // CreateMyTenantRequest | 

MyTenantsAPI.myTenantsCreateTenant(createMyTenantRequest: createMyTenantRequest) { (response, error) in
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
 **createMyTenantRequest** | [**CreateMyTenantRequest**](CreateMyTenantRequest.md) |  | 

### Return type

[**TenantCreatedDto**](TenantCreatedDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **myTenantsGetMyTenants**
```swift
    open class func myTenantsGetMyTenants(completion: @escaping (_ data: [TenantDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


MyTenantsAPI.myTenantsGetMyTenants() { (response, error) in
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

# **myTenantsValidateSlug**
```swift
    open class func myTenantsValidateSlug(slug: String? = nil, completion: @escaping (_ data: SlugValidationResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let slug = "slug_example" // String |  (optional)

MyTenantsAPI.myTenantsValidateSlug(slug: slug) { (response, error) in
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
 **slug** | **String** |  | [optional] 

### Return type

[**SlugValidationResult**](SlugValidationResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

