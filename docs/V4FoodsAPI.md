# V4FoodsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**foodsAddFavorite**](V4FoodsAPI.md#foodsaddfavorite) | **POST** /api/v4/foods/{foodId}/favorite | Add a food to favorites.
[**foodsDeleteFood**](V4FoodsAPI.md#foodsdeletefood) | **DELETE** /api/v4/foods/{foodId} | Delete a food from the database, handling any meal attributions that reference it.
[**foodsGetFavorites**](V4FoodsAPI.md#foodsgetfavorites) | **GET** /api/v4/foods/favorites | Get current user&#39;s favorite foods.
[**foodsGetFoodAttributionCount**](V4FoodsAPI.md#foodsgetfoodattributioncount) | **GET** /api/v4/foods/{foodId}/attribution-count | Get how many meal attributions reference a specific food.
[**foodsGetRecentFoods**](V4FoodsAPI.md#foodsgetrecentfoods) | **GET** /api/v4/foods/recent | Get recently used foods (excluding favorites).
[**foodsRemoveFavorite**](V4FoodsAPI.md#foodsremovefavorite) | **DELETE** /api/v4/foods/{foodId}/favorite | Remove a food from favorites.


# **foodsAddFavorite**
```swift
    open class func foodsAddFavorite(foodId: String, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Add a food to favorites.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let foodId = "foodId_example" // String | 

// Add a food to favorites.
V4FoodsAPI.foodsAddFavorite(foodId: foodId) { (response, error) in
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
 **foodId** | **String** |  | 

### Return type

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **foodsDeleteFood**
```swift
    open class func foodsDeleteFood(foodId: String, attributionMode: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a food from the database, handling any meal attributions that reference it.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let foodId = "foodId_example" // String | The food ID to delete.
let attributionMode = "attributionMode_example" // String | How to handle existing attributions: \"clear\" (default) sets them to Other, \"remove\" deletes them. (optional) (default to "clear")

// Delete a food from the database, handling any meal attributions that reference it.
V4FoodsAPI.foodsDeleteFood(foodId: foodId, attributionMode: attributionMode) { (response, error) in
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
 **foodId** | **String** | The food ID to delete. | 
 **attributionMode** | **String** | How to handle existing attributions: \&quot;clear\&quot; (default) sets them to Other, \&quot;remove\&quot; deletes them. | [optional] [default to &quot;clear&quot;]

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **foodsGetFavorites**
```swift
    open class func foodsGetFavorites(completion: @escaping (_ data: [Food]?, _ error: Error?) -> Void)
```

Get current user's favorite foods.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get current user's favorite foods.
V4FoodsAPI.foodsGetFavorites() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

[**[Food]**](Food.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **foodsGetFoodAttributionCount**
```swift
    open class func foodsGetFoodAttributionCount(foodId: String, completion: @escaping (_ data: FoodAttributionCount?, _ error: Error?) -> Void)
```

Get how many meal attributions reference a specific food.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let foodId = "foodId_example" // String | 

// Get how many meal attributions reference a specific food.
V4FoodsAPI.foodsGetFoodAttributionCount(foodId: foodId) { (response, error) in
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
 **foodId** | **String** |  | 

### Return type

[**FoodAttributionCount**](FoodAttributionCount.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **foodsGetRecentFoods**
```swift
    open class func foodsGetRecentFoods(limit: Int? = nil, completion: @escaping (_ data: [Food]?, _ error: Error?) -> Void)
```

Get recently used foods (excluding favorites).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let limit = 987 // Int |  (optional) (default to 20)

// Get recently used foods (excluding favorites).
V4FoodsAPI.foodsGetRecentFoods(limit: limit) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 20]

### Return type

[**[Food]**](Food.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **foodsRemoveFavorite**
```swift
    open class func foodsRemoveFavorite(foodId: String, completion: @escaping (_ data: URL?, _ error: Error?) -> Void)
```

Remove a food from favorites.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let foodId = "foodId_example" // String | 

// Remove a food from favorites.
V4FoodsAPI.foodsRemoveFavorite(foodId: foodId) { (response, error) in
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
 **foodId** | **String** |  | 

### Return type

**URL**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

