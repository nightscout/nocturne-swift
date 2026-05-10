# ConnectorStatusAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorStatusGetStatus**](ConnectorStatusAPI.md#connectorstatusgetstatus) | **GET** /api/v4/connectors/status | Gets the current status and metrics for all registered connectors


# **connectorStatusGetStatus**
```swift
    open class func connectorStatusGetStatus(completion: @escaping (_ data: [ConnectorStatusDto]?, _ error: Error?) -> Void)
```

Gets the current status and metrics for all registered connectors

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets the current status and metrics for all registered connectors
ConnectorStatusAPI.connectorStatusGetStatus() { (response, error) in
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

[**[ConnectorStatusDto]**](ConnectorStatusDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

