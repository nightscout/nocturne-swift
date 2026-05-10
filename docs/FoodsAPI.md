# FoodsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**foodsAddFavorite**](FoodsAPI.md#foodsaddfavorite) | **POST** /api/v4/foods/{foodId}/favorite | Add a food to favorites.
[**foodsCreateFood**](FoodsAPI.md#foodscreatefood) | **POST** /api/v4/foods | Create a new food record.
[**foodsDeleteFood**](FoodsAPI.md#foodsdeletefood) | **DELETE** /api/v4/foods/{foodId} | Delete a food from the database, handling any meal attributions that reference it.
[**foodsGetFavorites**](FoodsAPI.md#foodsgetfavorites) | **GET** /api/v4/foods/favorites | Get current user&#39;s favorite foods.
[**foodsGetFood**](FoodsAPI.md#foodsgetfood) | **GET** /api/v4/foods/{foodId} | Get a single food by ID.
[**foodsGetFoodAttributionCount**](FoodsAPI.md#foodsgetfoodattributioncount) | **GET** /api/v4/foods/{foodId}/attribution-count | Get how many meal attributions reference a specific food.
[**foodsGetFoods**](FoodsAPI.md#foodsgetfoods) | **GET** /api/v4/foods | List foods with optional filtering and pagination. This is a V4 endpoint (not Nightscout-legacy) used by the meal attribution UI.
[**foodsGetRecentFoods**](FoodsAPI.md#foodsgetrecentfoods) | **GET** /api/v4/foods/recent | Get recently used foods (excluding favorites).
[**foodsRemoveFavorite**](FoodsAPI.md#foodsremovefavorite) | **DELETE** /api/v4/foods/{foodId}/favorite | Remove a food from favorites.
[**foodsUpdateFood**](FoodsAPI.md#foodsupdatefood) | **PUT** /api/v4/foods/{foodId} | Update an existing food record by ID.


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
FoodsAPI.foodsAddFavorite(foodId: foodId) { (response, error) in
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

# **foodsCreateFood**
```swift
    open class func foodsCreateFood(food: Food, completion: @escaping (_ data: Food?, _ error: Error?) -> Void)
```

Create a new food record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let food = Food(id: "id_example", type: "type_example", category: "category_example", subcategory: "subcategory_example", name: "name_example", portion: 123, carbs: 123, fat: 123, protein: 123, energy: 123, gi: 123, unit: "unit_example", foods: [QuickPickFood(name: "name_example", portion: 123, carbs: 123, unit: "unit_example", portions: 123)], hideafteruse: false, hidden: false, position: 123, createdAt: "createdAt_example") // Food | 

// Create a new food record.
FoodsAPI.foodsCreateFood(food: food) { (response, error) in
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
 **food** | [**Food**](Food.md) |  | 

### Return type

[**Food**](Food.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

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
FoodsAPI.foodsDeleteFood(foodId: foodId, attributionMode: attributionMode) { (response, error) in
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
FoodsAPI.foodsGetFavorites() { (response, error) in
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

# **foodsGetFood**
```swift
    open class func foodsGetFood(foodId: String, completion: @escaping (_ data: Food?, _ error: Error?) -> Void)
```

Get a single food by ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let foodId = "foodId_example" // String | 

// Get a single food by ID.
FoodsAPI.foodsGetFood(foodId: foodId) { (response, error) in
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

[**Food**](Food.md)

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
FoodsAPI.foodsGetFoodAttributionCount(foodId: foodId) { (response, error) in
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

# **foodsGetFoods**
```swift
    open class func foodsGetFoods(find: String? = nil, count: Int? = nil, skip: Int? = nil, completion: @escaping (_ data: [Food]?, _ error: Error?) -> Void)
```

List foods with optional filtering and pagination. This is a V4 endpoint (not Nightscout-legacy) used by the meal attribution UI.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let find = "find_example" // String |  (optional)
let count = 987 // Int |  (optional)
let skip = 987 // Int |  (optional)

// List foods with optional filtering and pagination. This is a V4 endpoint (not Nightscout-legacy) used by the meal attribution UI.
FoodsAPI.foodsGetFoods(find: find, count: count, skip: skip) { (response, error) in
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
 **find** | **String** |  | [optional] 
 **count** | **Int** |  | [optional] 
 **skip** | **Int** |  | [optional] 

### Return type

[**[Food]**](Food.md)

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
FoodsAPI.foodsGetRecentFoods(limit: limit) { (response, error) in
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
FoodsAPI.foodsRemoveFavorite(foodId: foodId) { (response, error) in
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

# **foodsUpdateFood**
```swift
    open class func foodsUpdateFood(foodId: String, food: Food, completion: @escaping (_ data: Food?, _ error: Error?) -> Void)
```

Update an existing food record by ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let foodId = "foodId_example" // String | 
let food = Food(id: "id_example", type: "type_example", category: "category_example", subcategory: "subcategory_example", name: "name_example", portion: 123, carbs: 123, fat: 123, protein: 123, energy: 123, gi: 123, unit: "unit_example", foods: [QuickPickFood(name: "name_example", portion: 123, carbs: 123, unit: "unit_example", portions: 123)], hideafteruse: false, hidden: false, position: 123, createdAt: "createdAt_example") // Food | 

// Update an existing food record by ID.
FoodsAPI.foodsUpdateFood(foodId: foodId, food: food) { (response, error) in
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
 **food** | [**Food**](Food.md) |  | 

### Return type

[**Food**](Food.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

