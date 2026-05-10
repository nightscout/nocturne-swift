# BodyWeightAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bodyWeightCreate**](BodyWeightAPI.md#bodyweightcreate) | **POST** /api/v4/body-weight | Create a single body weight record
[**bodyWeightCreateBodyWeights**](BodyWeightAPI.md#bodyweightcreatebodyweights) | **POST** /api/v4/body-weight/batch | Create one or more body weight records (single object or array)
[**bodyWeightDeleteBodyWeight**](BodyWeightAPI.md#bodyweightdeletebodyweight) | **DELETE** /api/v4/body-weight/{id} | Delete a body weight record by ID
[**bodyWeightGetBodyWeight**](BodyWeightAPI.md#bodyweightgetbodyweight) | **GET** /api/v4/body-weight/{id} | Get a specific body weight record by ID
[**bodyWeightGetBodyWeights**](BodyWeightAPI.md#bodyweightgetbodyweights) | **GET** /api/v4/body-weight | Get body weight records with optional pagination
[**bodyWeightUpdateBodyWeight**](BodyWeightAPI.md#bodyweightupdatebodyweight) | **PUT** /api/v4/body-weight/{id} | Update an existing body weight record


# **bodyWeightCreate**
```swift
    open class func bodyWeightCreate(bodyWeight: BodyWeight, completion: @escaping (_ data: BodyWeight?, _ error: Error?) -> Void)
```

Create a single body weight record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let bodyWeight = BodyWeight(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, weightKg: 123, bodyFatPercent: 123, leanMassKg: 123, device: "device_example", enteredBy: "enteredBy_example", dataSource: "dataSource_example") // BodyWeight | 

// Create a single body weight record
BodyWeightAPI.bodyWeightCreate(bodyWeight: bodyWeight) { (response, error) in
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
 **bodyWeight** | [**BodyWeight**](BodyWeight.md) |  | 

### Return type

[**BodyWeight**](BodyWeight.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bodyWeightCreateBodyWeights**
```swift
    open class func bodyWeightCreateBodyWeights(body: JSONValue, completion: @escaping (_ data: [BodyWeight]?, _ error: Error?) -> Void)
```

Create one or more body weight records (single object or array)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let body =  // JSONValue | 

// Create one or more body weight records (single object or array)
BodyWeightAPI.bodyWeightCreateBodyWeights(body: body) { (response, error) in
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

[**[BodyWeight]**](BodyWeight.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bodyWeightDeleteBodyWeight**
```swift
    open class func bodyWeightDeleteBodyWeight(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a body weight record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a body weight record by ID
BodyWeightAPI.bodyWeightDeleteBodyWeight(id: id) { (response, error) in
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

# **bodyWeightGetBodyWeight**
```swift
    open class func bodyWeightGetBodyWeight(id: String, completion: @escaping (_ data: BodyWeight?, _ error: Error?) -> Void)
```

Get a specific body weight record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Record ID

// Get a specific body weight record by ID
BodyWeightAPI.bodyWeightGetBodyWeight(id: id) { (response, error) in
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

[**BodyWeight**](BodyWeight.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bodyWeightGetBodyWeights**
```swift
    open class func bodyWeightGetBodyWeights(count: Int? = nil, skip: Int? = nil, completion: @escaping (_ data: [BodyWeight]?, _ error: Error?) -> Void)
```

Get body weight records with optional pagination

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let count = 987 // Int | Maximum number of records to return (default: 10) (optional) (default to 10)
let skip = 987 // Int | Number of records to skip for pagination (default: 0) (optional) (default to 0)

// Get body weight records with optional pagination
BodyWeightAPI.bodyWeightGetBodyWeights(count: count, skip: skip) { (response, error) in
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

[**[BodyWeight]**](BodyWeight.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bodyWeightUpdateBodyWeight**
```swift
    open class func bodyWeightUpdateBodyWeight(id: String, bodyWeight: BodyWeight, completion: @escaping (_ data: BodyWeight?, _ error: Error?) -> Void)
```

Update an existing body weight record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let bodyWeight = BodyWeight(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, weightKg: 123, bodyFatPercent: 123, leanMassKg: 123, device: "device_example", enteredBy: "enteredBy_example", dataSource: "dataSource_example") // BodyWeight | 

// Update an existing body weight record
BodyWeightAPI.bodyWeightUpdateBodyWeight(id: id, bodyWeight: bodyWeight) { (response, error) in
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
 **bodyWeight** | [**BodyWeight**](BodyWeight.md) |  | 

### Return type

[**BodyWeight**](BodyWeight.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

