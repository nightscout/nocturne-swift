# DeviceCatalogAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deviceCatalogGetCatalog**](DeviceCatalogAPI.md#devicecataloggetcatalog) | **GET** /api/v4/devices/catalog | Get all known device models.
[**deviceCatalogGetCatalogByCategory**](DeviceCatalogAPI.md#devicecataloggetcatalogbycategory) | **GET** /api/v4/devices/catalog/{category} | Get device models filtered by category.


# **deviceCatalogGetCatalog**
```swift
    open class func deviceCatalogGetCatalog(completion: @escaping (_ data: [DeviceCatalogEntry]?, _ error: Error?) -> Void)
```

Get all known device models.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all known device models.
DeviceCatalogAPI.deviceCatalogGetCatalog() { (response, error) in
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

[**[DeviceCatalogEntry]**](DeviceCatalogEntry.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceCatalogGetCatalogByCategory**
```swift
    open class func deviceCatalogGetCatalogByCategory(category: DeviceCategory, completion: @escaping (_ data: [DeviceCatalogEntry]?, _ error: Error?) -> Void)
```

Get device models filtered by category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let category = DeviceCategory() // DeviceCategory | 

// Get device models filtered by category.
DeviceCatalogAPI.deviceCatalogGetCatalogByCategory(category: category) { (response, error) in
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
 **category** | [**DeviceCategory**](.md) |  | 

### Return type

[**[DeviceCatalogEntry]**](DeviceCatalogEntry.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

