# CalibrationAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**calibrationCreate**](CalibrationAPI.md#calibrationcreate) | **POST** /api/v4/glucose/calibrations | Creates a new record and returns it with a &#x60;Location&#x60; header pointing to the created resource.
[**calibrationDelete**](CalibrationAPI.md#calibrationdelete) | **DELETE** /api/v4/glucose/calibrations/{id} | Deletes a record by ID.
[**calibrationGetAll**](CalibrationAPI.md#calibrationgetall) | **GET** /api/v4/glucose/calibrations | 
[**calibrationGetById**](CalibrationAPI.md#calibrationgetbyid) | **GET** /api/v4/glucose/calibrations/{id} | Retrieves a single record by its unique identifier.
[**calibrationUpdate**](CalibrationAPI.md#calibrationupdate) | **PUT** /api/v4/glucose/calibrations/{id} | Updates an existing record by ID and returns the updated record.


# **calibrationCreate**
```swift
    open class func calibrationCreate(upsertCalibrationRequest: UpsertCalibrationRequest, completion: @escaping (_ data: Calibration?, _ error: Error?) -> Void)
```

Creates a new record and returns it with a `Location` header pointing to the created resource.

`Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.              On success, responds with `201 Created` and a `Location` header containing the URL of the newly created record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertCalibrationRequest = UpsertCalibrationRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", slope: 123, intercept: 123, scale: 123) // UpsertCalibrationRequest | The data used to create the record.

// Creates a new record and returns it with a `Location` header pointing to the created resource.
CalibrationAPI.calibrationCreate(upsertCalibrationRequest: upsertCalibrationRequest) { (response, error) in
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
 **upsertCalibrationRequest** | [**UpsertCalibrationRequest**](UpsertCalibrationRequest.md) | The data used to create the record. | 

### Return type

[**Calibration**](Calibration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **calibrationDelete**
```swift
    open class func calibrationDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Deletes a record by ID.

Returns `204 No Content` on success, or `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to delete.

// Deletes a record by ID.
CalibrationAPI.calibrationDelete(id: id) { (response, error) in
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

# **calibrationGetAll**
```swift
    open class func calibrationGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfCalibration?, _ error: Error?) -> Void)
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

CalibrationAPI.calibrationGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfCalibration**](PaginatedResponseOfCalibration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **calibrationGetById**
```swift
    open class func calibrationGetById(id: String, completion: @escaping (_ data: Calibration?, _ error: Error?) -> Void)
```

Retrieves a single record by its unique identifier.

Returns `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record.

// Retrieves a single record by its unique identifier.
CalibrationAPI.calibrationGetById(id: id) { (response, error) in
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

[**Calibration**](Calibration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **calibrationUpdate**
```swift
    open class func calibrationUpdate(id: String, upsertCalibrationRequest: UpsertCalibrationRequest, completion: @escaping (_ data: Calibration?, _ error: Error?) -> Void)
```

Updates an existing record by ID and returns the updated record.

Returns `404 Not Found` if no record with the given id exists.              `Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to update.
let upsertCalibrationRequest = UpsertCalibrationRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", slope: 123, intercept: 123, scale: 123) // UpsertCalibrationRequest | The data to apply to the existing record.

// Updates an existing record by ID and returns the updated record.
CalibrationAPI.calibrationUpdate(id: id, upsertCalibrationRequest: upsertCalibrationRequest) { (response, error) in
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
 **upsertCalibrationRequest** | [**UpsertCalibrationRequest**](UpsertCalibrationRequest.md) | The data to apply to the existing record. | 

### Return type

[**Calibration**](Calibration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

