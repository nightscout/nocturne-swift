# V4BatteryAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**batteryGetBatteryReadings**](V4BatteryAPI.md#batterygetbatteryreadings) | **GET** /api/v4/Battery/readings | Get battery readings for a device over a time period
[**batteryGetBatteryStatistics**](V4BatteryAPI.md#batterygetbatterystatistics) | **GET** /api/v4/Battery/statistics | Get battery statistics for a device or all devices
[**batteryGetChargeCycles**](V4BatteryAPI.md#batterygetchargecycles) | **GET** /api/v4/Battery/cycles | Get charge cycle history for a device
[**batteryGetCurrentBatteryStatus**](V4BatteryAPI.md#batterygetcurrentbatterystatus) | **GET** /api/v4/Battery/current | Get the current battery status for all tracked devices
[**batteryGetKnownDevices**](V4BatteryAPI.md#batterygetknowndevices) | **GET** /api/v4/Battery/devices | Get list of all known devices with battery data


# **batteryGetBatteryReadings**
```swift
    open class func batteryGetBatteryReadings(device: String? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [BatteryReading]?, _ error: Error?) -> Void)
```

Get battery readings for a device over a time period

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let device = "device_example" // String | Device identifier (optional, returns all devices if not specified) (optional)
let from = Date() // Date | Start time in milliseconds since Unix epoch (optional)
let to = Date() // Date | End time in milliseconds since Unix epoch (optional)

// Get battery readings for a device over a time period
V4BatteryAPI.batteryGetBatteryReadings(device: device, from: from, to: to) { (response, error) in
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
 **device** | **String** | Device identifier (optional, returns all devices if not specified) | [optional] 
 **from** | **Date** | Start time in milliseconds since Unix epoch | [optional] 
 **to** | **Date** | End time in milliseconds since Unix epoch | [optional] 

### Return type

[**[BatteryReading]**](BatteryReading.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **batteryGetBatteryStatistics**
```swift
    open class func batteryGetBatteryStatistics(device: String? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [BatteryStatistics]?, _ error: Error?) -> Void)
```

Get battery statistics for a device or all devices

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let device = "device_example" // String | Device identifier (optional, returns all devices if not specified) (optional)
let from = Date() // Date | Start time in milliseconds since Unix epoch (default: 7 days ago) (optional)
let to = Date() // Date | End time in milliseconds since Unix epoch (default: now) (optional)

// Get battery statistics for a device or all devices
V4BatteryAPI.batteryGetBatteryStatistics(device: device, from: from, to: to) { (response, error) in
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
 **device** | **String** | Device identifier (optional, returns all devices if not specified) | [optional] 
 **from** | **Date** | Start time in milliseconds since Unix epoch (default: 7 days ago) | [optional] 
 **to** | **Date** | End time in milliseconds since Unix epoch (default: now) | [optional] 

### Return type

[**[BatteryStatistics]**](BatteryStatistics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **batteryGetChargeCycles**
```swift
    open class func batteryGetChargeCycles(device: String? = nil, from: Date? = nil, to: Date? = nil, limit: Int? = nil, completion: @escaping (_ data: [ChargeCycle]?, _ error: Error?) -> Void)
```

Get charge cycle history for a device

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let device = "device_example" // String | Device identifier (optional, returns all devices if not specified) (optional)
let from = Date() // Date | Start time in milliseconds since Unix epoch (optional)
let to = Date() // Date | End time in milliseconds since Unix epoch (optional)
let limit = 987 // Int | Maximum number of cycles to return (default: 100) (optional) (default to 100)

// Get charge cycle history for a device
V4BatteryAPI.batteryGetChargeCycles(device: device, from: from, to: to, limit: limit) { (response, error) in
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
 **device** | **String** | Device identifier (optional, returns all devices if not specified) | [optional] 
 **from** | **Date** | Start time in milliseconds since Unix epoch | [optional] 
 **to** | **Date** | End time in milliseconds since Unix epoch | [optional] 
 **limit** | **Int** | Maximum number of cycles to return (default: 100) | [optional] [default to 100]

### Return type

[**[ChargeCycle]**](ChargeCycle.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **batteryGetCurrentBatteryStatus**
```swift
    open class func batteryGetCurrentBatteryStatus(recentMinutes: Int? = nil, completion: @escaping (_ data: CurrentBatteryStatus?, _ error: Error?) -> Void)
```

Get the current battery status for all tracked devices

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let recentMinutes = 987 // Int | How many minutes back to consider for \"recent\" readings (default: 30) (optional) (default to 30)

// Get the current battery status for all tracked devices
V4BatteryAPI.batteryGetCurrentBatteryStatus(recentMinutes: recentMinutes) { (response, error) in
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
 **recentMinutes** | **Int** | How many minutes back to consider for \&quot;recent\&quot; readings (default: 30) | [optional] [default to 30]

### Return type

[**CurrentBatteryStatus**](CurrentBatteryStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **batteryGetKnownDevices**
```swift
    open class func batteryGetKnownDevices(completion: @escaping (_ data: [String]?, _ error: Error?) -> Void)
```

Get list of all known devices with battery data

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get list of all known devices with battery data
V4BatteryAPI.batteryGetKnownDevices() { (response, error) in
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

**[String]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

