# StateSpansAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**stateSpansCreateStateSpan**](StateSpansAPI.md#statespanscreatestatespan) | **POST** /api/v4/state-spans | Create a new state span (manual entry)
[**stateSpansDeleteStateSpan**](StateSpansAPI.md#statespansdeletestatespan) | **DELETE** /api/v4/state-spans/{id} | Delete a state span
[**stateSpansGetActivities**](StateSpansAPI.md#statespansgetactivities) | **GET** /api/v4/state-spans/activities | Get all activity state spans (sleep, exercise, illness, travel)
[**stateSpansGetConnectivity**](StateSpansAPI.md#statespansgetconnectivity) | **GET** /api/v4/state-spans/connectivity | Get connectivity state spans
[**stateSpansGetExercise**](StateSpansAPI.md#statespansgetexercise) | **GET** /api/v4/state-spans/exercise | Get exercise state spans (user-annotated activity periods)
[**stateSpansGetIllness**](StateSpansAPI.md#statespansgetillness) | **GET** /api/v4/state-spans/illness | Get illness state spans (user-annotated illness periods)
[**stateSpansGetOverrides**](StateSpansAPI.md#statespansgetoverrides) | **GET** /api/v4/state-spans/overrides | Get override state spans
[**stateSpansGetProfiles**](StateSpansAPI.md#statespansgetprofiles) | **GET** /api/v4/state-spans/profiles | Get profile state spans
[**stateSpansGetPumpModes**](StateSpansAPI.md#statespansgetpumpmodes) | **GET** /api/v4/state-spans/pump-modes | Get pump mode state spans
[**stateSpansGetSleep**](StateSpansAPI.md#statespansgetsleep) | **GET** /api/v4/state-spans/sleep | Get sleep state spans (user-annotated sleep periods)
[**stateSpansGetStateSpan**](StateSpansAPI.md#statespansgetstatespan) | **GET** /api/v4/state-spans/{id} | Get a specific state span by ID
[**stateSpansGetStateSpans**](StateSpansAPI.md#statespansgetstatespans) | **GET** /api/v4/state-spans | Query all state spans with optional filtering
[**stateSpansGetTemporaryTargets**](StateSpansAPI.md#statespansgettemporarytargets) | **GET** /api/v4/state-spans/temporary-targets | Get temporary target state spans (AAPS temporary glucose targets)
[**stateSpansGetTravel**](StateSpansAPI.md#statespansgettravel) | **GET** /api/v4/state-spans/travel | Get travel state spans (user-annotated travel/timezone change periods)
[**stateSpansUpdateStateSpan**](StateSpansAPI.md#statespansupdatestatespan) | **PUT** /api/v4/state-spans/{id} | Update an existing state span


# **stateSpansCreateStateSpan**
```swift
    open class func stateSpansCreateStateSpan(createStateSpanRequest: CreateStateSpanRequest, completion: @escaping (_ data: StateSpan?, _ error: Error?) -> Void)
```

Create a new state span (manual entry)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createStateSpanRequest = CreateStateSpanRequest(category: StateSpanCategory(), state: "state_example", startMills: 123, endMills: 123, source: "source_example", metadata: "TODO", originalId: "originalId_example") // CreateStateSpanRequest | 

// Create a new state span (manual entry)
StateSpansAPI.stateSpansCreateStateSpan(createStateSpanRequest: createStateSpanRequest) { (response, error) in
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
 **createStateSpanRequest** | [**CreateStateSpanRequest**](CreateStateSpanRequest.md) |  | 

### Return type

[**StateSpan**](StateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansDeleteStateSpan**
```swift
    open class func stateSpansDeleteStateSpan(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a state span

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a state span
StateSpansAPI.stateSpansDeleteStateSpan(id: id) { (response, error) in
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetActivities**
```swift
    open class func stateSpansGetActivities(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get all activity state spans (sleep, exercise, illness, travel)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get all activity state spans (sleep, exercise, illness, travel)
StateSpansAPI.stateSpansGetActivities(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetConnectivity**
```swift
    open class func stateSpansGetConnectivity(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get connectivity state spans

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get connectivity state spans
StateSpansAPI.stateSpansGetConnectivity(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetExercise**
```swift
    open class func stateSpansGetExercise(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get exercise state spans (user-annotated activity periods)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get exercise state spans (user-annotated activity periods)
StateSpansAPI.stateSpansGetExercise(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetIllness**
```swift
    open class func stateSpansGetIllness(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get illness state spans (user-annotated illness periods)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get illness state spans (user-annotated illness periods)
StateSpansAPI.stateSpansGetIllness(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetOverrides**
```swift
    open class func stateSpansGetOverrides(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get override state spans

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get override state spans
StateSpansAPI.stateSpansGetOverrides(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetProfiles**
```swift
    open class func stateSpansGetProfiles(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get profile state spans

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get profile state spans
StateSpansAPI.stateSpansGetProfiles(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetPumpModes**
```swift
    open class func stateSpansGetPumpModes(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get pump mode state spans

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get pump mode state spans
StateSpansAPI.stateSpansGetPumpModes(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetSleep**
```swift
    open class func stateSpansGetSleep(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get sleep state spans (user-annotated sleep periods)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get sleep state spans (user-annotated sleep periods)
StateSpansAPI.stateSpansGetSleep(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetStateSpan**
```swift
    open class func stateSpansGetStateSpan(id: String, completion: @escaping (_ data: StateSpan?, _ error: Error?) -> Void)
```

Get a specific state span by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a specific state span by ID
StateSpansAPI.stateSpansGetStateSpan(id: id) { (response, error) in
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

[**StateSpan**](StateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetStateSpans**
```swift
    open class func stateSpansGetStateSpans(category: StateSpansGetStateSpansCategoryParameter? = nil, state: String? = nil, from: Date? = nil, to: Date? = nil, source: String? = nil, active: Bool? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Query all state spans with optional filtering

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let category = StateSpans_GetStateSpans_category_parameter() // StateSpansGetStateSpansCategoryParameter |  (optional)
let state = "state_example" // String |  (optional)
let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let source = "source_example" // String |  (optional)
let active = true // Bool |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Query all state spans with optional filtering
StateSpansAPI.stateSpansGetStateSpans(category: category, state: state, from: from, to: to, source: source, active: active, limit: limit, offset: offset, sort: sort) { (response, error) in
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
 **category** | [**StateSpansGetStateSpansCategoryParameter**](.md) |  | [optional] 
 **state** | **String** |  | [optional] 
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **source** | **String** |  | [optional] 
 **active** | **Bool** |  | [optional] 
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** |  | [optional] [default to &quot;timestamp_desc&quot;]

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetTemporaryTargets**
```swift
    open class func stateSpansGetTemporaryTargets(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get temporary target state spans (AAPS temporary glucose targets)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get temporary target state spans (AAPS temporary glucose targets)
StateSpansAPI.stateSpansGetTemporaryTargets(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansGetTravel**
```swift
    open class func stateSpansGetTravel(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, completion: @escaping (_ data: PaginatedResponseOfStateSpan?, _ error: Error?) -> Void)
```

Get travel state spans (user-annotated travel/timezone change periods)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")

// Get travel state spans (user-annotated travel/timezone change periods)
StateSpansAPI.stateSpansGetTravel(from: from, to: to, limit: limit, offset: offset, sort: sort) { (response, error) in
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

### Return type

[**PaginatedResponseOfStateSpan**](PaginatedResponseOfStateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stateSpansUpdateStateSpan**
```swift
    open class func stateSpansUpdateStateSpan(id: String, updateStateSpanRequest: UpdateStateSpanRequest, completion: @escaping (_ data: StateSpan?, _ error: Error?) -> Void)
```

Update an existing state span

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateStateSpanRequest = UpdateStateSpanRequest(category: StateSpanCategory(), state: "state_example", startMills: 123, endMills: 123, source: "source_example", metadata: "TODO") // UpdateStateSpanRequest | 

// Update an existing state span
StateSpansAPI.stateSpansUpdateStateSpan(id: id, updateStateSpanRequest: updateStateSpanRequest) { (response, error) in
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
 **updateStateSpanRequest** | [**UpdateStateSpanRequest**](UpdateStateSpanRequest.md) |  | 

### Return type

[**StateSpan**](StateSpan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

