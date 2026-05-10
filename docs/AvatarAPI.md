# AvatarAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**avatarDelete**](AvatarAPI.md#avatardelete) | **DELETE** /api/v4/me/avatar | Delete the current subject&#39;s avatar.
[**avatarGet**](AvatarAPI.md#avatarget) | **GET** /api/v4/me/avatar | Serve the current subject&#39;s avatar image.
[**avatarUpload**](AvatarAPI.md#avatarupload) | **POST** /api/v4/me/avatar | Upload or replace the current subject&#39;s avatar. Image is resized to 256x256 WebP.


# **avatarDelete**
```swift
    open class func avatarDelete(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete the current subject's avatar.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Delete the current subject's avatar.
AvatarAPI.avatarDelete() { (response, error) in
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

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **avatarGet**
```swift
    open class func avatarGet(id: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Serve the current subject's avatar image.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String |  (optional)

// Serve the current subject's avatar image.
AvatarAPI.avatarGet(id: id) { (response, error) in
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
 **id** | **String** |  | [optional] 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **avatarUpload**
```swift
    open class func avatarUpload(contentType: String? = nil, contentDisposition: String? = nil, headers: [JSONValue]? = nil, length: Int64? = nil, name: String? = nil, fileName: String? = nil, completion: @escaping (_ data: AvatarUploadResponse?, _ error: Error?) -> Void)
```

Upload or replace the current subject's avatar. Image is resized to 256x256 WebP.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let contentType = "contentType_example" // String |  (optional)
let contentDisposition = "contentDisposition_example" // String |  (optional)
let headers = [123] // [JSONValue] |  (optional)
let length = 987 // Int64 |  (optional)
let name = "name_example" // String |  (optional)
let fileName = "fileName_example" // String |  (optional)

// Upload or replace the current subject's avatar. Image is resized to 256x256 WebP.
AvatarAPI.avatarUpload(contentType: contentType, contentDisposition: contentDisposition, headers: headers, length: length, name: name, fileName: fileName) { (response, error) in
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
 **contentType** | **String** |  | [optional] 
 **contentDisposition** | **String** |  | [optional] 
 **headers** | [**[JSONValue]**](JSONValue.md) |  | [optional] 
 **length** | **Int64** |  | [optional] 
 **name** | **String** |  | [optional] 
 **fileName** | **String** |  | [optional] 

### Return type

[**AvatarUploadResponse**](AvatarUploadResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

