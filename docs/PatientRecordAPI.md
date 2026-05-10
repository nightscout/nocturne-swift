# PatientRecordAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**patientRecordCreateDevice**](PatientRecordAPI.md#patientrecordcreatedevice) | **POST** /api/v4/patient-record/devices | Create a new patient device
[**patientRecordCreateInsulin**](PatientRecordAPI.md#patientrecordcreateinsulin) | **POST** /api/v4/patient-record/insulins | Create a new patient insulin
[**patientRecordDeleteDevice**](PatientRecordAPI.md#patientrecorddeletedevice) | **DELETE** /api/v4/patient-record/devices/{id} | Delete a patient device
[**patientRecordDeleteInsulin**](PatientRecordAPI.md#patientrecorddeleteinsulin) | **DELETE** /api/v4/patient-record/insulins/{id} | Delete a patient insulin
[**patientRecordGetDevices**](PatientRecordAPI.md#patientrecordgetdevices) | **GET** /api/v4/patient-record/devices | Get all patient devices
[**patientRecordGetInsulins**](PatientRecordAPI.md#patientrecordgetinsulins) | **GET** /api/v4/patient-record/insulins | Get all patient insulins
[**patientRecordGetPatientRecord**](PatientRecordAPI.md#patientrecordgetpatientrecord) | **GET** /api/v4/patient-record | Get or create the patient record
[**patientRecordUpdateDevice**](PatientRecordAPI.md#patientrecordupdatedevice) | **PUT** /api/v4/patient-record/devices/{id} | Update a patient device
[**patientRecordUpdateInsulin**](PatientRecordAPI.md#patientrecordupdateinsulin) | **PUT** /api/v4/patient-record/insulins/{id} | Update a patient insulin
[**patientRecordUpdatePatientRecord**](PatientRecordAPI.md#patientrecordupdatepatientrecord) | **PUT** /api/v4/patient-record | Update the patient record


# **patientRecordCreateDevice**
```swift
    open class func patientRecordCreateDevice(patientDevice: PatientDevice, completion: @escaping (_ data: PatientDevice?, _ error: Error?) -> Void)
```

Create a new patient device

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let patientDevice = PatientDevice(id: "id_example", deviceCategory: DeviceCategory(), manufacturer: "manufacturer_example", model: "model_example", catalogId: "catalogId_example", aidAlgorithm: AidAlgorithm(), serialNumber: "serialNumber_example", deviceId: "deviceId_example", startDate: Date(), endDate: Date(), isCurrent: false, notes: "notes_example", createdAt: Date(), modifiedAt: Date()) // PatientDevice | 

// Create a new patient device
PatientRecordAPI.patientRecordCreateDevice(patientDevice: patientDevice) { (response, error) in
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
 **patientDevice** | [**PatientDevice**](PatientDevice.md) |  | 

### Return type

[**PatientDevice**](PatientDevice.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordCreateInsulin**
```swift
    open class func patientRecordCreateInsulin(patientInsulin: PatientInsulin, completion: @escaping (_ data: PatientInsulin?, _ error: Error?) -> Void)
```

Create a new patient insulin

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let patientInsulin = PatientInsulin(id: "id_example", insulinCategory: InsulinCategory(), name: "name_example", startDate: Date(), endDate: Date(), isCurrent: false, notes: "notes_example", formulationId: "formulationId_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123, role: InsulinRole(), isPrimary: false, createdAt: Date(), modifiedAt: Date()) // PatientInsulin | 

// Create a new patient insulin
PatientRecordAPI.patientRecordCreateInsulin(patientInsulin: patientInsulin) { (response, error) in
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
 **patientInsulin** | [**PatientInsulin**](PatientInsulin.md) |  | 

### Return type

[**PatientInsulin**](PatientInsulin.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordDeleteDevice**
```swift
    open class func patientRecordDeleteDevice(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a patient device

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a patient device
PatientRecordAPI.patientRecordDeleteDevice(id: id) { (response, error) in
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordDeleteInsulin**
```swift
    open class func patientRecordDeleteInsulin(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a patient insulin

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a patient insulin
PatientRecordAPI.patientRecordDeleteInsulin(id: id) { (response, error) in
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordGetDevices**
```swift
    open class func patientRecordGetDevices(completion: @escaping (_ data: [PatientDevice]?, _ error: Error?) -> Void)
```

Get all patient devices

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all patient devices
PatientRecordAPI.patientRecordGetDevices() { (response, error) in
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

[**[PatientDevice]**](PatientDevice.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordGetInsulins**
```swift
    open class func patientRecordGetInsulins(completion: @escaping (_ data: [PatientInsulin]?, _ error: Error?) -> Void)
```

Get all patient insulins

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all patient insulins
PatientRecordAPI.patientRecordGetInsulins() { (response, error) in
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

[**[PatientInsulin]**](PatientInsulin.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordGetPatientRecord**
```swift
    open class func patientRecordGetPatientRecord(completion: @escaping (_ data: PatientRecord?, _ error: Error?) -> Void)
```

Get or create the patient record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get or create the patient record
PatientRecordAPI.patientRecordGetPatientRecord() { (response, error) in
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

[**PatientRecord**](PatientRecord.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordUpdateDevice**
```swift
    open class func patientRecordUpdateDevice(id: String, patientDevice: PatientDevice, completion: @escaping (_ data: PatientDevice?, _ error: Error?) -> Void)
```

Update a patient device

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let patientDevice = PatientDevice(id: "id_example", deviceCategory: DeviceCategory(), manufacturer: "manufacturer_example", model: "model_example", catalogId: "catalogId_example", aidAlgorithm: AidAlgorithm(), serialNumber: "serialNumber_example", deviceId: "deviceId_example", startDate: Date(), endDate: Date(), isCurrent: false, notes: "notes_example", createdAt: Date(), modifiedAt: Date()) // PatientDevice | 

// Update a patient device
PatientRecordAPI.patientRecordUpdateDevice(id: id, patientDevice: patientDevice) { (response, error) in
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
 **patientDevice** | [**PatientDevice**](PatientDevice.md) |  | 

### Return type

[**PatientDevice**](PatientDevice.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordUpdateInsulin**
```swift
    open class func patientRecordUpdateInsulin(id: String, patientInsulin: PatientInsulin, completion: @escaping (_ data: PatientInsulin?, _ error: Error?) -> Void)
```

Update a patient insulin

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let patientInsulin = PatientInsulin(id: "id_example", insulinCategory: InsulinCategory(), name: "name_example", startDate: Date(), endDate: Date(), isCurrent: false, notes: "notes_example", formulationId: "formulationId_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123, role: InsulinRole(), isPrimary: false, createdAt: Date(), modifiedAt: Date()) // PatientInsulin | 

// Update a patient insulin
PatientRecordAPI.patientRecordUpdateInsulin(id: id, patientInsulin: patientInsulin) { (response, error) in
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
 **patientInsulin** | [**PatientInsulin**](PatientInsulin.md) |  | 

### Return type

[**PatientInsulin**](PatientInsulin.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patientRecordUpdatePatientRecord**
```swift
    open class func patientRecordUpdatePatientRecord(patientRecord: PatientRecord, completion: @escaping (_ data: PatientRecord?, _ error: Error?) -> Void)
```

Update the patient record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let patientRecord = PatientRecord(id: "id_example", diabetesType: DiabetesType(), diabetesTypeOther: "diabetesTypeOther_example", diagnosisDate: Date(), dateOfBirth: Date(), preferredName: "preferredName_example", pronouns: "pronouns_example", avatarUrl: "avatarUrl_example", createdAt: Date(), modifiedAt: Date()) // PatientRecord | 

// Update the patient record
PatientRecordAPI.patientRecordUpdatePatientRecord(patientRecord: patientRecord) { (response, error) in
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
 **patientRecord** | [**PatientRecord**](PatientRecord.md) |  | 

### Return type

[**PatientRecord**](PatientRecord.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

