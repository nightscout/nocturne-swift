# NutritionAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**nutritionAddCarbIntakeFood**](NutritionAPI.md#nutritionaddcarbintakefood) | **POST** /api/v4/nutrition/carbs/{id}/foods | Add a food breakdown entry to a carb intake record.
[**nutritionCreateCarbIntake**](NutritionAPI.md#nutritioncreatecarbintake) | **POST** /api/v4/nutrition/carbs | Create a new carb intake
[**nutritionCreateMeal**](NutritionAPI.md#nutritioncreatemeal) | **POST** /api/v4/nutrition/meals | Atomically create a correlated Bolus + CarbIntake for a meal event. Both records share a single CorrelationId and are persisted within a single transaction. When an existing row matches on (DataSource, SyncIdentifier), the idempotent upsert applies and the response returns 200 instead of 201.
[**nutritionDeleteCarbIntake**](NutritionAPI.md#nutritiondeletecarbintake) | **DELETE** /api/v4/nutrition/carbs/{id} | Delete a carb intake
[**nutritionDeleteCarbIntakeBySyncIdentifier**](NutritionAPI.md#nutritiondeletecarbintakebysyncidentifier) | **DELETE** /api/v4/nutrition/carbs/by-sync-id | Delete a carb intake by its external sync identifier (dataSource + syncIdentifier pair).
[**nutritionDeleteCarbIntakeFood**](NutritionAPI.md#nutritiondeletecarbintakefood) | **DELETE** /api/v4/nutrition/carbs/{id}/foods/{foodEntryId} | Remove a food breakdown entry.
[**nutritionGetCarbIntakeById**](NutritionAPI.md#nutritiongetcarbintakebyid) | **GET** /api/v4/nutrition/carbs/{id} | Get a carb intake by ID
[**nutritionGetCarbIntakeFoods**](NutritionAPI.md#nutritiongetcarbintakefoods) | **GET** /api/v4/nutrition/carbs/{id}/foods | Get food breakdown for a carb intake record.
[**nutritionGetCarbIntakes**](NutritionAPI.md#nutritiongetcarbintakes) | **GET** /api/v4/nutrition/carbs | Get carb intakes with optional filtering
[**nutritionGetMeals**](NutritionAPI.md#nutritiongetmeals) | **GET** /api/v4/nutrition/meals | Get meal events grouped by CorrelationId. Each event carries its own carb intakes, correlated boluses, food attribution rows, and aggregated totals. Carb intakes with a null CorrelationId become single-member events on their own (they are NOT collapsed together).
[**nutritionUpdateCarbIntake**](NutritionAPI.md#nutritionupdatecarbintake) | **PUT** /api/v4/nutrition/carbs/{id} | Update an existing carb intake
[**nutritionUpdateCarbIntakeFood**](NutritionAPI.md#nutritionupdatecarbintakefood) | **PUT** /api/v4/nutrition/carbs/{id}/foods/{foodEntryId} | Update a food breakdown entry.


# **nutritionAddCarbIntakeFood**
```swift
    open class func nutritionAddCarbIntakeFood(id: String, carbIntakeFoodRequest: CarbIntakeFoodRequest, completion: @escaping (_ data: TreatmentFoodBreakdown?, _ error: Error?) -> Void)
```

Add a food breakdown entry to a carb intake record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let carbIntakeFoodRequest = CarbIntakeFoodRequest(foodId: "foodId_example", portions: 123, carbs: 123, timeOffsetMinutes: 123, note: "note_example", inputMode: CarbIntakeFoodInputMode()) // CarbIntakeFoodRequest | 

// Add a food breakdown entry to a carb intake record.
NutritionAPI.nutritionAddCarbIntakeFood(id: id, carbIntakeFoodRequest: carbIntakeFoodRequest) { (response, error) in
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
 **carbIntakeFoodRequest** | [**CarbIntakeFoodRequest**](CarbIntakeFoodRequest.md) |  | 

### Return type

[**TreatmentFoodBreakdown**](TreatmentFoodBreakdown.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionCreateCarbIntake**
```swift
    open class func nutritionCreateCarbIntake(createCarbIntakeRequest: CreateCarbIntakeRequest, completion: @escaping (_ data: CarbIntake?, _ error: Error?) -> Void)
```

Create a new carb intake

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createCarbIntakeRequest = CreateCarbIntakeRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", carbs: 123, syncIdentifier: "syncIdentifier_example", carbTime: 123, absorptionTime: 123, correlationId: "correlationId_example") // CreateCarbIntakeRequest | 

// Create a new carb intake
NutritionAPI.nutritionCreateCarbIntake(createCarbIntakeRequest: createCarbIntakeRequest) { (response, error) in
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
 **createCarbIntakeRequest** | [**CreateCarbIntakeRequest**](CreateCarbIntakeRequest.md) |  | 

### Return type

[**CarbIntake**](CarbIntake.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionCreateMeal**
```swift
    open class func nutritionCreateMeal(createMealRequest: CreateMealRequest, completion: @escaping (_ data: CreateMealResponse?, _ error: Error?) -> Void)
```

Atomically create a correlated Bolus + CarbIntake for a meal event. Both records share a single CorrelationId and are persisted within a single transaction. When an existing row matches on (DataSource, SyncIdentifier), the idempotent upsert applies and the response returns 200 instead of 201.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createMealRequest = CreateMealRequest(timestamp: Date(), utcOffset: 123, insulin: 123, carbs: 123, bolusType: BolusType(), duration: 123, absorptionTime: 123, carbTime: 123, insulinType: "insulinType_example", device: "device_example", app: "app_example", dataSource: "dataSource_example", syncIdentifier: "syncIdentifier_example", bolusCalculationId: "bolusCalculationId_example", correlationId: "correlationId_example") // CreateMealRequest | 

// Atomically create a correlated Bolus + CarbIntake for a meal event. Both records share a single CorrelationId and are persisted within a single transaction. When an existing row matches on (DataSource, SyncIdentifier), the idempotent upsert applies and the response returns 200 instead of 201.
NutritionAPI.nutritionCreateMeal(createMealRequest: createMealRequest) { (response, error) in
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
 **createMealRequest** | [**CreateMealRequest**](CreateMealRequest.md) |  | 

### Return type

[**CreateMealResponse**](CreateMealResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionDeleteCarbIntake**
```swift
    open class func nutritionDeleteCarbIntake(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a carb intake

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a carb intake
NutritionAPI.nutritionDeleteCarbIntake(id: id) { (response, error) in
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

# **nutritionDeleteCarbIntakeBySyncIdentifier**
```swift
    open class func nutritionDeleteCarbIntakeBySyncIdentifier(dataSource: String? = nil, syncIdentifier: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a carb intake by its external sync identifier (dataSource + syncIdentifier pair).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let dataSource = "dataSource_example" // String |  (optional)
let syncIdentifier = "syncIdentifier_example" // String |  (optional)

// Delete a carb intake by its external sync identifier (dataSource + syncIdentifier pair).
NutritionAPI.nutritionDeleteCarbIntakeBySyncIdentifier(dataSource: dataSource, syncIdentifier: syncIdentifier) { (response, error) in
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
 **dataSource** | **String** |  | [optional] 
 **syncIdentifier** | **String** |  | [optional] 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionDeleteCarbIntakeFood**
```swift
    open class func nutritionDeleteCarbIntakeFood(id: String, foodEntryId: String, completion: @escaping (_ data: TreatmentFoodBreakdown?, _ error: Error?) -> Void)
```

Remove a food breakdown entry.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let foodEntryId = "foodEntryId_example" // String | 

// Remove a food breakdown entry.
NutritionAPI.nutritionDeleteCarbIntakeFood(id: id, foodEntryId: foodEntryId) { (response, error) in
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
 **foodEntryId** | **String** |  | 

### Return type

[**TreatmentFoodBreakdown**](TreatmentFoodBreakdown.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionGetCarbIntakeById**
```swift
    open class func nutritionGetCarbIntakeById(id: String, completion: @escaping (_ data: CarbIntake?, _ error: Error?) -> Void)
```

Get a carb intake by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a carb intake by ID
NutritionAPI.nutritionGetCarbIntakeById(id: id) { (response, error) in
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

[**CarbIntake**](CarbIntake.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionGetCarbIntakeFoods**
```swift
    open class func nutritionGetCarbIntakeFoods(id: String, completion: @escaping (_ data: TreatmentFoodBreakdown?, _ error: Error?) -> Void)
```

Get food breakdown for a carb intake record.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get food breakdown for a carb intake record.
NutritionAPI.nutritionGetCarbIntakeFoods(id: id) { (response, error) in
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

[**TreatmentFoodBreakdown**](TreatmentFoodBreakdown.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionGetCarbIntakes**
```swift
    open class func nutritionGetCarbIntakes(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfCarbIntake?, _ error: Error?) -> Void)
```

Get carb intakes with optional filtering

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

// Get carb intakes with optional filtering
NutritionAPI.nutritionGetCarbIntakes(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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

[**PaginatedResponseOfCarbIntake**](PaginatedResponseOfCarbIntake.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionGetMeals**
```swift
    open class func nutritionGetMeals(from: Date? = nil, to: Date? = nil, attributed: Bool? = nil, completion: @escaping (_ data: [MealEvent]?, _ error: Error?) -> Void)
```

Get meal events grouped by CorrelationId. Each event carries its own carb intakes, correlated boluses, food attribution rows, and aggregated totals. Carb intakes with a null CorrelationId become single-member events on their own (they are NOT collapsed together).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let attributed = true // Bool |  (optional)

// Get meal events grouped by CorrelationId. Each event carries its own carb intakes, correlated boluses, food attribution rows, and aggregated totals. Carb intakes with a null CorrelationId become single-member events on their own (they are NOT collapsed together).
NutritionAPI.nutritionGetMeals(from: from, to: to, attributed: attributed) { (response, error) in
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
 **attributed** | **Bool** |  | [optional] 

### Return type

[**[MealEvent]**](MealEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionUpdateCarbIntake**
```swift
    open class func nutritionUpdateCarbIntake(id: String, updateCarbIntakeRequest: UpdateCarbIntakeRequest, completion: @escaping (_ data: CarbIntake?, _ error: Error?) -> Void)
```

Update an existing carb intake

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateCarbIntakeRequest = UpdateCarbIntakeRequest(timestamp: Date(), utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", carbs: 123, syncIdentifier: "syncIdentifier_example", carbTime: 123, absorptionTime: 123, correlationId: "correlationId_example") // UpdateCarbIntakeRequest | 

// Update an existing carb intake
NutritionAPI.nutritionUpdateCarbIntake(id: id, updateCarbIntakeRequest: updateCarbIntakeRequest) { (response, error) in
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
 **updateCarbIntakeRequest** | [**UpdateCarbIntakeRequest**](UpdateCarbIntakeRequest.md) |  | 

### Return type

[**CarbIntake**](CarbIntake.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **nutritionUpdateCarbIntakeFood**
```swift
    open class func nutritionUpdateCarbIntakeFood(id: String, foodEntryId: String, carbIntakeFoodRequest: CarbIntakeFoodRequest, completion: @escaping (_ data: TreatmentFoodBreakdown?, _ error: Error?) -> Void)
```

Update a food breakdown entry.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let foodEntryId = "foodEntryId_example" // String | 
let carbIntakeFoodRequest = CarbIntakeFoodRequest(foodId: "foodId_example", portions: 123, carbs: 123, timeOffsetMinutes: 123, note: "note_example", inputMode: CarbIntakeFoodInputMode()) // CarbIntakeFoodRequest | 

// Update a food breakdown entry.
NutritionAPI.nutritionUpdateCarbIntakeFood(id: id, foodEntryId: foodEntryId, carbIntakeFoodRequest: carbIntakeFoodRequest) { (response, error) in
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
 **foodEntryId** | **String** |  | 
 **carbIntakeFoodRequest** | [**CarbIntakeFoodRequest**](CarbIntakeFoodRequest.md) |  | 

### Return type

[**TreatmentFoodBreakdown**](TreatmentFoodBreakdown.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

