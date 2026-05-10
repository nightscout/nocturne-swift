# ClockFacesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clockFacesCreate**](ClockFacesAPI.md#clockfacescreate) | **POST** /api/v4/clockfaces | Create a new clock face
[**clockFacesDelete**](ClockFacesAPI.md#clockfacesdelete) | **DELETE** /api/v4/clockfaces/{id} | Delete a clock face (owner only)
[**clockFacesGetById**](ClockFacesAPI.md#clockfacesgetbyid) | **GET** /api/v4/clockfaces/{id} | Get a clock face configuration by ID (public, no authentication required)
[**clockFacesList**](ClockFacesAPI.md#clockfaceslist) | **GET** /api/v4/clockfaces | List all clock faces for the current user
[**clockFacesUpdate**](ClockFacesAPI.md#clockfacesupdate) | **PUT** /api/v4/clockfaces/{id} | Update an existing clock face (owner only)


# **clockFacesCreate**
```swift
    open class func clockFacesCreate(createClockFaceRequest: CreateClockFaceRequest, completion: @escaping (_ data: ClockFace?, _ error: Error?) -> Void)
```

Create a new clock face

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createClockFaceRequest = CreateClockFaceRequest(name: "name_example", config: ClockFaceConfig(rows: [ClockRow(elements: [ClockElement(type: "type_example", size: 123, showUnits: false, hours: 123, width: 123, height: 123, minutesAhead: 123, format: "format_example", definitionId: "definitionId_example", show: ["show_example"], categories: ["categories_example"], visibilityThreshold: "visibilityThreshold_example", text: "text_example", style: ClockElementStyle(color: "color_example", font: "font_example", fontWeight: "fontWeight_example", opacity: 123, custom: "TODO"), chartConfig: ClockChartConfig(showIob: false, showCob: false, showBasal: false, showBolus: false, showCarbs: false, showDeviceEvents: false, showAlarms: false, showTrackers: false, showPredictions: false, lockToggles: false, showLegend: false, asBackground: false))])], settings: ClockSettings(bgColor: false, staleMinutes: 123, alwaysShowTime: false, backgroundImage: "backgroundImage_example", backgroundOpacity: 123))) // CreateClockFaceRequest | Clock face creation request

// Create a new clock face
ClockFacesAPI.clockFacesCreate(createClockFaceRequest: createClockFaceRequest) { (response, error) in
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
 **createClockFaceRequest** | [**CreateClockFaceRequest**](CreateClockFaceRequest.md) | Clock face creation request | 

### Return type

[**ClockFace**](ClockFace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clockFacesDelete**
```swift
    open class func clockFacesDelete(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a clock face (owner only)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Clock face UUID

// Delete a clock face (owner only)
ClockFacesAPI.clockFacesDelete(id: id) { (response, error) in
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
 **id** | **String** | Clock face UUID | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clockFacesGetById**
```swift
    open class func clockFacesGetById(id: String, completion: @escaping (_ data: ClockFacePublicDto?, _ error: Error?) -> Void)
```

Get a clock face configuration by ID (public, no authentication required)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Clock face UUID

// Get a clock face configuration by ID (public, no authentication required)
ClockFacesAPI.clockFacesGetById(id: id) { (response, error) in
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
 **id** | **String** | Clock face UUID | 

### Return type

[**ClockFacePublicDto**](ClockFacePublicDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clockFacesList**
```swift
    open class func clockFacesList(completion: @escaping (_ data: [ClockFaceListItem]?, _ error: Error?) -> Void)
```

List all clock faces for the current user

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List all clock faces for the current user
ClockFacesAPI.clockFacesList() { (response, error) in
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

[**[ClockFaceListItem]**](ClockFaceListItem.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clockFacesUpdate**
```swift
    open class func clockFacesUpdate(id: String, updateClockFaceRequest: UpdateClockFaceRequest, completion: @escaping (_ data: ClockFace?, _ error: Error?) -> Void)
```

Update an existing clock face (owner only)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | Clock face UUID
let updateClockFaceRequest = UpdateClockFaceRequest(name: "name_example", config: ClockFaceConfig(rows: [ClockRow(elements: [ClockElement(type: "type_example", size: 123, showUnits: false, hours: 123, width: 123, height: 123, minutesAhead: 123, format: "format_example", definitionId: "definitionId_example", show: ["show_example"], categories: ["categories_example"], visibilityThreshold: "visibilityThreshold_example", text: "text_example", style: ClockElementStyle(color: "color_example", font: "font_example", fontWeight: "fontWeight_example", opacity: 123, custom: "TODO"), chartConfig: ClockChartConfig(showIob: false, showCob: false, showBasal: false, showBolus: false, showCarbs: false, showDeviceEvents: false, showAlarms: false, showTrackers: false, showPredictions: false, lockToggles: false, showLegend: false, asBackground: false))])], settings: ClockSettings(bgColor: false, staleMinutes: 123, alwaysShowTime: false, backgroundImage: "backgroundImage_example", backgroundOpacity: 123))) // UpdateClockFaceRequest | Update request

// Update an existing clock face (owner only)
ClockFacesAPI.clockFacesUpdate(id: id, updateClockFaceRequest: updateClockFaceRequest) { (response, error) in
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
 **id** | **String** | Clock face UUID | 
 **updateClockFaceRequest** | [**UpdateClockFaceRequest**](UpdateClockFaceRequest.md) | Update request | 

### Return type

[**ClockFace**](ClockFace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

