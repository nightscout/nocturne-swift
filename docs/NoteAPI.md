# NoteAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**noteCreate**](NoteAPI.md#notecreate) | **POST** /api/v4/observations/notes | Creates a new record and returns it with a &#x60;Location&#x60; header pointing to the created resource.
[**noteDelete**](NoteAPI.md#notedelete) | **DELETE** /api/v4/observations/notes/{id} | Deletes a record by ID.
[**noteDeleteBySyncIdentifier**](NoteAPI.md#notedeletebysyncidentifier) | **DELETE** /api/v4/observations/notes/by-sync-id | Delete a note by its external sync identifier (dataSource + syncIdentifier pair).
[**noteGetAll**](NoteAPI.md#notegetall) | **GET** /api/v4/observations/notes | Lists records with pagination, optional date range, device, and source filtering.
[**noteGetById**](NoteAPI.md#notegetbyid) | **GET** /api/v4/observations/notes/{id} | Retrieves a single record by its unique identifier.
[**noteUpdate**](NoteAPI.md#noteupdate) | **PUT** /api/v4/observations/notes/{id} | Updates an existing record by ID and returns the updated record.


# **noteCreate**
```swift
    open class func noteCreate(upsertNoteRequest: UpsertNoteRequest, completion: @escaping (_ data: Note?, _ error: Error?) -> Void)
```

Creates a new record and returns it with a `Location` header pointing to the created resource.

`Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.              On success, responds with `201 Created` and a `Location` header containing the URL of the newly created record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertNoteRequest = UpsertNoteRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", text: "text_example", eventType: "eventType_example", isAnnouncement: false, syncIdentifier: "syncIdentifier_example") // UpsertNoteRequest | The data used to create the record.

// Creates a new record and returns it with a `Location` header pointing to the created resource.
NoteAPI.noteCreate(upsertNoteRequest: upsertNoteRequest) { (response, error) in
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
 **upsertNoteRequest** | [**UpsertNoteRequest**](UpsertNoteRequest.md) | The data used to create the record. | 

### Return type

[**Note**](Note.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **noteDelete**
```swift
    open class func noteDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Deletes a record by ID.

Returns `204 No Content` on success, or `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to delete.

// Deletes a record by ID.
NoteAPI.noteDelete(id: id) { (response, error) in
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

# **noteDeleteBySyncIdentifier**
```swift
    open class func noteDeleteBySyncIdentifier(dataSource: String? = nil, syncIdentifier: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a note by its external sync identifier (dataSource + syncIdentifier pair).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let dataSource = "dataSource_example" // String |  (optional)
let syncIdentifier = "syncIdentifier_example" // String |  (optional)

// Delete a note by its external sync identifier (dataSource + syncIdentifier pair).
NoteAPI.noteDeleteBySyncIdentifier(dataSource: dataSource, syncIdentifier: syncIdentifier) { (response, error) in
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

# **noteGetAll**
```swift
    open class func noteGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfNote?, _ error: Error?) -> Void)
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
NoteAPI.noteGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfNote**](PaginatedResponseOfNote.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **noteGetById**
```swift
    open class func noteGetById(id: String, completion: @escaping (_ data: Note?, _ error: Error?) -> Void)
```

Retrieves a single record by its unique identifier.

Returns `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record.

// Retrieves a single record by its unique identifier.
NoteAPI.noteGetById(id: id) { (response, error) in
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

[**Note**](Note.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **noteUpdate**
```swift
    open class func noteUpdate(id: String, upsertNoteRequest: UpsertNoteRequest, completion: @escaping (_ data: Note?, _ error: Error?) -> Void)
```

Updates an existing record by ID and returns the updated record.

Returns `404 Not Found` if no record with the given id exists.              `Timestamp` must be set on the mapped model; requests that resolve to a default timestamp are rejected with `400 Bad Request`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record to update.
let upsertNoteRequest = UpsertNoteRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", text: "text_example", eventType: "eventType_example", isAnnouncement: false, syncIdentifier: "syncIdentifier_example") // UpsertNoteRequest | The data to apply to the existing record.

// Updates an existing record by ID and returns the updated record.
NoteAPI.noteUpdate(id: id, upsertNoteRequest: upsertNoteRequest) { (response, error) in
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
 **upsertNoteRequest** | [**UpsertNoteRequest**](UpsertNoteRequest.md) | The data to apply to the existing record. | 

### Return type

[**Note**](Note.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

