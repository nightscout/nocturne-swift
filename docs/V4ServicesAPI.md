# V4ServicesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**servicesDeleteConnectorData**](V4ServicesAPI.md#servicesdeleteconnectordata) | **DELETE** /api/v4/services/connectors/{id}/data | Delete all data from a specific connector. WARNING: This is a destructive operation that cannot be undone.
[**servicesDeleteDataSourceData**](V4ServicesAPI.md#servicesdeletedatasourcedata) | **DELETE** /api/v4/services/data-sources/{id} | Delete all data from a specific data source. WARNING: This is a destructive operation that cannot be undone.
[**servicesDeleteDemoData**](V4ServicesAPI.md#servicesdeletedemodata) | **DELETE** /api/v4/services/data-sources/demo | Delete all demo data. This operation is safe as demo data can be easily regenerated.
[**servicesGetActiveDataSources**](V4ServicesAPI.md#servicesgetactivedatasources) | **GET** /api/v4/services/data-sources | Get all active data sources that have been sending data to this Nocturne instance. This includes CGM apps, AID systems, and any other uploaders.
[**servicesGetApiInfo**](V4ServicesAPI.md#servicesgetapiinfo) | **GET** /api/v4/services/api-info | Get API endpoint information for configuring external apps. This provides all the information needed to configure xDrip+, Loop, AAPS, etc.
[**servicesGetAvailableConnectors**](V4ServicesAPI.md#servicesgetavailableconnectors) | **GET** /api/v4/services/connectors | Get available connectors that can be configured to pull data into Nocturne.
[**servicesGetConnectorCapabilities**](V4ServicesAPI.md#servicesgetconnectorcapabilities) | **GET** /api/v4/services/connectors/{id}/capabilities | Get capabilities for a specific connector.
[**servicesGetConnectorDataSummary**](V4ServicesAPI.md#servicesgetconnectordatasummary) | **GET** /api/v4/services/connectors/{id}/data-summary | Get a summary of data counts for a specific connector. Returns the number of entries, treatments, and device statuses synced by this connector.
[**servicesGetConnectorSyncStatus**](V4ServicesAPI.md#servicesgetconnectorsyncstatus) | **GET** /api/v4/services/connectors/{id}/sync-status | Get sync status for a specific connector, including latest timestamps and connector state. Used by connectors on startup to determine where to resume syncing from.
[**servicesGetDataSource**](V4ServicesAPI.md#servicesgetdatasource) | **GET** /api/v4/services/data-sources/{id} | Get detailed information about a specific data source.
[**servicesGetServicesOverview**](V4ServicesAPI.md#servicesgetservicesoverview) | **GET** /api/v4/services | Get a complete overview of services, data sources, and available integrations.
[**servicesGetUploaderApps**](V4ServicesAPI.md#servicesgetuploaderapps) | **GET** /api/v4/services/uploaders | Get uploader apps that can push data to Nocturne with setup instructions.
[**servicesGetUploaderSetup**](V4ServicesAPI.md#servicesgetuploadersetup) | **GET** /api/v4/services/uploaders/{appId}/setup | Get setup instructions for a specific uploader app.
[**servicesTriggerConnectorSync**](V4ServicesAPI.md#servicestriggerconnectorsync) | **POST** /api/v4/services/connectors/{id}/sync | Trigger a manual sync for a specific connector.


# **servicesDeleteConnectorData**
```swift
    open class func servicesDeleteConnectorData(id: String, completion: @escaping (_ data: DataSourceDeleteResult?, _ error: Error?) -> Void)
```

Delete all data from a specific connector. WARNING: This is a destructive operation that cannot be undone.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Connector ID (e.g., \"dexcom\")

// Delete all data from a specific connector. WARNING: This is a destructive operation that cannot be undone.
V4ServicesAPI.servicesDeleteConnectorData(id: id) { (response, error) in
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
 **id** | **String** | Connector ID (e.g., \&quot;dexcom\&quot;) | 

### Return type

[**DataSourceDeleteResult**](DataSourceDeleteResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesDeleteDataSourceData**
```swift
    open class func servicesDeleteDataSourceData(id: String, completion: @escaping (_ data: DataSourceDeleteResult?, _ error: Error?) -> Void)
```

Delete all data from a specific data source. WARNING: This is a destructive operation that cannot be undone.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Data source ID or device ID

// Delete all data from a specific data source. WARNING: This is a destructive operation that cannot be undone.
V4ServicesAPI.servicesDeleteDataSourceData(id: id) { (response, error) in
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
 **id** | **String** | Data source ID or device ID | 

### Return type

[**DataSourceDeleteResult**](DataSourceDeleteResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesDeleteDemoData**
```swift
    open class func servicesDeleteDemoData(completion: @escaping (_ data: DataSourceDeleteResult?, _ error: Error?) -> Void)
```

Delete all demo data. This operation is safe as demo data can be easily regenerated.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Delete all demo data. This operation is safe as demo data can be easily regenerated.
V4ServicesAPI.servicesDeleteDemoData() { (response, error) in
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

[**DataSourceDeleteResult**](DataSourceDeleteResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetActiveDataSources**
```swift
    open class func servicesGetActiveDataSources(completion: @escaping (_ data: [DataSourceInfo]?, _ error: Error?) -> Void)
```

Get all active data sources that have been sending data to this Nocturne instance. This includes CGM apps, AID systems, and any other uploaders.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all active data sources that have been sending data to this Nocturne instance. This includes CGM apps, AID systems, and any other uploaders.
V4ServicesAPI.servicesGetActiveDataSources() { (response, error) in
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

[**[DataSourceInfo]**](DataSourceInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetApiInfo**
```swift
    open class func servicesGetApiInfo(completion: @escaping (_ data: ApiEndpointInfo?, _ error: Error?) -> Void)
```

Get API endpoint information for configuring external apps. This provides all the information needed to configure xDrip+, Loop, AAPS, etc.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get API endpoint information for configuring external apps. This provides all the information needed to configure xDrip+, Loop, AAPS, etc.
V4ServicesAPI.servicesGetApiInfo() { (response, error) in
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

[**ApiEndpointInfo**](ApiEndpointInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetAvailableConnectors**
```swift
    open class func servicesGetAvailableConnectors(completion: @escaping (_ data: [AvailableConnector]?, _ error: Error?) -> Void)
```

Get available connectors that can be configured to pull data into Nocturne.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get available connectors that can be configured to pull data into Nocturne.
V4ServicesAPI.servicesGetAvailableConnectors() { (response, error) in
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

[**[AvailableConnector]**](AvailableConnector.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetConnectorCapabilities**
```swift
    open class func servicesGetConnectorCapabilities(id: String, completion: @escaping (_ data: ConnectorCapabilities?, _ error: Error?) -> Void)
```

Get capabilities for a specific connector.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The connector ID (e.g., \"dexcom\", \"libre\")

// Get capabilities for a specific connector.
V4ServicesAPI.servicesGetConnectorCapabilities(id: id) { (response, error) in
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
 **id** | **String** | The connector ID (e.g., \&quot;dexcom\&quot;, \&quot;libre\&quot;) | 

### Return type

[**ConnectorCapabilities**](ConnectorCapabilities.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetConnectorDataSummary**
```swift
    open class func servicesGetConnectorDataSummary(id: String, completion: @escaping (_ data: ConnectorDataSummary?, _ error: Error?) -> Void)
```

Get a summary of data counts for a specific connector. Returns the number of entries, treatments, and device statuses synced by this connector.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Connector ID (e.g., \"dexcom\")

// Get a summary of data counts for a specific connector. Returns the number of entries, treatments, and device statuses synced by this connector.
V4ServicesAPI.servicesGetConnectorDataSummary(id: id) { (response, error) in
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
 **id** | **String** | Connector ID (e.g., \&quot;dexcom\&quot;) | 

### Return type

[**ConnectorDataSummary**](ConnectorDataSummary.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetConnectorSyncStatus**
```swift
    open class func servicesGetConnectorSyncStatus(id: String, completion: @escaping (_ data: ConnectorSyncStatus?, _ error: Error?) -> Void)
```

Get sync status for a specific connector, including latest timestamps and connector state. Used by connectors on startup to determine where to resume syncing from.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | The connector ID (e.g., \"dexcom\", \"libre\", \"glooko\")

// Get sync status for a specific connector, including latest timestamps and connector state. Used by connectors on startup to determine where to resume syncing from.
V4ServicesAPI.servicesGetConnectorSyncStatus(id: id) { (response, error) in
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
 **id** | **String** | The connector ID (e.g., \&quot;dexcom\&quot;, \&quot;libre\&quot;, \&quot;glooko\&quot;) | 

### Return type

[**ConnectorSyncStatus**](ConnectorSyncStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetDataSource**
```swift
    open class func servicesGetDataSource(id: String, completion: @escaping (_ data: DataSourceInfo?, _ error: Error?) -> Void)
```

Get detailed information about a specific data source.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Data source ID or device ID

// Get detailed information about a specific data source.
V4ServicesAPI.servicesGetDataSource(id: id) { (response, error) in
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
 **id** | **String** | Data source ID or device ID | 

### Return type

[**DataSourceInfo**](DataSourceInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetServicesOverview**
```swift
    open class func servicesGetServicesOverview(completion: @escaping (_ data: ServicesOverview?, _ error: Error?) -> Void)
```

Get a complete overview of services, data sources, and available integrations.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get a complete overview of services, data sources, and available integrations.
V4ServicesAPI.servicesGetServicesOverview() { (response, error) in
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

[**ServicesOverview**](ServicesOverview.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetUploaderApps**
```swift
    open class func servicesGetUploaderApps(completion: @escaping (_ data: [UploaderApp]?, _ error: Error?) -> Void)
```

Get uploader apps that can push data to Nocturne with setup instructions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get uploader apps that can push data to Nocturne with setup instructions.
V4ServicesAPI.servicesGetUploaderApps() { (response, error) in
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

[**[UploaderApp]**](UploaderApp.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesGetUploaderSetup**
```swift
    open class func servicesGetUploaderSetup(appId: String, completion: @escaping (_ data: UploaderSetupResponse?, _ error: Error?) -> Void)
```

Get setup instructions for a specific uploader app.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let appId = "appId_example" // String | The uploader app ID (e.g., \"xdrip\", \"loop\", \"aaps\")

// Get setup instructions for a specific uploader app.
V4ServicesAPI.servicesGetUploaderSetup(appId: appId) { (response, error) in
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
 **appId** | **String** | The uploader app ID (e.g., \&quot;xdrip\&quot;, \&quot;loop\&quot;, \&quot;aaps\&quot;) | 

### Return type

[**UploaderSetupResponse**](UploaderSetupResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **servicesTriggerConnectorSync**
```swift
    open class func servicesTriggerConnectorSync(id: String, syncRequest: SyncRequest, completion: @escaping (_ data: SyncResult?, _ error: Error?) -> Void)
```

Trigger a manual sync for a specific connector.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Connector ID (e.g., \"dexcom\", \"tidepool\")
let syncRequest = SyncRequest(from: Date(), to: Date(), dataTypes: [SyncDataType()]) // SyncRequest | Sync request parameters (date range and data types)

// Trigger a manual sync for a specific connector.
V4ServicesAPI.servicesTriggerConnectorSync(id: id, syncRequest: syncRequest) { (response, error) in
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
 **id** | **String** | Connector ID (e.g., \&quot;dexcom\&quot;, \&quot;tidepool\&quot;) | 
 **syncRequest** | [**SyncRequest**](SyncRequest.md) | Sync request parameters (date range and data types) | 

### Return type

[**SyncResult**](SyncResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

