# InsulinCatalogAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**insulinCatalogGetCatalog**](InsulinCatalogAPI.md#insulincataloggetcatalog) | **GET** /api/v4/insulins/catalog | Get all known insulin formulations.
[**insulinCatalogGetCatalogByCategory**](InsulinCatalogAPI.md#insulincataloggetcatalogbycategory) | **GET** /api/v4/insulins/catalog/{category} | Get insulin formulations filtered by category.


# **insulinCatalogGetCatalog**
```swift
    open class func insulinCatalogGetCatalog(completion: @escaping (_ data: [InsulinFormulation]?, _ error: Error?) -> Void)
```

Get all known insulin formulations.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all known insulin formulations.
InsulinCatalogAPI.insulinCatalogGetCatalog() { (response, error) in
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

[**[InsulinFormulation]**](InsulinFormulation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insulinCatalogGetCatalogByCategory**
```swift
    open class func insulinCatalogGetCatalogByCategory(category: InsulinCategory, completion: @escaping (_ data: [InsulinFormulation]?, _ error: Error?) -> Void)
```

Get insulin formulations filtered by category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let category = InsulinCategory() // InsulinCategory | 

// Get insulin formulations filtered by category.
InsulinCatalogAPI.insulinCatalogGetCatalogByCategory(category: category) { (response, error) in
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
 **category** | [**InsulinCategory**](.md) |  | 

### Return type

[**[InsulinFormulation]**](InsulinFormulation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

