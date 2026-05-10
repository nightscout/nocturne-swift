# DeviceEventAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deviceEventCreate**](DeviceEventAPI.md#deviceeventcreate) | **POST** /api/v4/observations/device-events | Creates a new record and returns it with a &#x60;Location&#x60; header pointing to the created resource.
[**deviceEventDelete**](DeviceEventAPI.md#deviceeventdelete) | **DELETE** /api/v4/observations/device-events/{id} | Deletes a record by ID.
[**deviceEventDeleteBySyncIdentifier**](DeviceEventAPI.md#deviceeventdeletebysyncidentifier) | **DELETE** /api/v4/observations/device-events/by-sync-id | Delete a device event by its external sync identifier (dataSource + syncIdentifier pair).
[**deviceEventGetAll**](DeviceEventAPI.md#deviceeventgetall) | **GET** /api/v4/observations/device-events | Lists records with pagination, optional date range, device, and source filtering.
[**deviceEventGetById**](DeviceEventAPI.md#deviceeventgetbyid) | **GET** /api/v4/observations/device-events/{id} | Retrieves a single record by its unique identifier.
[**deviceEventUpdate**](DeviceEventAPI.md#deviceeventupdate) | **PUT** /api/v4/observations/device-events/{id} | Updates an existing record by ID and returns the updated record.


# **deviceEventCreate**
```swift
    open class func deviceEventCreate(upsertDeviceEventRequest: UpsertDeviceEventRequest, completion: @escaping (_ data: DeviceEvent?, _ error: Error?) -> Void)
```

Creates a new record and returns it with a `Location` header pointing to the created resource.

`Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.              On success, responds with `201 Created` and a `Location` header containing the URL of the newly created record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertDeviceEventRequest = UpsertDeviceEventRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", eventType: DeviceEventType(), notes: "notes_example", syncIdentifier: "syncIdentifier_example") // UpsertDeviceEventRequest | The data used to create the record.

// Creates a new record and returns it with a `Location` header pointing to the created resource.
DeviceEventAPI.deviceEventCreate(upsertDeviceEventRequest: upsertDeviceEventRequest) { (response, error) in
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
 **upsertDeviceEventRequest** | [**UpsertDeviceEventRequest**](UpsertDeviceEventRequest.md) | The data used to create the record. | 

### Return type

[**DeviceEvent**](DeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceEventDelete**
```swift
    open class func deviceEventDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Deletes a record by ID.

Returns `204 No Content` on success, or `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to delete.

// Deletes a record by ID.
DeviceEventAPI.deviceEventDelete(id: id) { (response, error) in
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

# **deviceEventDeleteBySyncIdentifier**
```swift
    open class func deviceEventDeleteBySyncIdentifier(dataSource: String? = nil, syncIdentifier: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a device event by its external sync identifier (dataSource + syncIdentifier pair).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let dataSource = "dataSource_example" // String |  (optional)
let syncIdentifier = "syncIdentifier_example" // String |  (optional)

// Delete a device event by its external sync identifier (dataSource + syncIdentifier pair).
DeviceEventAPI.deviceEventDeleteBySyncIdentifier(dataSource: dataSource, syncIdentifier: syncIdentifier) { (response, error) in
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

# **deviceEventGetAll**
```swift
    open class func deviceEventGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfDeviceEvent?, _ error: Error?) -> Void)
```

Lists records with pagination, optional date range, device, and source filtering.

The `sort` parameter accepts exactly two values: - `timestamp_asc` — oldest records first - `timestamp_desc` — newest records first (default)              Use `limit` and `offset` together for paginated access to large result sets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date | Inclusive start of the date range filter. (optional)
let to = Date() // Date | Inclusive end of the date range filter. (optional)
let limit = 987 // Int | Maximum number of records to return. Defaults to `100`. (optional) (default to 100)
let offset = 987 // Int | Number of records to skip for pagination. Defaults to `0`. (optional) (default to 0)
let sort = "sort_example" // String | Sort order for results by timestamp. Defaults to `timestamp_desc`. (optional) (default to "timestamp_desc")
let device = "device_example" // String | Optional filter to restrict results to a specific device. (optional)
let source = "source_example" // String | Optional filter to restrict results to a specific data source. (optional)

// Lists records with pagination, optional date range, device, and source filtering.
DeviceEventAPI.deviceEventGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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
 **from** | **Date** | Inclusive start of the date range filter. | [optional] 
 **to** | **Date** | Inclusive end of the date range filter. | [optional] 
 **limit** | **Int** | Maximum number of records to return. Defaults to &#x60;100&#x60;. | [optional] [default to 100]
 **offset** | **Int** | Number of records to skip for pagination. Defaults to &#x60;0&#x60;. | [optional] [default to 0]
 **sort** | **String** | Sort order for results by timestamp. Defaults to &#x60;timestamp_desc&#x60;. | [optional] [default to &quot;timestamp_desc&quot;]
 **device** | **String** | Optional filter to restrict results to a specific device. | [optional] 
 **source** | **String** | Optional filter to restrict results to a specific data source. | [optional] 

### Return type

[**PaginatedResponseOfDeviceEvent**](PaginatedResponseOfDeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceEventGetById**
```swift
    open class func deviceEventGetById(id: String, completion: @escaping (_ data: DeviceEvent?, _ error: Error?) -> Void)
```

Retrieves a single record by its unique identifier.

Returns `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record.

// Retrieves a single record by its unique identifier.
DeviceEventAPI.deviceEventGetById(id: id) { (response, error) in
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

[**DeviceEvent**](DeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceEventUpdate**
```swift
    open class func deviceEventUpdate(id: String, upsertDeviceEventRequest: UpsertDeviceEventRequest, completion: @escaping (_ data: DeviceEvent?, _ error: Error?) -> Void)
```

Updates an existing record by ID and returns the updated record.

Returns `404 Not Found` if no record with the given id exists.              `Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to update.
let upsertDeviceEventRequest = UpsertDeviceEventRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", eventType: DeviceEventType(), notes: "notes_example", syncIdentifier: "syncIdentifier_example") // UpsertDeviceEventRequest | The data to apply to the existing record.

// Updates an existing record by ID and returns the updated record.
DeviceEventAPI.deviceEventUpdate(id: id, upsertDeviceEventRequest: upsertDeviceEventRequest) { (response, error) in
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
 **upsertDeviceEventRequest** | [**UpsertDeviceEventRequest**](UpsertDeviceEventRequest.md) | The data to apply to the existing record. | 

### Return type

[**DeviceEvent**](DeviceEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

