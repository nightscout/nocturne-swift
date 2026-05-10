# V4BGChecksAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bGCheckCreate**](V4BGChecksAPI.md#bgcheckcreate) | **POST** /api/v4/observations/bg-checks | 
[**bGCheckDelete**](V4BGChecksAPI.md#bgcheckdelete) | **DELETE** /api/v4/observations/bg-checks/{id} | 
[**bGCheckGetAll**](V4BGChecksAPI.md#bgcheckgetall) | **GET** /api/v4/observations/bg-checks | 
[**bGCheckGetById**](V4BGChecksAPI.md#bgcheckgetbyid) | **GET** /api/v4/observations/bg-checks/{id} | 
[**bGCheckUpdate**](V4BGChecksAPI.md#bgcheckupdate) | **PUT** /api/v4/observations/bg-checks/{id} | 


# **bGCheckCreate**
```swift
    open class func bGCheckCreate(upsertBGCheckRequest: UpsertBGCheckRequest, completion: @escaping (_ data: BGCheck?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertBGCheckRequest = UpsertBGCheckRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", glucose: 123, units: GlucoseUnit(), glucoseType: GlucoseType(), syncIdentifier: "syncIdentifier_example") // UpsertBGCheckRequest | 

V4BGChecksAPI.bGCheckCreate(upsertBGCheckRequest: upsertBGCheckRequest) { (response, error) in
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
 **upsertBGCheckRequest** | [**UpsertBGCheckRequest**](UpsertBGCheckRequest.md) |  | 

### Return type

[**BGCheck**](BGCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bGCheckDelete**
```swift
    open class func bGCheckDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4BGChecksAPI.bGCheckDelete(id: id) { (response, error) in
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

# **bGCheckGetAll**
```swift
    open class func bGCheckGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfBGCheck?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")
let device = "device_example" // String |  (optional)
let source = "source_example" // String |  (optional)

V4BGChecksAPI.bGCheckGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** |  | [optional] [default to &quot;timestamp_desc&quot;]
 **device** | **String** |  | [optional] 
 **source** | **String** |  | [optional] 

### Return type

[**PaginatedResponseOfBGCheck**](PaginatedResponseOfBGCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bGCheckGetById**
```swift
    open class func bGCheckGetById(id: String, completion: @escaping (_ data: BGCheck?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4BGChecksAPI.bGCheckGetById(id: id) { (response, error) in
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

[**BGCheck**](BGCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bGCheckUpdate**
```swift
    open class func bGCheckUpdate(id: String, upsertBGCheckRequest: UpsertBGCheckRequest, completion: @escaping (_ data: BGCheck?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertBGCheckRequest = UpsertBGCheckRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", glucose: 123, units: GlucoseUnit(), glucoseType: GlucoseType(), syncIdentifier: "syncIdentifier_example") // UpsertBGCheckRequest | 

V4BGChecksAPI.bGCheckUpdate(id: id, upsertBGCheckRequest: upsertBGCheckRequest) { (response, error) in
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
 **upsertBGCheckRequest** | [**UpsertBGCheckRequest**](UpsertBGCheckRequest.md) |  | 

### Return type

[**BGCheck**](BGCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

