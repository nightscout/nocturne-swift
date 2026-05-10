# V4BolusesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bolusCreate**](V4BolusesAPI.md#boluscreate) | **POST** /api/v4/insulin/boluses | 
[**bolusDelete**](V4BolusesAPI.md#bolusdelete) | **DELETE** /api/v4/insulin/boluses/{id} | 
[**bolusGetAll**](V4BolusesAPI.md#bolusgetall) | **GET** /api/v4/insulin/boluses | 
[**bolusGetById**](V4BolusesAPI.md#bolusgetbyid) | **GET** /api/v4/insulin/boluses/{id} | 
[**bolusUpdate**](V4BolusesAPI.md#bolusupdate) | **PUT** /api/v4/insulin/boluses/{id} | 


# **bolusCreate**
```swift
    open class func bolusCreate(createBolusRequest: CreateBolusRequest, completion: @escaping (_ data: Bolus?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createBolusRequest = CreateBolusRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", insulin: 123, programmed: 123, delivered: 123, bolusType: BolusType(), kind: BolusKind(), automatic: false, duration: 123, syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", unabsorbed: 123, bolusCalculationId: "bolusCalculationId_example", apsSnapshotId: "apsSnapshotId_example") // CreateBolusRequest | 

V4BolusesAPI.bolusCreate(createBolusRequest: createBolusRequest) { (response, error) in
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
 **createBolusRequest** | [**CreateBolusRequest**](CreateBolusRequest.md) |  | 

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4BolusesAPI.bolusDelete(id: id) { (response, error) in
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

# **bolusGetAll**
```swift
    open class func bolusGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfBolus?, _ error: Error?) -> Void)
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

V4BolusesAPI.bolusGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4BolusesAPI.bolusGetById(id: id) { (response, error) in
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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateBolusRequest = UpdateBolusRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", insulin: 123, programmed: 123, delivered: 123, automatic: false, duration: 123, syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", unabsorbed: 123, bolusCalculationId: "bolusCalculationId_example", apsSnapshotId: "apsSnapshotId_example") // UpdateBolusRequest | 

V4BolusesAPI.bolusUpdate(id: id, updateBolusRequest: updateBolusRequest) { (response, error) in
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
 **updateBolusRequest** | [**UpdateBolusRequest**](UpdateBolusRequest.md) |  | 

### Return type

[**Bolus**](Bolus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

