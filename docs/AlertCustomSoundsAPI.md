# AlertCustomSoundsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**alertCustomSoundsDeleteSound**](AlertCustomSoundsAPI.md#alertcustomsoundsdeletesound) | **DELETE** /api/v4/alert-sounds/{id} | Delete a custom sound.
[**alertCustomSoundsGetSounds**](AlertCustomSoundsAPI.md#alertcustomsoundsgetsounds) | **GET** /api/v4/alert-sounds | List all custom sounds for the current tenant (metadata only, no audio data).
[**alertCustomSoundsStreamSound**](AlertCustomSoundsAPI.md#alertcustomsoundsstreamsound) | **GET** /api/v4/alert-sounds/{id}/stream | Stream the raw audio bytes for a custom sound.
[**alertCustomSoundsUploadSound**](AlertCustomSoundsAPI.md#alertcustomsoundsuploadsound) | **POST** /api/v4/alert-sounds | Upload a custom alert sound file.


# **alertCustomSoundsDeleteSound**
```swift
    open class func alertCustomSoundsDeleteSound(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a custom sound.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a custom sound.
AlertCustomSoundsAPI.alertCustomSoundsDeleteSound(id: id) { (response, error) in
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

# **alertCustomSoundsGetSounds**
```swift
    open class func alertCustomSoundsGetSounds(completion: @escaping (_ data: [AlertCustomSoundResponse]?, _ error: Error?) -> Void)
```

List all custom sounds for the current tenant (metadata only, no audio data).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List all custom sounds for the current tenant (metadata only, no audio data).
AlertCustomSoundsAPI.alertCustomSoundsGetSounds() { (response, error) in
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

[**[AlertCustomSoundResponse]**](AlertCustomSoundResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertCustomSoundsStreamSound**
```swift
    open class func alertCustomSoundsStreamSound(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Stream the raw audio bytes for a custom sound.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Stream the raw audio bytes for a custom sound.
AlertCustomSoundsAPI.alertCustomSoundsStreamSound(id: id) { (response, error) in
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

# **alertCustomSoundsUploadSound**
```swift
    open class func alertCustomSoundsUploadSound(contentType: String? = nil, contentDisposition: String? = nil, headers: [JSONValue]? = nil, length: Int64? = nil, name: String? = nil, fileName: String? = nil, completion: @escaping (_ data: AlertCustomSoundResponse?, _ error: Error?) -> Void)
```

Upload a custom alert sound file.

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

// Upload a custom alert sound file.
AlertCustomSoundsAPI.alertCustomSoundsUploadSound(contentType: contentType, contentDisposition: contentDisposition, headers: headers, length: length, name: name, fileName: fileName) { (response, error) in
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

[**AlertCustomSoundResponse**](AlertCustomSoundResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

