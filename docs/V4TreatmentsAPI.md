# V4TreatmentsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**treatmentsCreateTreatment**](V4TreatmentsAPI.md#treatmentscreatetreatment) | **POST** /api/v4/treatments | Create a treatment with tracker integration. If the treatment&#39;s event type matches a tracker&#39;s trigger event types, the tracker instance will be automatically started/restarted.
[**treatmentsCreateTreatments**](V4TreatmentsAPI.md#treatmentscreatetreatments) | **POST** /api/v4/treatments/bulk | Create multiple treatments with tracker integration.
[**treatmentsDeleteTreatment**](V4TreatmentsAPI.md#treatmentsdeletetreatment) | **DELETE** /api/v4/treatments/{id} | Delete a treatment by ID
[**treatmentsGetTreatment**](V4TreatmentsAPI.md#treatmentsgettreatment) | **GET** /api/v4/treatments/{id} | Get a specific treatment by ID
[**treatmentsGetTreatments**](V4TreatmentsAPI.md#treatmentsgettreatments) | **GET** /api/v4/treatments | Get treatments with optional filtering and pagination. Unlike V1-V3 endpoints, this does NOT include StateSpan-derived basal data. For basal delivery, query /api/v4/state-spans?category&#x3D;BasalDelivery instead.
[**treatmentsUpdateTreatment**](V4TreatmentsAPI.md#treatmentsupdatetreatment) | **PUT** /api/v4/treatments/{id} | Update an existing treatment by ID


# **treatmentsCreateTreatment**
```swift
    open class func treatmentsCreateTreatment(treatment: Treatment, completion: @escaping (_ data: Treatment?, _ error: Error?) -> Void)
```

Create a treatment with tracker integration. If the treatment's event type matches a tracker's trigger event types, the tracker instance will be automatically started/restarted.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let treatment = Treatment(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, id: "id_example", identifier: "identifier_example", srvModified: 123, srvCreated: 123, eventType: "eventType_example", reason: "reason_example", glucose: 123, glucoseType: "glucoseType_example", carbs: 123, insulin: 123, protein: 123, fat: 123, foodType: "foodType_example", units: "units_example", createdAt: "createdAt_example", duration: 123, percent: 123, absolute: 123, notes: "notes_example", enteredBy: "enteredBy_example", targetTop: 123, targetBottom: 123, profile: "profile_example", split: "split_example", date: 123, carbTime: 123, boluscalc: "TODO", timestamp: "timestamp_example", cuttedby: "cuttedby_example", cutting: "cutting_example", eventTime: "eventTime_example", preBolus: 123, rate: 123, mgdl: 123, mmol: 123, endmills: 123, durationType: "durationType_example", isAnnouncement: false, profileJson: "profileJson_example", endprofile: "endprofile_example", insulinNeedsScaleFactor: 123, absorptionTime: 123, enteredinsulin: 123, splitNow: 123, splitExt: 123, status: "status_example", relative: 123, CR: 123, NSCLIENT_ID: "NSCLIENT_ID_example", first: false, end: false, circadianPercentageProfile: false, percentage: 123, timeshift: 123, transmitterId: "transmitterId_example", remoteCarbs: 123, remoteAbsorption: 123, remoteBolus: 123, reasonDisplay: "reasonDisplay_example", otp: "otp_example", syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", automatic: false, temp: "temp_example", amount: 123, programmed: 123, unabsorbed: 123, type: "type_example", bolusType: "bolusType_example", dataSource: "dataSource_example", insulinRecommendationForCarbs: 123, insulinRecommendationForCorrection: 123, insulinProgrammed: 123, insulinDelivered: 123, insulinOnBoard: 123, bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", calculationType: CalculationType2(), durationInMilliseconds: 123, pumpId: 123, pumpSerial: "pumpSerial_example", pumpType: "pumpType_example", endId: 123, isValid: false, isReadOnly: false, isBasalInsulin: false, bolusCalculatorResult: "bolusCalculatorResult_example", originalDuration: 123, originalProfileName: "originalProfileName_example", originalPercentage: 123, originalTimeshift: 123, originalCustomizedName: "originalCustomizedName_example", originalEnd: 123, additionalProperties: "TODO", canonicalId: "canonicalId_example", dbId: "dbId_example", sources: ["sources_example"], insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123)) // Treatment | 

// Create a treatment with tracker integration. If the treatment's event type matches a tracker's trigger event types, the tracker instance will be automatically started/restarted.
V4TreatmentsAPI.treatmentsCreateTreatment(treatment: treatment) { (response, error) in
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
 **treatment** | [**Treatment**](Treatment.md) |  | 

### Return type

[**Treatment**](Treatment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **treatmentsCreateTreatments**
```swift
    open class func treatmentsCreateTreatments(treatment: [Treatment], completion: @escaping (_ data: [Treatment]?, _ error: Error?) -> Void)
```

Create multiple treatments with tracker integration.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let treatment = [Treatment(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, id: "id_example", identifier: "identifier_example", srvModified: 123, srvCreated: 123, eventType: "eventType_example", reason: "reason_example", glucose: 123, glucoseType: "glucoseType_example", carbs: 123, insulin: 123, protein: 123, fat: 123, foodType: "foodType_example", units: "units_example", createdAt: "createdAt_example", duration: 123, percent: 123, absolute: 123, notes: "notes_example", enteredBy: "enteredBy_example", targetTop: 123, targetBottom: 123, profile: "profile_example", split: "split_example", date: 123, carbTime: 123, boluscalc: "TODO", timestamp: "timestamp_example", cuttedby: "cuttedby_example", cutting: "cutting_example", eventTime: "eventTime_example", preBolus: 123, rate: 123, mgdl: 123, mmol: 123, endmills: 123, durationType: "durationType_example", isAnnouncement: false, profileJson: "profileJson_example", endprofile: "endprofile_example", insulinNeedsScaleFactor: 123, absorptionTime: 123, enteredinsulin: 123, splitNow: 123, splitExt: 123, status: "status_example", relative: 123, CR: 123, NSCLIENT_ID: "NSCLIENT_ID_example", first: false, end: false, circadianPercentageProfile: false, percentage: 123, timeshift: 123, transmitterId: "transmitterId_example", remoteCarbs: 123, remoteAbsorption: 123, remoteBolus: 123, reasonDisplay: "reasonDisplay_example", otp: "otp_example", syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", automatic: false, temp: "temp_example", amount: 123, programmed: 123, unabsorbed: 123, type: "type_example", bolusType: "bolusType_example", dataSource: "dataSource_example", insulinRecommendationForCarbs: 123, insulinRecommendationForCorrection: 123, insulinProgrammed: 123, insulinDelivered: 123, insulinOnBoard: 123, bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", calculationType: CalculationType2(), durationInMilliseconds: 123, pumpId: 123, pumpSerial: "pumpSerial_example", pumpType: "pumpType_example", endId: 123, isValid: false, isReadOnly: false, isBasalInsulin: false, bolusCalculatorResult: "bolusCalculatorResult_example", originalDuration: 123, originalProfileName: "originalProfileName_example", originalPercentage: 123, originalTimeshift: 123, originalCustomizedName: "originalCustomizedName_example", originalEnd: 123, additionalProperties: "TODO", canonicalId: "canonicalId_example", dbId: "dbId_example", sources: ["sources_example"], insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123))] // [Treatment] | 

// Create multiple treatments with tracker integration.
V4TreatmentsAPI.treatmentsCreateTreatments(treatment: treatment) { (response, error) in
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
 **treatment** | [**[Treatment]**](Treatment.md) |  | 

### Return type

[**[Treatment]**](Treatment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **treatmentsDeleteTreatment**
```swift
    open class func treatmentsDeleteTreatment(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a treatment by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a treatment by ID
V4TreatmentsAPI.treatmentsDeleteTreatment(id: id) { (response, error) in
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
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **treatmentsGetTreatment**
```swift
    open class func treatmentsGetTreatment(id: String, completion: @escaping (_ data: Treatment?, _ error: Error?) -> Void)
```

Get a specific treatment by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a specific treatment by ID
V4TreatmentsAPI.treatmentsGetTreatment(id: id) { (response, error) in
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

[**Treatment**](Treatment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **treatmentsGetTreatments**
```swift
    open class func treatmentsGetTreatments(eventType: String? = nil, count: Int? = nil, skip: Int? = nil, find: String? = nil, completion: @escaping (_ data: [Treatment]?, _ error: Error?) -> Void)
```

Get treatments with optional filtering and pagination. Unlike V1-V3 endpoints, this does NOT include StateSpan-derived basal data. For basal delivery, query /api/v4/state-spans?category=BasalDelivery instead.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let eventType = "eventType_example" // String | Optional filter by event type (optional)
let count = 987 // Int | Maximum number of treatments to return (default: 100) (optional) (default to 100)
let skip = 987 // Int | Number of treatments to skip for pagination (default: 0) (optional) (default to 0)
let find = "find_example" // String | Optional MongoDB-style query filter for advanced filtering (optional)

// Get treatments with optional filtering and pagination. Unlike V1-V3 endpoints, this does NOT include StateSpan-derived basal data. For basal delivery, query /api/v4/state-spans?category=BasalDelivery instead.
V4TreatmentsAPI.treatmentsGetTreatments(eventType: eventType, count: count, skip: skip, find: find) { (response, error) in
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
 **eventType** | **String** | Optional filter by event type | [optional] 
 **count** | **Int** | Maximum number of treatments to return (default: 100) | [optional] [default to 100]
 **skip** | **Int** | Number of treatments to skip for pagination (default: 0) | [optional] [default to 0]
 **find** | **String** | Optional MongoDB-style query filter for advanced filtering | [optional] 

### Return type

[**[Treatment]**](Treatment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **treatmentsUpdateTreatment**
```swift
    open class func treatmentsUpdateTreatment(id: String, treatment: Treatment, completion: @escaping (_ data: Treatment?, _ error: Error?) -> Void)
```

Update an existing treatment by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let treatment = Treatment(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, id: "id_example", identifier: "identifier_example", srvModified: 123, srvCreated: 123, eventType: "eventType_example", reason: "reason_example", glucose: 123, glucoseType: "glucoseType_example", carbs: 123, insulin: 123, protein: 123, fat: 123, foodType: "foodType_example", units: "units_example", createdAt: "createdAt_example", duration: 123, percent: 123, absolute: 123, notes: "notes_example", enteredBy: "enteredBy_example", targetTop: 123, targetBottom: 123, profile: "profile_example", split: "split_example", date: 123, carbTime: 123, boluscalc: "TODO", timestamp: "timestamp_example", cuttedby: "cuttedby_example", cutting: "cutting_example", eventTime: "eventTime_example", preBolus: 123, rate: 123, mgdl: 123, mmol: 123, endmills: 123, durationType: "durationType_example", isAnnouncement: false, profileJson: "profileJson_example", endprofile: "endprofile_example", insulinNeedsScaleFactor: 123, absorptionTime: 123, enteredinsulin: 123, splitNow: 123, splitExt: 123, status: "status_example", relative: 123, CR: 123, NSCLIENT_ID: "NSCLIENT_ID_example", first: false, end: false, circadianPercentageProfile: false, percentage: 123, timeshift: 123, transmitterId: "transmitterId_example", remoteCarbs: 123, remoteAbsorption: 123, remoteBolus: 123, reasonDisplay: "reasonDisplay_example", otp: "otp_example", syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", automatic: false, temp: "temp_example", amount: 123, programmed: 123, unabsorbed: 123, type: "type_example", bolusType: "bolusType_example", dataSource: "dataSource_example", insulinRecommendationForCarbs: 123, insulinRecommendationForCorrection: 123, insulinProgrammed: 123, insulinDelivered: 123, insulinOnBoard: 123, bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", calculationType: CalculationType2(), durationInMilliseconds: 123, pumpId: 123, pumpSerial: "pumpSerial_example", pumpType: "pumpType_example", endId: 123, isValid: false, isReadOnly: false, isBasalInsulin: false, bolusCalculatorResult: "bolusCalculatorResult_example", originalDuration: 123, originalProfileName: "originalProfileName_example", originalPercentage: 123, originalTimeshift: 123, originalCustomizedName: "originalCustomizedName_example", originalEnd: 123, additionalProperties: "TODO", canonicalId: "canonicalId_example", dbId: "dbId_example", sources: ["sources_example"], insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123)) // Treatment | 

// Update an existing treatment by ID
V4TreatmentsAPI.treatmentsUpdateTreatment(id: id, treatment: treatment) { (response, error) in
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
 **treatment** | [**Treatment**](Treatment.md) |  | 

### Return type

[**Treatment**](Treatment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

