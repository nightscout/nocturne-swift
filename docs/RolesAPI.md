# RolesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**roleCreateRole**](RolesAPI.md#rolecreaterole) | **POST** /api/v4/roles | Create a custom role.
[**roleDeleteRole**](RolesAPI.md#roledeleterole) | **DELETE** /api/v4/roles/{id} | Delete a role.
[**roleGetRoles**](RolesAPI.md#rolegetroles) | **GET** /api/v4/roles | List roles for the current tenant.
[**roleUpdateRole**](RolesAPI.md#roleupdaterole) | **PUT** /api/v4/roles/{id} | Update a role.


# **roleCreateRole**
```swift
    open class func roleCreateRole(createRoleRequest: CreateRoleRequest, completion: @escaping (_ data: TenantRoleDto?, _ error: Error?) -> Void)
```

Create a custom role.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createRoleRequest = CreateRoleRequest(name: "name_example", description: "description_example", permissions: ["permissions_example"]) // CreateRoleRequest | 

// Create a custom role.
RolesAPI.roleCreateRole(createRoleRequest: createRoleRequest) { (response, error) in
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
 **createRoleRequest** | [**CreateRoleRequest**](CreateRoleRequest.md) |  | 

### Return type

[**TenantRoleDto**](TenantRoleDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **roleDeleteRole**
```swift
    open class func roleDeleteRole(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a role.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a role.
RolesAPI.roleDeleteRole(id: id) { (response, error) in
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

# **roleGetRoles**
```swift
    open class func roleGetRoles(completion: @escaping (_ data: [TenantRoleDto]?, _ error: Error?) -> Void)
```

List roles for the current tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List roles for the current tenant.
RolesAPI.roleGetRoles() { (response, error) in
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

[**[TenantRoleDto]**](TenantRoleDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **roleUpdateRole**
```swift
    open class func roleUpdateRole(id: String, updateRoleRequest: UpdateRoleRequest, completion: @escaping (_ data: TenantRoleDto?, _ error: Error?) -> Void)
```

Update a role.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateRoleRequest = UpdateRoleRequest(name: "name_example", description: "description_example", permissions: ["permissions_example"]) // UpdateRoleRequest | 

// Update a role.
RolesAPI.roleUpdateRole(id: id, updateRoleRequest: updateRoleRequest) { (response, error) in
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
 **updateRoleRequest** | [**UpdateRoleRequest**](UpdateRoleRequest.md) |  | 

### Return type

[**TenantRoleDto**](TenantRoleDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

