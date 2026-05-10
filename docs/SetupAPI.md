# SetupAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**setupCreateTenant**](SetupAPI.md#setupcreatetenant) | **POST** /api/v4/setup/tenant | Create the first tenant on a fresh install. Only succeeds when zero tenants exist.
[**setupOidcCallback**](SetupAPI.md#setupoidccallback) | **GET** /api/v4/setup/oidc/callback | OIDC callback for setup owner creation. Called by the OIDC provider after authentication. Links the identity, issues session cookies, and redirects to /setup.
[**setupOwnerComplete**](SetupAPI.md#setupownercomplete) | **POST** /api/v4/setup/owner/complete | Complete passkey registration for the first owner account. Verifies attestation, generates recovery codes, issues a full JWT session.
[**setupOwnerOidc**](SetupAPI.md#setupowneroidc) | **POST** /api/v4/setup/owner/oidc | Initiate OIDC-based owner creation. Creates the subject and owner role, then redirects to the OIDC provider to link an identity.
[**setupOwnerOptions**](SetupAPI.md#setupowneroptions) | **POST** /api/v4/setup/owner/options | Generate passkey registration options for the first owner account. Guard: exactly one tenant must exist with zero non-system members.
[**setupValidateUsername**](SetupAPI.md#setupvalidateusername) | **GET** /api/v4/setup/validate-username | Check whether a username is available for the owner account.


# **setupCreateTenant**
```swift
    open class func setupCreateTenant(setupTenantRequest: SetupTenantRequest, completion: @escaping (_ data: SetupTenantResponse?, _ error: Error?) -> Void)
```

Create the first tenant on a fresh install. Only succeeds when zero tenants exist.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let setupTenantRequest = SetupTenantRequest(slug: "slug_example", displayName: "displayName_example") // SetupTenantRequest | 

// Create the first tenant on a fresh install. Only succeeds when zero tenants exist.
SetupAPI.setupCreateTenant(setupTenantRequest: setupTenantRequest) { (response, error) in
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
 **setupTenantRequest** | [**SetupTenantRequest**](SetupTenantRequest.md) |  | 

### Return type

[**SetupTenantResponse**](SetupTenantResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setupOidcCallback**
```swift
    open class func setupOidcCallback(code: String? = nil, state: String? = nil, error: String? = nil, errorDescription: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

OIDC callback for setup owner creation. Called by the OIDC provider after authentication. Links the identity, issues session cookies, and redirects to /setup.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let code = "code_example" // String |  (optional)
let state = "state_example" // String |  (optional)
let error = "error_example" // String |  (optional)
let errorDescription = "errorDescription_example" // String |  (optional)

// OIDC callback for setup owner creation. Called by the OIDC provider after authentication. Links the identity, issues session cookies, and redirects to /setup.
SetupAPI.setupOidcCallback(code: code, state: state, error: error, errorDescription: errorDescription) { (response, error) in
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
 **code** | **String** |  | [optional] 
 **state** | **String** |  | [optional] 
 **error** | **String** |  | [optional] 
 **errorDescription** | **String** |  | [optional] 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setupOwnerComplete**
```swift
    open class func setupOwnerComplete(setupOwnerCompleteRequest: SetupOwnerCompleteRequest, completion: @escaping (_ data: SetupOwnerCompleteResponse?, _ error: Error?) -> Void)
```

Complete passkey registration for the first owner account. Verifies attestation, generates recovery codes, issues a full JWT session.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let setupOwnerCompleteRequest = SetupOwnerCompleteRequest(attestationResponseJson: "attestationResponseJson_example", challengeToken: "challengeToken_example") // SetupOwnerCompleteRequest | 

// Complete passkey registration for the first owner account. Verifies attestation, generates recovery codes, issues a full JWT session.
SetupAPI.setupOwnerComplete(setupOwnerCompleteRequest: setupOwnerCompleteRequest) { (response, error) in
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
 **setupOwnerCompleteRequest** | [**SetupOwnerCompleteRequest**](SetupOwnerCompleteRequest.md) |  | 

### Return type

[**SetupOwnerCompleteResponse**](SetupOwnerCompleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setupOwnerOidc**
```swift
    open class func setupOwnerOidc(setupOwnerOidcRequest: SetupOwnerOidcRequest, completion: @escaping (_ data: SetupOwnerOidcResponse?, _ error: Error?) -> Void)
```

Initiate OIDC-based owner creation. Creates the subject and owner role, then redirects to the OIDC provider to link an identity.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let setupOwnerOidcRequest = SetupOwnerOidcRequest(username: "username_example", displayName: "displayName_example", providerId: "providerId_example") // SetupOwnerOidcRequest | 

// Initiate OIDC-based owner creation. Creates the subject and owner role, then redirects to the OIDC provider to link an identity.
SetupAPI.setupOwnerOidc(setupOwnerOidcRequest: setupOwnerOidcRequest) { (response, error) in
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
 **setupOwnerOidcRequest** | [**SetupOwnerOidcRequest**](SetupOwnerOidcRequest.md) |  | 

### Return type

[**SetupOwnerOidcResponse**](SetupOwnerOidcResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setupOwnerOptions**
```swift
    open class func setupOwnerOptions(setupOwnerOptionsRequest: SetupOwnerOptionsRequest, completion: @escaping (_ data: SetupOwnerOptionsResponse?, _ error: Error?) -> Void)
```

Generate passkey registration options for the first owner account. Guard: exactly one tenant must exist with zero non-system members.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let setupOwnerOptionsRequest = SetupOwnerOptionsRequest(username: "username_example", displayName: "displayName_example") // SetupOwnerOptionsRequest | 

// Generate passkey registration options for the first owner account. Guard: exactly one tenant must exist with zero non-system members.
SetupAPI.setupOwnerOptions(setupOwnerOptionsRequest: setupOwnerOptionsRequest) { (response, error) in
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
 **setupOwnerOptionsRequest** | [**SetupOwnerOptionsRequest**](SetupOwnerOptionsRequest.md) |  | 

### Return type

[**SetupOwnerOptionsResponse**](SetupOwnerOptionsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setupValidateUsername**
```swift
    open class func setupValidateUsername(username: String? = nil, completion: @escaping (_ data: SlugValidationResult?, _ error: Error?) -> Void)
```

Check whether a username is available for the owner account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let username = "username_example" // String |  (optional)

// Check whether a username is available for the owner account.
SetupAPI.setupValidateUsername(username: username) { (response, error) in
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
 **username** | **String** |  | [optional] 

### Return type

[**SlugValidationResult**](SlugValidationResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

