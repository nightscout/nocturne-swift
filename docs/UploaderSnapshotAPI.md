# UploaderSnapshotAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**uploaderSnapshotGetAll**](UploaderSnapshotAPI.md#uploadersnapshotgetall) | **GET** /api/v4/device-status/uploader | Lists records with pagination, optional date range, device, and source filtering.
[**uploaderSnapshotGetById**](UploaderSnapshotAPI.md#uploadersnapshotgetbyid) | **GET** /api/v4/device-status/uploader/{id} | Retrieves a single record by its unique identifier.


# **uploaderSnapshotGetAll**
```swift
    open class func uploaderSnapshotGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfUploaderSnapshot?, _ error: Error?) -> Void)
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
UploaderSnapshotAPI.uploaderSnapshotGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfUploaderSnapshot**](PaginatedResponseOfUploaderSnapshot.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploaderSnapshotGetById**
```swift
    open class func uploaderSnapshotGetById(id: String, completion: @escaping (_ data: UploaderSnapshot?, _ error: Error?) -> Void)
```

Retrieves a single record by its unique identifier.

Returns `404 Not Found` if no record with the given id exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The unique identifier of the record.

// Retrieves a single record by its unique identifier.
UploaderSnapshotAPI.uploaderSnapshotGetById(id: id) { (response, error) in
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

[**UploaderSnapshot**](UploaderSnapshot.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

