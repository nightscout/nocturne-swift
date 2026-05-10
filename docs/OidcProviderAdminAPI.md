# OidcProviderAdminAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**oidcProviderAdminCreate**](OidcProviderAdminAPI.md#oidcprovideradmincreate) | **POST** /api/v4/admin/oidc-providers | 
[**oidcProviderAdminDelete**](OidcProviderAdminAPI.md#oidcprovideradmindelete) | **DELETE** /api/v4/admin/oidc-providers/{id} | 
[**oidcProviderAdminDisable**](OidcProviderAdminAPI.md#oidcprovideradmindisable) | **POST** /api/v4/admin/oidc-providers/{id}/disable | 
[**oidcProviderAdminEnable**](OidcProviderAdminAPI.md#oidcprovideradminenable) | **POST** /api/v4/admin/oidc-providers/{id}/enable | 
[**oidcProviderAdminGetAll**](OidcProviderAdminAPI.md#oidcprovideradmingetall) | **GET** /api/v4/admin/oidc-providers | 
[**oidcProviderAdminGetById**](OidcProviderAdminAPI.md#oidcprovideradmingetbyid) | **GET** /api/v4/admin/oidc-providers/{id} | 
[**oidcProviderAdminGetConfigManaged**](OidcProviderAdminAPI.md#oidcprovideradmingetconfigmanaged) | **GET** /api/v4/admin/oidc-providers/config-managed | 
[**oidcProviderAdminTestExisting**](OidcProviderAdminAPI.md#oidcprovideradmintestexisting) | **POST** /api/v4/admin/oidc-providers/{id}/test | 
[**oidcProviderAdminTestUnsaved**](OidcProviderAdminAPI.md#oidcprovideradmintestunsaved) | **POST** /api/v4/admin/oidc-providers/test | 
[**oidcProviderAdminUpdate**](OidcProviderAdminAPI.md#oidcprovideradminupdate) | **PUT** /api/v4/admin/oidc-providers/{id} | 


# **oidcProviderAdminCreate**
```swift
    open class func oidcProviderAdminCreate(createOidcProviderRequest: CreateOidcProviderRequest, completion: @escaping (_ data: OidcProviderResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createOidcProviderRequest = CreateOidcProviderRequest(name: "name_example", issuerUrl: "issuerUrl_example", clientId: "clientId_example", clientSecret: "clientSecret_example", scopes: ["scopes_example"], claimMappings: "TODO", defaultRoles: ["defaultRoles_example"], isEnabled: false, displayOrder: 123, icon: "icon_example", buttonColor: "buttonColor_example") // CreateOidcProviderRequest | 

OidcProviderAdminAPI.oidcProviderAdminCreate(createOidcProviderRequest: createOidcProviderRequest) { (response, error) in
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
 **createOidcProviderRequest** | [**CreateOidcProviderRequest**](CreateOidcProviderRequest.md) |  | 

### Return type

[**OidcProviderResponse**](OidcProviderResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oidcProviderAdminDelete**
```swift
    open class func oidcProviderAdminDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

OidcProviderAdminAPI.oidcProviderAdminDelete(id: id) { (response, error) in
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

# **oidcProviderAdminDisable**
```swift
    open class func oidcProviderAdminDisable(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

OidcProviderAdminAPI.oidcProviderAdminDisable(id: id) { (response, error) in
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

# **oidcProviderAdminEnable**
```swift
    open class func oidcProviderAdminEnable(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

OidcProviderAdminAPI.oidcProviderAdminEnable(id: id) { (response, error) in
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

# **oidcProviderAdminGetAll**
```swift
    open class func oidcProviderAdminGetAll(completion: @escaping (_ data: [OidcProviderResponse]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


OidcProviderAdminAPI.oidcProviderAdminGetAll() { (response, error) in
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

[**[OidcProviderResponse]**](OidcProviderResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oidcProviderAdminGetById**
```swift
    open class func oidcProviderAdminGetById(id: String, completion: @escaping (_ data: OidcProviderResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

OidcProviderAdminAPI.oidcProviderAdminGetById(id: id) { (response, error) in
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

[**OidcProviderResponse**](OidcProviderResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oidcProviderAdminGetConfigManaged**
```swift
    open class func oidcProviderAdminGetConfigManaged(completion: @escaping (_ data: ConfigManagedResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


OidcProviderAdminAPI.oidcProviderAdminGetConfigManaged() { (response, error) in
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

[**ConfigManagedResponse**](ConfigManagedResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oidcProviderAdminTestExisting**
```swift
    open class func oidcProviderAdminTestExisting(id: String, completion: @escaping (_ data: OidcProviderTestResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

OidcProviderAdminAPI.oidcProviderAdminTestExisting(id: id) { (response, error) in
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

[**OidcProviderTestResult**](OidcProviderTestResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oidcProviderAdminTestUnsaved**
```swift
    open class func oidcProviderAdminTestUnsaved(testProviderRequest: TestProviderRequest, completion: @escaping (_ data: OidcProviderTestResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let testProviderRequest = TestProviderRequest(issuerUrl: "issuerUrl_example", clientId: "clientId_example", clientSecret: "clientSecret_example") // TestProviderRequest | 

OidcProviderAdminAPI.oidcProviderAdminTestUnsaved(testProviderRequest: testProviderRequest) { (response, error) in
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
 **testProviderRequest** | [**TestProviderRequest**](TestProviderRequest.md) |  | 

### Return type

[**OidcProviderTestResult**](OidcProviderTestResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oidcProviderAdminUpdate**
```swift
    open class func oidcProviderAdminUpdate(id: String, updateOidcProviderRequest: UpdateOidcProviderRequest, completion: @escaping (_ data: OidcProviderResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateOidcProviderRequest = UpdateOidcProviderRequest(name: "name_example", issuerUrl: "issuerUrl_example", clientId: "clientId_example", clientSecret: "clientSecret_example", scopes: ["scopes_example"], claimMappings: "TODO", defaultRoles: ["defaultRoles_example"], isEnabled: false, displayOrder: 123, icon: "icon_example", buttonColor: "buttonColor_example") // UpdateOidcProviderRequest | 

OidcProviderAdminAPI.oidcProviderAdminUpdate(id: id, updateOidcProviderRequest: updateOidcProviderRequest) { (response, error) in
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
 **updateOidcProviderRequest** | [**UpdateOidcProviderRequest**](UpdateOidcProviderRequest.md) |  | 

### Return type

[**OidcProviderResponse**](OidcProviderResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

