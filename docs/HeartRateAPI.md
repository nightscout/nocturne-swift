# HeartRateAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**heartRateCreateHeartRates**](HeartRateAPI.md#heartratecreateheartrates) | **POST** /api/v4/HeartRate | Create one or more heart rate records
[**heartRateDeleteHeartRate**](HeartRateAPI.md#heartratedeleteheartrate) | **DELETE** /api/v4/HeartRate/{id} | Delete a heart rate record by ID
[**heartRateGetHeartRate**](HeartRateAPI.md#heartrategetheartrate) | **GET** /api/v4/HeartRate/{id} | Get a specific heart rate record by ID
[**heartRateGetHeartRates**](HeartRateAPI.md#heartrategetheartrates) | **GET** /api/v4/HeartRate | Get heart rate records with optional pagination and date filtering
[**heartRateUpdateHeartRate**](HeartRateAPI.md#heartrateupdateheartrate) | **PUT** /api/v4/HeartRate/{id} | Update an existing heart rate record


# **heartRateCreateHeartRates**
```swift
    open class func heartRateCreateHeartRates(upsertHeartRateRequest: [UpsertHeartRateRequest], completion: @escaping (_ data: [HeartRate]?, _ error: Error?) -> Void)
```

Create one or more heart rate records

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertHeartRateRequest = [UpsertHeartRateRequest(timestamp: Date(), utcOffset: 123, bpm: 123, accuracy: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example")] // [UpsertHeartRateRequest] | 

// Create one or more heart rate records
HeartRateAPI.heartRateCreateHeartRates(upsertHeartRateRequest: upsertHeartRateRequest) { (response, error) in
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
 **upsertHeartRateRequest** | [**[UpsertHeartRateRequest]**](UpsertHeartRateRequest.md) |  | 

### Return type

[**[HeartRate]**](HeartRate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **heartRateDeleteHeartRate**
```swift
    open class func heartRateDeleteHeartRate(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a heart rate record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a heart rate record by ID
HeartRateAPI.heartRateDeleteHeartRate(id: id) { (response, error) in
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

# **heartRateGetHeartRate**
```swift
    open class func heartRateGetHeartRate(id: String, completion: @escaping (_ data: HeartRate?, _ error: Error?) -> Void)
```

Get a specific heart rate record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Record ID

// Get a specific heart rate record by ID
HeartRateAPI.heartRateGetHeartRate(id: id) { (response, error) in
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
 **id** | **String** | Record ID | 

### Return type

[**HeartRate**](HeartRate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **heartRateGetHeartRates**
```swift
    open class func heartRateGetHeartRates(count: Int? = nil, skip: Int? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [HeartRate]?, _ error: Error?) -> Void)
```

Get heart rate records with optional pagination and date filtering

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let count = 987 // Int | Maximum number of records to return (default: 10, ignored when from/to are specified) (optional) (default to 10)
let skip = 987 // Int | Number of records to skip for pagination (default: 0, ignored when from/to are specified) (optional) (default to 0)
let from = Date() // Date | Start of date range (inclusive). When specified with 'to', returns all records in range. (optional)
let to = Date() // Date | End of date range (exclusive). When specified with 'from', returns all records in range. (optional)

// Get heart rate records with optional pagination and date filtering
HeartRateAPI.heartRateGetHeartRates(count: count, skip: skip, from: from, to: to) { (response, error) in
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
 **count** | **Int** | Maximum number of records to return (default: 10, ignored when from/to are specified) | [optional] [default to 10]
 **skip** | **Int** | Number of records to skip for pagination (default: 0, ignored when from/to are specified) | [optional] [default to 0]
 **from** | **Date** | Start of date range (inclusive). When specified with &#39;to&#39;, returns all records in range. | [optional] 
 **to** | **Date** | End of date range (exclusive). When specified with &#39;from&#39;, returns all records in range. | [optional] 

### Return type

[**[HeartRate]**](HeartRate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **heartRateUpdateHeartRate**
```swift
    open class func heartRateUpdateHeartRate(id: String, upsertHeartRateRequest: UpsertHeartRateRequest, completion: @escaping (_ data: HeartRate?, _ error: Error?) -> Void)
```

Update an existing heart rate record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertHeartRateRequest = UpsertHeartRateRequest(timestamp: Date(), utcOffset: 123, bpm: 123, accuracy: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example") // UpsertHeartRateRequest | 

// Update an existing heart rate record
HeartRateAPI.heartRateUpdateHeartRate(id: id, upsertHeartRateRequest: upsertHeartRateRequest) { (response, error) in
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
 **upsertHeartRateRequest** | [**UpsertHeartRateRequest**](UpsertHeartRateRequest.md) |  | 

### Return type

[**HeartRate**](HeartRate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

