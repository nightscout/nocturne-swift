# ActogramAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**actogramGetActogram**](ActogramAPI.md#actogramgetactogram) | **GET** /api/v4/Actogram | Get actogram report data for a time window.


# **actogramGetActogram**
```swift
    open class func actogramGetActogram(startTime: Int64? = nil, endTime: Int64? = nil, completion: @escaping (_ data: ActogramReportData?, _ error: Error?) -> Void)
```

Get actogram report data for a time window.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startTime = 987 // Int64 | Start of the window as Unix milliseconds (inclusive). (optional)
let endTime = 987 // Int64 | End of the window as Unix milliseconds (exclusive).             Must be greater than startTime. (optional)

// Get actogram report data for a time window.
ActogramAPI.actogramGetActogram(startTime: startTime, endTime: endTime) { (response, error) in
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
 **startTime** | **Int64** | Start of the window as Unix milliseconds (inclusive). | [optional] 
 **endTime** | **Int64** | End of the window as Unix milliseconds (exclusive).             Must be greater than startTime. | [optional] 

### Return type

[**ActogramReportData**](ActogramReportData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

