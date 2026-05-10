# V4MeterGlucoseAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**meterGlucoseCreate**](V4MeterGlucoseAPI.md#meterglucosecreate) | **POST** /api/v4/glucose/meter | 
[**meterGlucoseDelete**](V4MeterGlucoseAPI.md#meterglucosedelete) | **DELETE** /api/v4/glucose/meter/{id} | 
[**meterGlucoseGetAll**](V4MeterGlucoseAPI.md#meterglucosegetall) | **GET** /api/v4/glucose/meter | 
[**meterGlucoseGetById**](V4MeterGlucoseAPI.md#meterglucosegetbyid) | **GET** /api/v4/glucose/meter/{id} | 
[**meterGlucoseUpdate**](V4MeterGlucoseAPI.md#meterglucoseupdate) | **PUT** /api/v4/glucose/meter/{id} | 


# **meterGlucoseCreate**
```swift
    open class func meterGlucoseCreate(upsertMeterGlucoseRequest: UpsertMeterGlucoseRequest, completion: @escaping (_ data: MeterGlucose?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertMeterGlucoseRequest = UpsertMeterGlucoseRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", mgdl: 123) // UpsertMeterGlucoseRequest | 

V4MeterGlucoseAPI.meterGlucoseCreate(upsertMeterGlucoseRequest: upsertMeterGlucoseRequest) { (response, error) in
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
 **upsertMeterGlucoseRequest** | [**UpsertMeterGlucoseRequest**](UpsertMeterGlucoseRequest.md) |  | 

### Return type

[**MeterGlucose**](MeterGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **meterGlucoseDelete**
```swift
    open class func meterGlucoseDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4MeterGlucoseAPI.meterGlucoseDelete(id: id) { (response, error) in
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

# **meterGlucoseGetAll**
```swift
    open class func meterGlucoseGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfMeterGlucose?, _ error: Error?) -> Void)
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

V4MeterGlucoseAPI.meterGlucoseGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfMeterGlucose**](PaginatedResponseOfMeterGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **meterGlucoseGetById**
```swift
    open class func meterGlucoseGetById(id: String, completion: @escaping (_ data: MeterGlucose?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4MeterGlucoseAPI.meterGlucoseGetById(id: id) { (response, error) in
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

[**MeterGlucose**](MeterGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **meterGlucoseUpdate**
```swift
    open class func meterGlucoseUpdate(id: String, upsertMeterGlucoseRequest: UpsertMeterGlucoseRequest, completion: @escaping (_ data: MeterGlucose?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertMeterGlucoseRequest = UpsertMeterGlucoseRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", mgdl: 123) // UpsertMeterGlucoseRequest | 

V4MeterGlucoseAPI.meterGlucoseUpdate(id: id, upsertMeterGlucoseRequest: upsertMeterGlucoseRequest) { (response, error) in
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
 **upsertMeterGlucoseRequest** | [**UpsertMeterGlucoseRequest**](UpsertMeterGlucoseRequest.md) |  | 

### Return type

[**MeterGlucose**](MeterGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

