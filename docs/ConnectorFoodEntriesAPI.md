# ConnectorFoodEntriesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorFoodEntriesImportEntries**](ConnectorFoodEntriesAPI.md#connectorfoodentriesimportentries) | **POST** /api/v4/connector-food-entries/import | Import connector food entries.


# **connectorFoodEntriesImportEntries**
```swift
    open class func connectorFoodEntriesImportEntries(connectorFoodEntryImport: [ConnectorFoodEntryImport], completion: @escaping (_ data: [ConnectorFoodEntry]?, _ error: Error?) -> Void)
```

Import connector food entries.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorFoodEntryImport = [ConnectorFoodEntryImport(connectorSource: "connectorSource_example", externalEntryId: "externalEntryId_example", externalFoodId: "externalFoodId_example", consumedAt: Date(), loggedAt: Date(), mealName: "mealName_example", carbs: 123, protein: 123, fat: 123, energy: 123, servings: 123, servingDescription: "servingDescription_example", food: ConnectorFoodImport(externalId: "externalId_example", name: "name_example", brandName: "brandName_example", carbs: 123, protein: 123, fat: 123, energy: 123, portion: 123, unit: "unit_example"))] // [ConnectorFoodEntryImport] | 

// Import connector food entries.
ConnectorFoodEntriesAPI.connectorFoodEntriesImportEntries(connectorFoodEntryImport: connectorFoodEntryImport) { (response, error) in
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
 **connectorFoodEntryImport** | [**[ConnectorFoodEntryImport]**](ConnectorFoodEntryImport.md) |  | 

### Return type

[**[ConnectorFoodEntry]**](ConnectorFoodEntry.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

