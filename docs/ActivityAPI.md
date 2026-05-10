# ActivityAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activityCreateActivities**](ActivityAPI.md#activitycreateactivities) | **POST** /api/v4/Activity | Create one or more activity records
[**activityDeleteActivity**](ActivityAPI.md#activitydeleteactivity) | **DELETE** /api/v4/Activity/{id} | Delete an activity record by ID
[**activityGetActivities**](ActivityAPI.md#activitygetactivities) | **GET** /api/v4/Activity | Get activity records with pagination
[**activityGetActivity**](ActivityAPI.md#activitygetactivity) | **GET** /api/v4/Activity/{id} | Get a specific activity record by ID
[**activityUpdateActivity**](ActivityAPI.md#activityupdateactivity) | **PUT** /api/v4/Activity/{id} | Update an existing activity record


# **activityCreateActivities**
```swift
    open class func activityCreateActivities(upsertActivityRequest: [UpsertActivityRequest], completion: @escaping (_ data: [Activity]?, _ error: Error?) -> Void)
```

Create one or more activity records

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let upsertActivityRequest = [UpsertActivityRequest(mills: 123, utcOffset: 123, type: "type_example", description: "description_example", duration: 123, intensity: "intensity_example", notes: "notes_example", enteredBy: "enteredBy_example", distance: 123, distanceUnits: "distanceUnits_example", energy: 123, energyUnits: "energyUnits_example", name: "name_example")] // [UpsertActivityRequest] | 

// Create one or more activity records
ActivityAPI.activityCreateActivities(upsertActivityRequest: upsertActivityRequest) { (response, error) in
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
 **upsertActivityRequest** | [**[UpsertActivityRequest]**](UpsertActivityRequest.md) |  | 

### Return type

[**[Activity]**](Activity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **activityDeleteActivity**
```swift
    open class func activityDeleteActivity(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete an activity record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete an activity record by ID
ActivityAPI.activityDeleteActivity(id: id) { (response, error) in
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

# **activityGetActivities**
```swift
    open class func activityGetActivities(limit: Int? = nil, offset: Int? = nil, completion: @escaping (_ data: PaginatedResponseOfActivity?, _ error: Error?) -> Void)
```

Get activity records with pagination

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)

// Get activity records with pagination
ActivityAPI.activityGetActivities(limit: limit, offset: offset) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]

### Return type

[**PaginatedResponseOfActivity**](PaginatedResponseOfActivity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **activityGetActivity**
```swift
    open class func activityGetActivity(id: String, completion: @escaping (_ data: Activity?, _ error: Error?) -> Void)
```

Get a specific activity record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a specific activity record by ID
ActivityAPI.activityGetActivity(id: id) { (response, error) in
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

[**Activity**](Activity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **activityUpdateActivity**
```swift
    open class func activityUpdateActivity(id: String, upsertActivityRequest: UpsertActivityRequest, completion: @escaping (_ data: Activity?, _ error: Error?) -> Void)
```

Update an existing activity record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let upsertActivityRequest = UpsertActivityRequest(mills: 123, utcOffset: 123, type: "type_example", description: "description_example", duration: 123, intensity: "intensity_example", notes: "notes_example", enteredBy: "enteredBy_example", distance: 123, distanceUnits: "distanceUnits_example", energy: 123, energyUnits: "energyUnits_example", name: "name_example") // UpsertActivityRequest | 

// Update an existing activity record
ActivityAPI.activityUpdateActivity(id: id, upsertActivityRequest: upsertActivityRequest) { (response, error) in
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
 **upsertActivityRequest** | [**UpsertActivityRequest**](UpsertActivityRequest.md) |  | 

### Return type

[**Activity**](Activity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

