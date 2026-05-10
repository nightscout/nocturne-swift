# V4BolusCalculationsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bolusCalculationCreate**](V4BolusCalculationsAPI.md#boluscalculationcreate) | **POST** /api/v4/insulin/calculations | 
[**bolusCalculationDelete**](V4BolusCalculationsAPI.md#boluscalculationdelete) | **DELETE** /api/v4/insulin/calculations/{id} | 
[**bolusCalculationGetAll**](V4BolusCalculationsAPI.md#boluscalculationgetall) | **GET** /api/v4/insulin/calculations | 
[**bolusCalculationGetById**](V4BolusCalculationsAPI.md#boluscalculationgetbyid) | **GET** /api/v4/insulin/calculations/{id} | 
[**bolusCalculationUpdate**](V4BolusCalculationsAPI.md#boluscalculationupdate) | **PUT** /api/v4/insulin/calculations/{id} | 


# **bolusCalculationCreate**
```swift
    open class func bolusCalculationCreate(upsertBolusCalculationRequest: UpsertBolusCalculationRequest, completion: @escaping (_ data: BolusCalculation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertBolusCalculationRequest = UpsertBolusCalculationRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", carbInput: 123, insulinOnBoard: 123, insulinRecommendation: 123, carbRatio: 123, calculationType: CalculationType(), insulinRecommendationForCarbs: 123, insulinProgrammed: 123, enteredInsulin: 123, splitNow: 123, splitExt: 123, preBolus: 123) // UpsertBolusCalculationRequest | 

V4BolusCalculationsAPI.bolusCalculationCreate(upsertBolusCalculationRequest: upsertBolusCalculationRequest) { (response, error) in
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
 **upsertBolusCalculationRequest** | [**UpsertBolusCalculationRequest**](UpsertBolusCalculationRequest.md) |  | 

### Return type

[**BolusCalculation**](BolusCalculation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bolusCalculationDelete**
```swift
    open class func bolusCalculationDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4BolusCalculationsAPI.bolusCalculationDelete(id: id) { (response, error) in
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

# **bolusCalculationGetAll**
```swift
    open class func bolusCalculationGetAll(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfBolusCalculation?, _ error: Error?) -> Void)
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

V4BolusCalculationsAPI.bolusCalculationGetAll(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfBolusCalculation**](PaginatedResponseOfBolusCalculation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bolusCalculationGetById**
```swift
    open class func bolusCalculationGetById(id: String, completion: @escaping (_ data: BolusCalculation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

V4BolusCalculationsAPI.bolusCalculationGetById(id: id) { (response, error) in
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

[**BolusCalculation**](BolusCalculation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bolusCalculationUpdate**
```swift
    open class func bolusCalculationUpdate(id: String, upsertBolusCalculationRequest: UpsertBolusCalculationRequest, completion: @escaping (_ data: BolusCalculation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertBolusCalculationRequest = UpsertBolusCalculationRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", carbInput: 123, insulinOnBoard: 123, insulinRecommendation: 123, carbRatio: 123, calculationType: CalculationType(), insulinRecommendationForCarbs: 123, insulinProgrammed: 123, enteredInsulin: 123, splitNow: 123, splitExt: 123, preBolus: 123) // UpsertBolusCalculationRequest | 

V4BolusCalculationsAPI.bolusCalculationUpdate(id: id, upsertBolusCalculationRequest: upsertBolusCalculationRequest) { (response, error) in
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
 **upsertBolusCalculationRequest** | [**UpsertBolusCalculationRequest**](UpsertBolusCalculationRequest.md) |  | 

### Return type

[**BolusCalculation**](BolusCalculation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

