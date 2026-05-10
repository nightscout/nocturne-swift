# MealMatchingAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**mealMatchingAcceptMatch**](MealMatchingAPI.md#mealmatchingacceptmatch) | **POST** /api/v4/meal-matching/accept | Accept a meal match
[**mealMatchingDismissMatch**](MealMatchingAPI.md#mealmatchingdismissmatch) | **POST** /api/v4/meal-matching/dismiss | Dismiss a meal match
[**mealMatchingGetFoodEntry**](MealMatchingAPI.md#mealmatchinggetfoodentry) | **GET** /api/v4/meal-matching/food-entries/{id} | Get a food entry for review
[**mealMatchingGetSuggestions**](MealMatchingAPI.md#mealmatchinggetsuggestions) | **GET** /api/v4/meal-matching/suggestions | Get suggested meal matches for a date range


# **mealMatchingAcceptMatch**
```swift
    open class func mealMatchingAcceptMatch(acceptMatchRequest: AcceptMatchRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Accept a meal match

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let acceptMatchRequest = AcceptMatchRequest(foodEntryId: "foodEntryId_example", treatmentId: "treatmentId_example", carbs: 123, timeOffsetMinutes: 123) // AcceptMatchRequest | 

// Accept a meal match
MealMatchingAPI.mealMatchingAcceptMatch(acceptMatchRequest: acceptMatchRequest) { (response, error) in
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
 **acceptMatchRequest** | [**AcceptMatchRequest**](AcceptMatchRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mealMatchingDismissMatch**
```swift
    open class func mealMatchingDismissMatch(dismissMatchRequest: DismissMatchRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Dismiss a meal match

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let dismissMatchRequest = DismissMatchRequest(foodEntryId: "foodEntryId_example") // DismissMatchRequest | 

// Dismiss a meal match
MealMatchingAPI.mealMatchingDismissMatch(dismissMatchRequest: dismissMatchRequest) { (response, error) in
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
 **dismissMatchRequest** | [**DismissMatchRequest**](DismissMatchRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mealMatchingGetFoodEntry**
```swift
    open class func mealMatchingGetFoodEntry(id: String, completion: @escaping (_ data: ConnectorFoodEntry?, _ error: Error?) -> Void)
```

Get a food entry for review

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a food entry for review
MealMatchingAPI.mealMatchingGetFoodEntry(id: id) { (response, error) in
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

[**ConnectorFoodEntry**](ConnectorFoodEntry.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mealMatchingGetSuggestions**
```swift
    open class func mealMatchingGetSuggestions(from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [SuggestedMealMatch]?, _ error: Error?) -> Void)
```

Get suggested meal matches for a date range

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)

// Get suggested meal matches for a date range
MealMatchingAPI.mealMatchingGetSuggestions(from: from, to: to) { (response, error) in
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

### Return type

[**[SuggestedMealMatch]**](SuggestedMealMatch.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

