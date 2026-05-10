# V4HeartRateAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**heartRateCreateHeartRates**](V4HeartRateAPI.md#heartratecreateheartrates) | **POST** /api/v4/HeartRate | Create one or more heart rate records (single object or array)
[**heartRateDeleteHeartRate**](V4HeartRateAPI.md#heartratedeleteheartrate) | **DELETE** /api/v4/HeartRate/{id} | Delete a heart rate record by ID
[**heartRateGetHeartRate**](V4HeartRateAPI.md#heartrategetheartrate) | **GET** /api/v4/HeartRate/{id} | Get a specific heart rate record by ID
[**heartRateGetHeartRates**](V4HeartRateAPI.md#heartrategetheartrates) | **GET** /api/v4/HeartRate | Get heart rate records with optional pagination
[**heartRateUpdateHeartRate**](V4HeartRateAPI.md#heartrateupdateheartrate) | **PUT** /api/v4/HeartRate/{id} | Update an existing heart rate record


# **heartRateCreateHeartRates**
```swift
    open class func heartRateCreateHeartRates(body: JSONValue, completion: @escaping (_ data: [HeartRate]?, _ error: Error?) -> Void)
```

Create one or more heart rate records (single object or array)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let body =  // JSONValue | 

// Create one or more heart rate records (single object or array)
V4HeartRateAPI.heartRateCreateHeartRates(body: body) { (response, error) in
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
V4HeartRateAPI.heartRateDeleteHeartRate(id: id) { (response, error) in
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
V4HeartRateAPI.heartRateGetHeartRate(id: id) { (response, error) in
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
    open class func heartRateGetHeartRates(count: Int? = nil, skip: Int? = nil, completion: @escaping (_ data: [HeartRate]?, _ error: Error?) -> Void)
```

Get heart rate records with optional pagination

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let count = 987 // Int | Maximum number of records to return (default: 10) (optional) (default to 10)
let skip = 987 // Int | Number of records to skip for pagination (default: 0) (optional) (default to 0)

// Get heart rate records with optional pagination
V4HeartRateAPI.heartRateGetHeartRates(count: count, skip: skip) { (response, error) in
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

[**[HeartRate]**](HeartRate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **heartRateUpdateHeartRate**
```swift
    open class func heartRateUpdateHeartRate(id: String, heartRate: HeartRate, completion: @escaping (_ data: HeartRate?, _ error: Error?) -> Void)
```

Update an existing heart rate record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let heartRate = HeartRate(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, id: "id_example", createdAt: "createdAt_example", bpm: 123, accuracy: 123, device: "device_example", enteredBy: "enteredBy_example", dataSource: "dataSource_example") // HeartRate | 

// Update an existing heart rate record
V4HeartRateAPI.heartRateUpdateHeartRate(id: id, heartRate: heartRate) { (response, error) in
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
 **heartRate** | [**HeartRate**](HeartRate.md) |  | 

### Return type

[**HeartRate**](HeartRate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

