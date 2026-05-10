# V4StepCountAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**stepCountCreateStepCounts**](V4StepCountAPI.md#stepcountcreatestepcounts) | **POST** /api/v4/StepCount | Create one or more step count records (single object or array)
[**stepCountDeleteStepCount**](V4StepCountAPI.md#stepcountdeletestepcount) | **DELETE** /api/v4/StepCount/{id} | Delete a step count record by ID
[**stepCountGetStepCount**](V4StepCountAPI.md#stepcountgetstepcount) | **GET** /api/v4/StepCount/{id} | Get a specific step count record by ID
[**stepCountGetStepCounts**](V4StepCountAPI.md#stepcountgetstepcounts) | **GET** /api/v4/StepCount | Get step count records with optional pagination
[**stepCountUpdateStepCount**](V4StepCountAPI.md#stepcountupdatestepcount) | **PUT** /api/v4/StepCount/{id} | Update an existing step count record


# **stepCountCreateStepCounts**
```swift
    open class func stepCountCreateStepCounts(body: JSONValue, completion: @escaping (_ data: [StepCount]?, _ error: Error?) -> Void)
```

Create one or more step count records (single object or array)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let body =  // JSONValue | 

// Create one or more step count records (single object or array)
V4StepCountAPI.stepCountCreateStepCounts(body: body) { (response, error) in
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
 **body** | **JSONValue** |  | 

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
V4StepCountAPI.stepCountDeleteStepCount(id: id) { (response, error) in
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
V4StepCountAPI.stepCountGetStepCount(id: id) { (response, error) in
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
    open class func stepCountGetStepCounts(count: Int? = nil, skip: Int? = nil, completion: @escaping (_ data: [StepCount]?, _ error: Error?) -> Void)
```

Get step count records with optional pagination

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let count = 987 // Int | Maximum number of records to return (default: 10) (optional) (default to 10)
let skip = 987 // Int | Number of records to skip for pagination (default: 0) (optional) (default to 0)

// Get step count records with optional pagination
V4StepCountAPI.stepCountGetStepCounts(count: count, skip: skip) { (response, error) in
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
 **count** | **Int** | Maximum number of records to return (default: 10) | [optional] [default to 10]
 **skip** | **Int** | Number of records to skip for pagination (default: 0) | [optional] [default to 0]

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
    open class func stepCountUpdateStepCount(id: String, stepCount: StepCount, completion: @escaping (_ data: StepCount?, _ error: Error?) -> Void)
```

Update an existing step count record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let stepCount = StepCount(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, id: "id_example", createdAt: "createdAt_example", metric: 123, source: 123, device: "device_example", enteredBy: "enteredBy_example", dataSource: "dataSource_example") // StepCount | 

// Update an existing step count record
V4StepCountAPI.stepCountUpdateStepCount(id: id, stepCount: stepCount) { (response, error) in
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
 **stepCount** | [**StepCount**](StepCount.md) |  | 

### Return type

[**StepCount**](StepCount.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

