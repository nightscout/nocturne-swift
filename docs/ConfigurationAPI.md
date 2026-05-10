# ConfigurationAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**configurationDeleteConfiguration**](ConfigurationAPI.md#configurationdeleteconfiguration) | **DELETE** /api/v4/connectors/config/{connectorName} | Deletes all configuration and secrets for a connector.
[**configurationGetAllConnectorStatus**](ConfigurationAPI.md#configurationgetallconnectorstatus) | **GET** /api/v4/connectors/config | Gets status information for all registered connectors.
[**configurationGetConfiguration**](ConfigurationAPI.md#configurationgetconfiguration) | **GET** /api/v4/connectors/config/{connectorName} | Gets the configuration for a specific connector. Returns runtime configuration only (secrets are not included).
[**configurationGetEffectiveConfiguration**](ConfigurationAPI.md#configurationgeteffectiveconfiguration) | **GET** /api/v4/connectors/config/{connectorName}/effective | Gets the effective configuration from a running connector. This returns the actual runtime values including those resolved from environment variables. This endpoint is public since it only exposes non-secret configuration values.
[**configurationGetSchema**](ConfigurationAPI.md#configurationgetschema) | **GET** /api/v4/connectors/config/{connectorName}/schema | Gets the JSON Schema for a connector&#39;s configuration. Schema is generated from the connector&#39;s configuration class attributes. This endpoint is public since schema is just metadata, not sensitive data.
[**configurationSaveConfiguration**](ConfigurationAPI.md#configurationsaveconfiguration) | **PUT** /api/v4/connectors/config/{connectorName} | Saves or updates runtime configuration for a connector. Only properties marked with [RuntimeConfigurable] are accepted. Validates the configuration against the connector&#39;s schema before saving.
[**configurationSaveSecrets**](ConfigurationAPI.md#configurationsavesecrets) | **PUT** /api/v4/connectors/config/{connectorName}/secrets | Saves encrypted secrets for a connector. Secrets are encrypted using AES-256-GCM before storage.
[**configurationSetActive**](ConfigurationAPI.md#configurationsetactive) | **PATCH** /api/v4/connectors/config/{connectorName}/active | Enables or disables a connector.


# **configurationDeleteConfiguration**
```swift
    open class func configurationDeleteConfiguration(connectorName: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Deletes all configuration and secrets for a connector.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | The connector name

// Deletes all configuration and secrets for a connector.
ConfigurationAPI.configurationDeleteConfiguration(connectorName: connectorName) { (response, error) in
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
 **connectorName** | **String** | The connector name | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **configurationGetAllConnectorStatus**
```swift
    open class func configurationGetAllConnectorStatus(completion: @escaping (_ data: [ConnectorStatusInfo]?, _ error: Error?) -> Void)
```

Gets status information for all registered connectors.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets status information for all registered connectors.
ConfigurationAPI.configurationGetAllConnectorStatus() { (response, error) in
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

[**[ConnectorStatusInfo]**](ConnectorStatusInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **configurationGetConfiguration**
```swift
    open class func configurationGetConfiguration(connectorName: String, completion: @escaping (_ data: ConnectorConfigurationResponse?, _ error: Error?) -> Void)
```

Gets the configuration for a specific connector. Returns runtime configuration only (secrets are not included).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | The connector name (e.g., \"Dexcom\", \"Glooko\")

// Gets the configuration for a specific connector. Returns runtime configuration only (secrets are not included).
ConfigurationAPI.configurationGetConfiguration(connectorName: connectorName) { (response, error) in
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
 **connectorName** | **String** | The connector name (e.g., \&quot;Dexcom\&quot;, \&quot;Glooko\&quot;) | 

### Return type

[**ConnectorConfigurationResponse**](ConnectorConfigurationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **configurationGetEffectiveConfiguration**
```swift
    open class func configurationGetEffectiveConfiguration(connectorName: String, completion: @escaping (_ data: [String: JSONValue]?, _ error: Error?) -> Void)
```

Gets the effective configuration from a running connector. This returns the actual runtime values including those resolved from environment variables. This endpoint is public since it only exposes non-secret configuration values.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | The connector name

// Gets the effective configuration from a running connector. This returns the actual runtime values including those resolved from environment variables. This endpoint is public since it only exposes non-secret configuration values.
ConfigurationAPI.configurationGetEffectiveConfiguration(connectorName: connectorName) { (response, error) in
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
 **connectorName** | **String** | The connector name | 

### Return type

**[String: JSONValue]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **configurationGetSchema**
```swift
    open class func configurationGetSchema(connectorName: String, completion: @escaping (_ data: JsonDocument?, _ error: Error?) -> Void)
```

Gets the JSON Schema for a connector's configuration. Schema is generated from the connector's configuration class attributes. This endpoint is public since schema is just metadata, not sensitive data.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | The connector name

// Gets the JSON Schema for a connector's configuration. Schema is generated from the connector's configuration class attributes. This endpoint is public since schema is just metadata, not sensitive data.
ConfigurationAPI.configurationGetSchema(connectorName: connectorName) { (response, error) in
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
 **connectorName** | **String** | The connector name | 

### Return type

[**JsonDocument**](JsonDocument.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **configurationSaveConfiguration**
```swift
    open class func configurationSaveConfiguration(connectorName: String, jsonDocument: JsonDocument, completion: @escaping (_ data: ConnectorConfigurationResponse?, _ error: Error?) -> Void)
```

Saves or updates runtime configuration for a connector. Only properties marked with [RuntimeConfigurable] are accepted. Validates the configuration against the connector's schema before saving.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | The connector name
let jsonDocument = JsonDocument(isDisposable: false, rootElement: 123) // JsonDocument | Configuration values as JSON

// Saves or updates runtime configuration for a connector. Only properties marked with [RuntimeConfigurable] are accepted. Validates the configuration against the connector's schema before saving.
ConfigurationAPI.configurationSaveConfiguration(connectorName: connectorName, jsonDocument: jsonDocument) { (response, error) in
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
 **connectorName** | **String** | The connector name | 
 **jsonDocument** | [**JsonDocument**](JsonDocument.md) | Configuration values as JSON | 

### Return type

[**ConnectorConfigurationResponse**](ConnectorConfigurationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **configurationSaveSecrets**
```swift
    open class func configurationSaveSecrets(connectorName: String, requestBody: [String: String], completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Saves encrypted secrets for a connector. Secrets are encrypted using AES-256-GCM before storage.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | The connector name
let requestBody = "TODO" // [String: String] | Dictionary of secret property names to plaintext values

// Saves encrypted secrets for a connector. Secrets are encrypted using AES-256-GCM before storage.
ConfigurationAPI.configurationSaveSecrets(connectorName: connectorName, requestBody: requestBody) { (response, error) in
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
 **connectorName** | **String** | The connector name | 
 **requestBody** | [**[String: String]**](String.md) | Dictionary of secret property names to plaintext values | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **configurationSetActive**
```swift
    open class func configurationSetActive(connectorName: String, setActiveRequest: SetActiveRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Enables or disables a connector.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let connectorName = "connectorName_example" // String | The connector name
let setActiveRequest = SetActiveRequest(isActive: false) // SetActiveRequest | Request containing the active state

// Enables or disables a connector.
ConfigurationAPI.configurationSetActive(connectorName: connectorName, setActiveRequest: setActiveRequest) { (response, error) in
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
 **connectorName** | **String** | The connector name | 
 **setActiveRequest** | [**SetActiveRequest**](SetActiveRequest.md) | Request containing the active state | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

