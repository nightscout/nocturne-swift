# V4UploaderSnapshotsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**uploaderSnapshotGetAll**](V4UploaderSnapshotsAPI.md#uploadersnapshotgetall) | **GET** /api/v4/device-status/uploader | 
[**uploaderSnapshotGetById**](V4UploaderSnapshotsAPI.md#uploadersnapshotgetbyid) | **GET** /api/v4/device-status/uploader/{id} | 


# **uploaderSnapshotGetAll**
```swift
    open class func uploaderSnapshotGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfUploaderSnapshot?, _ error: Error?) -> Void)
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

V4UploaderSnapshotsAPI.uploaderSnapshotGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4UploaderSnapshotsAPI.uploaderSnapshotGetById(id: id) { (response, error) in
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

[**UploaderSnapshot**](UploaderSnapshot.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

