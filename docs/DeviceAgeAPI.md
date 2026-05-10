# DeviceAgeAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deviceAgeGetAllDeviceAges**](DeviceAgeAPI.md#deviceagegetalldeviceages) | **GET** /api/v4/deviceage/all | Get all device ages in a single call
[**deviceAgeGetBatteryAge**](DeviceAgeAPI.md#deviceagegetbatteryage) | **GET** /api/v4/deviceage/battery | Get pump battery age (BAGE)
[**deviceAgeGetCannulaAge**](DeviceAgeAPI.md#deviceagegetcannulaage) | **GET** /api/v4/deviceage/cannula | Get cannula/site age (CAGE)
[**deviceAgeGetInsulinAge**](DeviceAgeAPI.md#deviceagegetinsulinage) | **GET** /api/v4/deviceage/insulin | Get insulin reservoir age (IAGE)
[**deviceAgeGetSensorAge**](DeviceAgeAPI.md#deviceagegetsensorage) | **GET** /api/v4/deviceage/sensor | Get sensor age (SAGE) Returns both Sensor Start and Sensor Change events


# **deviceAgeGetAllDeviceAges**
```swift
    open class func deviceAgeGetAllDeviceAges(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Get all device ages in a single call

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all device ages in a single call
DeviceAgeAPI.deviceAgeGetAllDeviceAges() { (response, error) in
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

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceAgeGetBatteryAge**
```swift
    open class func deviceAgeGetBatteryAge(info: Int? = nil, warn: Int? = nil, urgent: Int? = nil, display: String? = nil, enableAlerts: Bool? = nil, completion: @escaping (_ data: DeviceAgeInfo?, _ error: Error?) -> Void)
```

Get pump battery age (BAGE)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let info = 987 // Int |  (optional)
let warn = 987 // Int |  (optional)
let urgent = 987 // Int |  (optional)
let display = "display_example" // String |  (optional)
let enableAlerts = true // Bool |  (optional)

// Get pump battery age (BAGE)
DeviceAgeAPI.deviceAgeGetBatteryAge(info: info, warn: warn, urgent: urgent, display: display, enableAlerts: enableAlerts) { (response, error) in
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
 **info** | **Int** |  | [optional] 
 **warn** | **Int** |  | [optional] 
 **urgent** | **Int** |  | [optional] 
 **display** | **String** |  | [optional] 
 **enableAlerts** | **Bool** |  | [optional] 

### Return type

[**DeviceAgeInfo**](DeviceAgeInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceAgeGetCannulaAge**
```swift
    open class func deviceAgeGetCannulaAge(info: Int? = nil, warn: Int? = nil, urgent: Int? = nil, display: String? = nil, enableAlerts: Bool? = nil, completion: @escaping (_ data: DeviceAgeInfo?, _ error: Error?) -> Void)
```

Get cannula/site age (CAGE)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let info = 987 // Int |  (optional)
let warn = 987 // Int |  (optional)
let urgent = 987 // Int |  (optional)
let display = "display_example" // String |  (optional)
let enableAlerts = true // Bool |  (optional)

// Get cannula/site age (CAGE)
DeviceAgeAPI.deviceAgeGetCannulaAge(info: info, warn: warn, urgent: urgent, display: display, enableAlerts: enableAlerts) { (response, error) in
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
 **info** | **Int** |  | [optional] 
 **warn** | **Int** |  | [optional] 
 **urgent** | **Int** |  | [optional] 
 **display** | **String** |  | [optional] 
 **enableAlerts** | **Bool** |  | [optional] 

### Return type

[**DeviceAgeInfo**](DeviceAgeInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceAgeGetInsulinAge**
```swift
    open class func deviceAgeGetInsulinAge(info: Int? = nil, warn: Int? = nil, urgent: Int? = nil, display: String? = nil, enableAlerts: Bool? = nil, completion: @escaping (_ data: DeviceAgeInfo?, _ error: Error?) -> Void)
```

Get insulin reservoir age (IAGE)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let info = 987 // Int |  (optional)
let warn = 987 // Int |  (optional)
let urgent = 987 // Int |  (optional)
let display = "display_example" // String |  (optional)
let enableAlerts = true // Bool |  (optional)

// Get insulin reservoir age (IAGE)
DeviceAgeAPI.deviceAgeGetInsulinAge(info: info, warn: warn, urgent: urgent, display: display, enableAlerts: enableAlerts) { (response, error) in
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
 **info** | **Int** |  | [optional] 
 **warn** | **Int** |  | [optional] 
 **urgent** | **Int** |  | [optional] 
 **display** | **String** |  | [optional] 
 **enableAlerts** | **Bool** |  | [optional] 

### Return type

[**DeviceAgeInfo**](DeviceAgeInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deviceAgeGetSensorAge**
```swift
    open class func deviceAgeGetSensorAge(info: Int? = nil, warn: Int? = nil, urgent: Int? = nil, display: String? = nil, enableAlerts: Bool? = nil, completion: @escaping (_ data: SensorAgeInfo?, _ error: Error?) -> Void)
```

Get sensor age (SAGE) Returns both Sensor Start and Sensor Change events

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let info = 987 // Int |  (optional)
let warn = 987 // Int |  (optional)
let urgent = 987 // Int |  (optional)
let display = "display_example" // String |  (optional)
let enableAlerts = true // Bool |  (optional)

// Get sensor age (SAGE) Returns both Sensor Start and Sensor Change events
DeviceAgeAPI.deviceAgeGetSensorAge(info: info, warn: warn, urgent: urgent, display: display, enableAlerts: enableAlerts) { (response, error) in
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
 **info** | **Int** |  | [optional] 
 **warn** | **Int** |  | [optional] 
 **urgent** | **Int** |  | [optional] 
 **display** | **String** |  | [optional] 
 **enableAlerts** | **Bool** |  | [optional] 

### Return type

[**SensorAgeInfo**](SensorAgeInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

