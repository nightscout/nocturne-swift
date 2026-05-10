# BolusAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bolusCreate**](BolusAPI.md#boluscreate) | **POST** /api/v4/insulin/boluses | Creates a new record and returns it with a &#x60;Location&#x60; header pointing to the created resource.
[**bolusDelete**](BolusAPI.md#bolusdelete) | **DELETE** /api/v4/insulin/boluses/{id} | Deletes a record by ID.
[**bolusDeleteBySyncIdentifier**](BolusAPI.md#bolusdeletebysyncidentifier) | **DELETE** /api/v4/insulin/boluses/by-sync-id | Delete a bolus by its external sync identifier (dataSource + syncIdentifier pair).
[**bolusGetAll**](BolusAPI.md#bolusgetall) | **GET** /api/v4/insulin/boluses | 
[**bolusGetById**](BolusAPI.md#bolusgetbyid) | **GET** /api/v4/insulin/boluses/{id} | Retrieves a single record by its unique identifier.
[**bolusUpdate**](BolusAPI.md#bolusupdate) | **PUT** /api/v4/insulin/boluses/{id} | Updates an existing record by ID and returns the updated record.


# **bolusCreate**
```swift
    open class func bolusCreate(createBolusRequest: CreateBolusRequest, completion: @escaping (_ data: Bolus?, _ error: Error?) -> Void)
```

Creates a new record and returns it with a `Location` header pointing to the created resource.

`Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.              On success, responds with `201 Created` and a `Location` header containing the URL of the newly created record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createBolusRequest = CreateBolusRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", insulin: 123, programmed: 123, delivered: 123, bolusType: BolusType(), kind: BolusKind(), automatic: false, duration: 123, syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", patientInsulinId: "patientInsulinId_example", unabsorbed: 123, bolusCalculationId: "bolusCalculationId_example", apsSnapshotId: "apsSnapshotId_example", correlationId: "correlationId_example") // CreateBolusRequest | The data used to create the record.

// Creates a new record and returns it with a `Location` header pointing to the created resource.
BolusAPI.bolusCreate(createBolusRequest: createBolusRequest) { (response, error) in
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
 **createBolusRequest** | [**CreateBolusRequest**](CreateBolusRequest.md) | The data used to create the record. | 

### Return type

[**Bolus**](Bolus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bolusDelete**
```swift
    open class func bolusDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Deletes a record by ID.

Returns `204 No Content` on success, or `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to delete.

// Deletes a record by ID.
BolusAPI.bolusDelete(id: id) { (response, error) in
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

# **bolusDeleteBySyncIdentifier**
```swift
    open class func bolusDeleteBySyncIdentifier(dataSource: String? = nil, syncIdentifier: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a bolus by its external sync identifier (dataSource + syncIdentifier pair).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let dataSource = "dataSource_example" // String |  (optional)
let syncIdentifier = "syncIdentifier_example" // String |  (optional)

// Delete a bolus by its external sync identifier (dataSource + syncIdentifier pair).
BolusAPI.bolusDeleteBySyncIdentifier(dataSource: dataSource, syncIdentifier: syncIdentifier) { (response, error) in
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
 **dataSource** | **String** |  | [optional] 
 **syncIdentifier** | **String** |  | [optional] 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bolusGetAll**
```swift
    open class func bolusGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfBolus?, _ error: Error?) -> Void)
```



Response is cached for 90 seconds, varying by all query parameters.

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

BolusAPI.bolusGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfBolus**](PaginatedResponseOfBolus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bolusGetById**
```swift
    open class func bolusGetById(id: String, completion: @escaping (_ data: Bolus?, _ error: Error?) -> Void)
```

Retrieves a single record by its unique identifier.

Returns `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record.

// Retrieves a single record by its unique identifier.
BolusAPI.bolusGetById(id: id) { (response, error) in
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

[**Bolus**](Bolus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bolusUpdate**
```swift
    open class func bolusUpdate(id: String, updateBolusRequest: UpdateBolusRequest, completion: @escaping (_ data: Bolus?, _ error: Error?) -> Void)
```

Updates an existing record by ID and returns the updated record.

Returns `404 Not Found` if no record with the given id exists.              `Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to update.
let updateBolusRequest = UpdateBolusRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", insulin: 123, programmed: 123, delivered: 123, automatic: false, duration: 123, syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", patientInsulinId: "patientInsulinId_example", unabsorbed: 123, bolusCalculationId: "bolusCalculationId_example", apsSnapshotId: "apsSnapshotId_example", correlationId: "correlationId_example") // UpdateBolusRequest | The data to apply to the existing record.

// Updates an existing record by ID and returns the updated record.
BolusAPI.bolusUpdate(id: id, updateBolusRequest: updateBolusRequest) { (response, error) in
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
 **updateBolusRequest** | [**UpdateBolusRequest**](UpdateBolusRequest.md) | The data to apply to the existing record. | 

### Return type

[**Bolus**](Bolus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

