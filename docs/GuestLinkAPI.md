# GuestLinkAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**guestLinkActivateGuestLink**](GuestLinkAPI.md#guestlinkactivateguestlink) | **POST** /api/v4/guest-links/activate | Activate a guest link by code and receive a session cookie.
[**guestLinkCreateGuestLink**](GuestLinkAPI.md#guestlinkcreateguestlink) | **POST** /api/v4/guest-links | Create a new guest link for temporary read-only data sharing.
[**guestLinkGetGuestLinks**](GuestLinkAPI.md#guestlinkgetguestlinks) | **GET** /api/v4/guest-links | List guest links for the current user&#39;s effective subject.
[**guestLinkRevokeGuestLink**](GuestLinkAPI.md#guestlinkrevokeguestlink) | **DELETE** /api/v4/guest-links/{grantId} | Revoke an active guest link.


# **guestLinkActivateGuestLink**
```swift
    open class func guestLinkActivateGuestLink(activateGuestLinkRequest: ActivateGuestLinkRequest, completion: @escaping (_ data: ActivateGuestLinkResponse?, _ error: Error?) -> Void)
```

Activate a guest link by code and receive a session cookie.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let activateGuestLinkRequest = ActivateGuestLinkRequest(code: "code_example") // ActivateGuestLinkRequest | 

// Activate a guest link by code and receive a session cookie.
GuestLinkAPI.guestLinkActivateGuestLink(activateGuestLinkRequest: activateGuestLinkRequest) { (response, error) in
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
 **activateGuestLinkRequest** | [**ActivateGuestLinkRequest**](ActivateGuestLinkRequest.md) |  | 

### Return type

[**ActivateGuestLinkResponse**](ActivateGuestLinkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **guestLinkCreateGuestLink**
```swift
    open class func guestLinkCreateGuestLink(createGuestLinkRequest: CreateGuestLinkRequest, completion: @escaping (_ data: GuestLinkCreationResult?, _ error: Error?) -> Void)
```

Create a new guest link for temporary read-only data sharing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createGuestLinkRequest = CreateGuestLinkRequest(label: "label_example", scopes: ["scopes_example"]) // CreateGuestLinkRequest | 

// Create a new guest link for temporary read-only data sharing.
GuestLinkAPI.guestLinkCreateGuestLink(createGuestLinkRequest: createGuestLinkRequest) { (response, error) in
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
 **createGuestLinkRequest** | [**CreateGuestLinkRequest**](CreateGuestLinkRequest.md) |  | 

### Return type

[**GuestLinkCreationResult**](GuestLinkCreationResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **guestLinkGetGuestLinks**
```swift
    open class func guestLinkGetGuestLinks(completion: @escaping (_ data: [GuestLinkInfo]?, _ error: Error?) -> Void)
```

List guest links for the current user's effective subject.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List guest links for the current user's effective subject.
GuestLinkAPI.guestLinkGetGuestLinks() { (response, error) in
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

[**[GuestLinkInfo]**](GuestLinkInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **guestLinkRevokeGuestLink**
```swift
    open class func guestLinkRevokeGuestLink(grantId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Revoke an active guest link.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let grantId = "grantId_example" // String | 

// Revoke an active guest link.
GuestLinkAPI.guestLinkRevokeGuestLink(grantId: grantId) { (response, error) in
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
 **grantId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

