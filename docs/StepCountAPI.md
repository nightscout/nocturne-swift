# StepCountAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**stepCountCreateStepCounts**](StepCountAPI.md#stepcountcreatestepcounts) | **POST** /api/v4/StepCount | Create one or more step count records
[**stepCountDeleteStepCount**](StepCountAPI.md#stepcountdeletestepcount) | **DELETE** /api/v4/StepCount/{id} | Delete a step count record by ID
[**stepCountGetStepCount**](StepCountAPI.md#stepcountgetstepcount) | **GET** /api/v4/StepCount/{id} | Get a specific step count record by ID
[**stepCountGetStepCounts**](StepCountAPI.md#stepcountgetstepcounts) | **GET** /api/v4/StepCount | Get step count records with optional pagination and date filtering
[**stepCountUpdateStepCount**](StepCountAPI.md#stepcountupdatestepcount) | **PUT** /api/v4/StepCount/{id} | Update an existing step count record


# **stepCountCreateStepCounts**
```swift
    open class func stepCountCreateStepCounts(upsertStepCountRequest: [UpsertStepCountRequest], completion: @escaping (_ data: [StepCount]?, _ error: Error?) -> Void)
```

Create one or more step count records

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertStepCountRequest = [UpsertStepCountRequest(timestamp: Date(), utcOffset: 123, metric: 123, source: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example")] // [UpsertStepCountRequest] | 

// Create one or more step count records
StepCountAPI.stepCountCreateStepCounts(upsertStepCountRequest: upsertStepCountRequest) { (response, error) in
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
 **upsertStepCountRequest** | [**[UpsertStepCountRequest]**](UpsertStepCountRequest.md) |  | 

### Return type

[**[StepCount]**](StepCount.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stepCountDeleteStepCount**
```swift
    open class func stepCountDeleteStepCount(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a step count record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a step count record by ID
StepCountAPI.stepCountDeleteStepCount(id: id) { (response, error) in
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

# **stepCountGetStepCount**
```swift
    open class func stepCountGetStepCount(id: String, completion: @escaping (_ data: StepCount?, _ error: Error?) -> Void)
```

Get a specific step count record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Record ID

// Get a specific step count record by ID
StepCountAPI.stepCountGetStepCount(id: id) { (response, error) in
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

[**StepCount**](StepCount.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stepCountGetStepCounts**
```swift
    open class func stepCountGetStepCounts(count: Int? = nil, skip: Int? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [StepCount]?, _ error: Error?) -> Void)
```

Get step count records with optional pagination and date filtering

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let count = 987 // Int | Maximum number of records to return (default: 10, ignored when from/to are specified) (optional) (default to 10)
let skip = 987 // Int | Number of records to skip for pagination (default: 0, ignored when from/to are specified) (optional) (default to 0)
let from = Date() // Date | Start of date range (inclusive). When specified with 'to', returns all records in range. (optional)
let to = Date() // Date | End of date range (exclusive). When specified with 'from', returns all records in range. (optional)

// Get step count records with optional pagination and date filtering
StepCountAPI.stepCountGetStepCounts(count: count, skip: skip, from: from, to: to) { (response, error) in
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

[**[StepCount]**](StepCount.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stepCountUpdateStepCount**
```swift
    open class func stepCountUpdateStepCount(id: String, upsertStepCountRequest: UpsertStepCountRequest, completion: @escaping (_ data: StepCount?, _ error: Error?) -> Void)
```

Update an existing step count record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertStepCountRequest = UpsertStepCountRequest(timestamp: Date(), utcOffset: 123, metric: 123, source: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example") // UpsertStepCountRequest | 

// Update an existing step count record
StepCountAPI.stepCountUpdateStepCount(id: id, upsertStepCountRequest: upsertStepCountRequest) { (response, error) in
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
 **upsertStepCountRequest** | [**UpsertStepCountRequest**](UpsertStepCountRequest.md) |  | 

### Return type

[**StepCount**](StepCount.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

