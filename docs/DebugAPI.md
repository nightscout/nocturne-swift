# DebugAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**debugEchoQuery**](DebugAPI.md#debugechoquery) | **GET** /api/v4/debug/echo/{echo} | Echo endpoint for debugging MongoDB queries Returns information about how REST API parameters translate into MongoDB queries
[**debugEchoQueryWithModel**](DebugAPI.md#debugechoquerywithmodel) | **GET** /api/v4/debug/echo/{echo}/{model} | Echo endpoint for debugging MongoDB queries with model Returns information about how REST API parameters translate into MongoDB queries
[**debugEchoQueryWithModelAndSpec**](DebugAPI.md#debugechoquerywithmodelandspec) | **GET** /api/v4/debug/echo/{echo}/{model}/{spec} | Echo endpoint for debugging MongoDB queries with model and spec Returns information about how REST API parameters translate into MongoDB queries
[**debugPreviewEntries**](DebugAPI.md#debugpreviewentries) | **POST** /api/v4/debug/entries/preview | Preview endpoint for entry creation without persistence Allows previewing entry data without actually storing it in the database


# **debugEchoQuery**
```swift
    open class func debugEchoQuery(echo: String, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Echo endpoint for debugging MongoDB queries Returns information about how REST API parameters translate into MongoDB queries

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let echo = "echo_example" // String | Storage type to query (entries, treatments, devicestatus, activity)

// Echo endpoint for debugging MongoDB queries Returns information about how REST API parameters translate into MongoDB queries
DebugAPI.debugEchoQuery(echo: echo) { (response, error) in
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
 **echo** | **String** | Storage type to query (entries, treatments, devicestatus, activity) | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugEchoQueryWithModel**
```swift
    open class func debugEchoQueryWithModel(echo: String, model: String, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Echo endpoint for debugging MongoDB queries with model Returns information about how REST API parameters translate into MongoDB queries

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let echo = "echo_example" // String | Storage type to query (entries, treatments, devicestatus, activity)
let model = "model_example" // String | Model specification

// Echo endpoint for debugging MongoDB queries with model Returns information about how REST API parameters translate into MongoDB queries
DebugAPI.debugEchoQueryWithModel(echo: echo, model: model) { (response, error) in
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
 **echo** | **String** | Storage type to query (entries, treatments, devicestatus, activity) | 
 **model** | **String** | Model specification | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugEchoQueryWithModelAndSpec**
```swift
    open class func debugEchoQueryWithModelAndSpec(echo: String, model: String, spec: String, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Echo endpoint for debugging MongoDB queries with model and spec Returns information about how REST API parameters translate into MongoDB queries

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let echo = "echo_example" // String | Storage type to query (entries, treatments, devicestatus, activity)
let model = "model_example" // String | Model specification
let spec = "spec_example" // String | Specification parameter

// Echo endpoint for debugging MongoDB queries with model and spec Returns information about how REST API parameters translate into MongoDB queries
DebugAPI.debugEchoQueryWithModelAndSpec(echo: echo, model: model, spec: spec) { (response, error) in
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
 **echo** | **String** | Storage type to query (entries, treatments, devicestatus, activity) | 
 **model** | **String** | Model specification | 
 **spec** | **String** | Specification parameter | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **debugPreviewEntries**
```swift
    open class func debugPreviewEntries(body: JSONValue, completion: @escaping (_ data: JSONValue?, _ error: Error?) -> Void)
```

Preview endpoint for entry creation without persistence Allows previewing entry data without actually storing it in the database

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let body =  // JSONValue | Entry data to preview (single object or array)

// Preview endpoint for entry creation without persistence Allows previewing entry data without actually storing it in the database
DebugAPI.debugPreviewEntries(body: body) { (response, error) in
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
 **body** | **JSONValue** | Entry data to preview (single object or array) | 

### Return type

**JSONValue**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

