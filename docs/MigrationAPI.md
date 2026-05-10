# MigrationAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**migrationCancelMigration**](MigrationAPI.md#migrationcancelmigration) | **POST** /api/v4/migration/{jobId}/cancel | 
[**migrationGetHistory**](MigrationAPI.md#migrationgethistory) | **GET** /api/v4/migration/history | 
[**migrationGetPendingConfig**](MigrationAPI.md#migrationgetpendingconfig) | **GET** /api/v4/migration/pending-config | 
[**migrationGetSources**](MigrationAPI.md#migrationgetsources) | **GET** /api/v4/migration/sources | 
[**migrationGetStatus**](MigrationAPI.md#migrationgetstatus) | **GET** /api/v4/migration/{jobId}/status | 
[**migrationStartFromConnector**](MigrationAPI.md#migrationstartfromconnector) | **POST** /api/v4/migration/start-from-connector/{connectorName} | Start a migration using saved connector credentials (e.g., after Nightscout connector setup).
[**migrationStartMigration**](MigrationAPI.md#migrationstartmigration) | **POST** /api/v4/migration/start | 
[**migrationTestConnection**](MigrationAPI.md#migrationtestconnection) | **POST** /api/v4/migration/test | 


# **migrationCancelMigration**
```swift
    open class func migrationCancelMigration(jobId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let jobId = "jobId_example" // String | 

MigrationAPI.migrationCancelMigration(jobId: jobId) { (response, error) in
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
 **jobId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **migrationGetHistory**
```swift
    open class func migrationGetHistory(completion: @escaping (_ data: [MigrationJobInfo]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


MigrationAPI.migrationGetHistory() { (response, error) in
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

[**[MigrationJobInfo]**](MigrationJobInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **migrationGetPendingConfig**
```swift
    open class func migrationGetPendingConfig(completion: @escaping (_ data: PendingMigrationConfig?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


MigrationAPI.migrationGetPendingConfig() { (response, error) in
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

[**PendingMigrationConfig**](PendingMigrationConfig.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **migrationGetSources**
```swift
    open class func migrationGetSources(completion: @escaping (_ data: [MigrationSourceDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


MigrationAPI.migrationGetSources() { (response, error) in
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

[**[MigrationSourceDto]**](MigrationSourceDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **migrationGetStatus**
```swift
    open class func migrationGetStatus(jobId: String, completion: @escaping (_ data: MigrationJobStatus?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let jobId = "jobId_example" // String | 

MigrationAPI.migrationGetStatus(jobId: jobId) { (response, error) in
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
 **jobId** | **String** |  | 

### Return type

[**MigrationJobStatus**](MigrationJobStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **migrationStartFromConnector**
```swift
    open class func migrationStartFromConnector(connectorName: String, completion: @escaping (_ data: MigrationJobInfo?, _ error: Error?) -> Void)
```

Start a migration using saved connector credentials (e.g., after Nightscout connector setup).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | 

// Start a migration using saved connector credentials (e.g., after Nightscout connector setup).
MigrationAPI.migrationStartFromConnector(connectorName: connectorName) { (response, error) in
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
 **connectorName** | **String** |  | 

### Return type

[**MigrationJobInfo**](MigrationJobInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **migrationStartMigration**
```swift
    open class func migrationStartMigration(startMigrationRequest: StartMigrationRequest, completion: @escaping (_ data: MigrationJobInfo?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startMigrationRequest = StartMigrationRequest(mode: MigrationMode(), nightscoutUrl: "nightscoutUrl_example", nightscoutApiSecret: "nightscoutApiSecret_example", mongoConnectionString: "mongoConnectionString_example", mongoDatabaseName: "mongoDatabaseName_example", collections: ["collections_example"], startDate: Date(), endDate: Date()) // StartMigrationRequest | 

MigrationAPI.migrationStartMigration(startMigrationRequest: startMigrationRequest) { (response, error) in
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
 **startMigrationRequest** | [**StartMigrationRequest**](StartMigrationRequest.md) |  | 

### Return type

[**MigrationJobInfo**](MigrationJobInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **migrationTestConnection**
```swift
    open class func migrationTestConnection(testMigrationConnectionRequest: TestMigrationConnectionRequest, completion: @escaping (_ data: TestMigrationConnectionResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let testMigrationConnectionRequest = TestMigrationConnectionRequest(mode: MigrationMode(), nightscoutUrl: "nightscoutUrl_example", nightscoutApiSecret: "nightscoutApiSecret_example", mongoConnectionString: "mongoConnectionString_example", mongoDatabaseName: "mongoDatabaseName_example") // TestMigrationConnectionRequest | 

MigrationAPI.migrationTestConnection(testMigrationConnectionRequest: testMigrationConnectionRequest) { (response, error) in
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
 **testMigrationConnectionRequest** | [**TestMigrationConnectionRequest**](TestMigrationConnectionRequest.md) |  | 

### Return type

[**TestMigrationConnectionResult**](TestMigrationConnectionResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

