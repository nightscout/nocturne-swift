# MeterGlucoseAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**meterGlucoseCreate**](MeterGlucoseAPI.md#meterglucosecreate) | **POST** /api/v4/glucose/meter | Creates a new record and returns it with a &#x60;Location&#x60; header pointing to the created resource.
[**meterGlucoseDelete**](MeterGlucoseAPI.md#meterglucosedelete) | **DELETE** /api/v4/glucose/meter/{id} | Deletes a record by ID.
[**meterGlucoseGetAll**](MeterGlucoseAPI.md#meterglucosegetall) | **GET** /api/v4/glucose/meter | 
[**meterGlucoseGetById**](MeterGlucoseAPI.md#meterglucosegetbyid) | **GET** /api/v4/glucose/meter/{id} | Retrieves a single record by its unique identifier.
[**meterGlucoseUpdate**](MeterGlucoseAPI.md#meterglucoseupdate) | **PUT** /api/v4/glucose/meter/{id} | Updates an existing record by ID and returns the updated record.


# **meterGlucoseCreate**
```swift
    open class func meterGlucoseCreate(upsertMeterGlucoseRequest: UpsertMeterGlucoseRequest, completion: @escaping (_ data: MeterGlucose?, _ error: Error?) -> Void)
```

Creates a new record and returns it with a `Location` header pointing to the created resource.

`Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.              On success, responds with `201 Created` and a `Location` header containing the URL of the newly created record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertMeterGlucoseRequest = UpsertMeterGlucoseRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", mgdl: 123) // UpsertMeterGlucoseRequest | The data used to create the record.

// Creates a new record and returns it with a `Location` header pointing to the created resource.
MeterGlucoseAPI.meterGlucoseCreate(upsertMeterGlucoseRequest: upsertMeterGlucoseRequest) { (response, error) in
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
 **upsertMeterGlucoseRequest** | [**UpsertMeterGlucoseRequest**](UpsertMeterGlucoseRequest.md) | The data used to create the record. | 

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

Deletes a record by ID.

Returns `204 No Content` on success, or `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to delete.

// Deletes a record by ID.
MeterGlucoseAPI.meterGlucoseDelete(id: id) { (response, error) in
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
 **id** | **String** | The unique identifier of the record to delete. | 

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



Response is cached for 120 seconds, varied by all query parameters.

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

MeterGlucoseAPI.meterGlucoseGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

Retrieves a single record by its unique identifier.

Returns `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record.

// Retrieves a single record by its unique identifier.
MeterGlucoseAPI.meterGlucoseGetById(id: id) { (response, error) in
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
 **id** | **String** | The unique identifier of the record. | 

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

Updates an existing record by ID and returns the updated record.

Returns `404 Not Found` if no record with the given id exists.              `Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to update.
let upsertMeterGlucoseRequest = UpsertMeterGlucoseRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", mgdl: 123) // UpsertMeterGlucoseRequest | The data to apply to the existing record.

// Updates an existing record by ID and returns the updated record.
MeterGlucoseAPI.meterGlucoseUpdate(id: id, upsertMeterGlucoseRequest: upsertMeterGlucoseRequest) { (response, error) in
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
 **id** | **String** | The unique identifier of the record to update. | 
 **upsertMeterGlucoseRequest** | [**UpsertMeterGlucoseRequest**](UpsertMeterGlucoseRequest.md) | The data to apply to the existing record. | 

### Return type

[**MeterGlucose**](MeterGlucose.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

