# V4SensorGlucoseAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**sensorGlucoseCreate**](V4SensorGlucoseAPI.md#sensorglucosecreate) | **POST** /api/v4/glucose/sensor | 
[**sensorGlucoseDelete**](V4SensorGlucoseAPI.md#sensorglucosedelete) | **DELETE** /api/v4/glucose/sensor/{id} | 
[**sensorGlucoseGetAll**](V4SensorGlucoseAPI.md#sensorglucosegetall) | **GET** /api/v4/glucose/sensor | 
[**sensorGlucoseGetById**](V4SensorGlucoseAPI.md#sensorglucosegetbyid) | **GET** /api/v4/glucose/sensor/{id} | 
[**sensorGlucoseUpdate**](V4SensorGlucoseAPI.md#sensorglucoseupdate) | **PUT** /api/v4/glucose/sensor/{id} | 


# **sensorGlucoseCreate**
```swift
    open class func sensorGlucoseCreate(upsertSensorGlucoseRequest: UpsertSensorGlucoseRequest, completion: @escaping (_ data: SensorGlucose?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertSensorGlucoseRequest = UpsertSensorGlucoseRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", mgdl: 123, direction: GlucoseDirection(), trendRate: 123, noise: 123) // UpsertSensorGlucoseRequest | 

V4SensorGlucoseAPI.sensorGlucoseCreate(upsertSensorGlucoseRequest: upsertSensorGlucoseRequest) { (response, error) in
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
 **upsertSensorGlucoseRequest** | [**UpsertSensorGlucoseRequest**](UpsertSensorGlucoseRequest.md) |  | 

### Return type

[**SensorGlucose**](SensorGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sensorGlucoseDelete**
```swift
    open class func sensorGlucoseDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4SensorGlucoseAPI.sensorGlucoseDelete(id: id) { (response, error) in
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

# **sensorGlucoseGetAll**
```swift
    open class func sensorGlucoseGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfSensorGlucose?, _ error: Error?) -> Void)
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

V4SensorGlucoseAPI.sensorGlucoseGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfSensorGlucose**](PaginatedResponseOfSensorGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sensorGlucoseGetById**
```swift
    open class func sensorGlucoseGetById(id: String, completion: @escaping (_ data: SensorGlucose?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4SensorGlucoseAPI.sensorGlucoseGetById(id: id) { (response, error) in
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

[**SensorGlucose**](SensorGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sensorGlucoseUpdate**
```swift
    open class func sensorGlucoseUpdate(id: String, upsertSensorGlucoseRequest: UpsertSensorGlucoseRequest, completion: @escaping (_ data: SensorGlucose?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertSensorGlucoseRequest = UpsertSensorGlucoseRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", mgdl: 123, direction: GlucoseDirection(), trendRate: 123, noise: 123) // UpsertSensorGlucoseRequest | 

V4SensorGlucoseAPI.sensorGlucoseUpdate(id: id, upsertSensorGlucoseRequest: upsertSensorGlucoseRequest) { (response, error) in
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
 **upsertSensorGlucoseRequest** | [**UpsertSensorGlucoseRequest**](UpsertSensorGlucoseRequest.md) |  | 

### Return type

[**SensorGlucose**](SensorGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

