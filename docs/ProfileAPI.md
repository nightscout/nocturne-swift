# ProfileAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**profileCreateBasalSchedule**](ProfileAPI.md#profilecreatebasalschedule) | **POST** /api/v4/profile/basal | Create a new basal schedule
[**profileCreateCarbRatioSchedule**](ProfileAPI.md#profilecreatecarbratioschedule) | **POST** /api/v4/profile/carb-ratio | Create a new carb ratio schedule
[**profileCreateSensitivitySchedule**](ProfileAPI.md#profilecreatesensitivityschedule) | **POST** /api/v4/profile/sensitivity | Create a new sensitivity schedule
[**profileCreateTargetRangeSchedule**](ProfileAPI.md#profilecreatetargetrangeschedule) | **POST** /api/v4/profile/target-range | Create a new target range schedule
[**profileCreateTherapySettings**](ProfileAPI.md#profilecreatetherapysettings) | **POST** /api/v4/profile/settings | Create a new therapy settings record
[**profileDeleteBasalSchedule**](ProfileAPI.md#profiledeletebasalschedule) | **DELETE** /api/v4/profile/basal/{id} | Delete a basal schedule
[**profileDeleteCarbRatioSchedule**](ProfileAPI.md#profiledeletecarbratioschedule) | **DELETE** /api/v4/profile/carb-ratio/{id} | Delete a carb ratio schedule
[**profileDeleteSensitivitySchedule**](ProfileAPI.md#profiledeletesensitivityschedule) | **DELETE** /api/v4/profile/sensitivity/{id} | Delete a sensitivity schedule
[**profileDeleteTargetRangeSchedule**](ProfileAPI.md#profiledeletetargetrangeschedule) | **DELETE** /api/v4/profile/target-range/{id} | Delete a target range schedule
[**profileDeleteTherapySettings**](ProfileAPI.md#profiledeletetherapysettings) | **DELETE** /api/v4/profile/settings/{id} | Delete a therapy settings record
[**profileGetBasalScheduleById**](ProfileAPI.md#profilegetbasalschedulebyid) | **GET** /api/v4/profile/basal/by-id/{id} | Get a basal schedule by ID
[**profileGetBasalSchedulesByName**](ProfileAPI.md#profilegetbasalschedulesbyname) | **GET** /api/v4/profile/basal/{profileName} | Get basal schedules by profile name
[**profileGetCarbRatioScheduleById**](ProfileAPI.md#profilegetcarbratioschedulebyid) | **GET** /api/v4/profile/carb-ratio/by-id/{id} | Get a carb ratio schedule by ID
[**profileGetCarbRatioSchedulesByName**](ProfileAPI.md#profilegetcarbratioschedulesbyname) | **GET** /api/v4/profile/carb-ratio/{profileName} | Get carb ratio schedules by profile name
[**profileGetProfileRecords**](ProfileAPI.md#profilegetprofilerecords) | **GET** /api/v4/profile/records | Get legacy Nightscout-shaped profile records projected from V4 schedule data. Intended for connector consumption where the caller needs the monolithic Profile shape (store with basal/carbratio/sens/target arrays).
[**profileGetProfileSummary**](ProfileAPI.md#profilegetprofilesummary) | **GET** /api/v4/profile/summary | Get a consolidated summary of all profile data across all profile names. Optionally provide a date range to include schedule change detection info.
[**profileGetSensitivityScheduleById**](ProfileAPI.md#profilegetsensitivityschedulebyid) | **GET** /api/v4/profile/sensitivity/by-id/{id} | Get a sensitivity schedule by ID
[**profileGetSensitivitySchedulesByName**](ProfileAPI.md#profilegetsensitivityschedulesbyname) | **GET** /api/v4/profile/sensitivity/{profileName} | Get sensitivity schedules by profile name
[**profileGetTargetRangeScheduleById**](ProfileAPI.md#profilegettargetrangeschedulebyid) | **GET** /api/v4/profile/target-range/by-id/{id} | Get a target range schedule by ID
[**profileGetTargetRangeSchedulesByName**](ProfileAPI.md#profilegettargetrangeschedulesbyname) | **GET** /api/v4/profile/target-range/{profileName} | Get target range schedules by profile name
[**profileGetTherapySettings**](ProfileAPI.md#profilegettherapysettings) | **GET** /api/v4/profile/settings | Get all therapy settings with optional filtering
[**profileGetTherapySettingsById**](ProfileAPI.md#profilegettherapysettingsbyid) | **GET** /api/v4/profile/settings/{id} | Get a therapy settings record by ID
[**profileGetTherapySettingsByName**](ProfileAPI.md#profilegettherapysettingsbyname) | **GET** /api/v4/profile/settings/by-name/{profileName} | Get therapy settings by profile name
[**profileUpdateBasalSchedule**](ProfileAPI.md#profileupdatebasalschedule) | **PUT** /api/v4/profile/basal/{id} | Update an existing basal schedule
[**profileUpdateCarbRatioSchedule**](ProfileAPI.md#profileupdatecarbratioschedule) | **PUT** /api/v4/profile/carb-ratio/{id} | Update an existing carb ratio schedule
[**profileUpdateSensitivitySchedule**](ProfileAPI.md#profileupdatesensitivityschedule) | **PUT** /api/v4/profile/sensitivity/{id} | Update an existing sensitivity schedule
[**profileUpdateTargetRangeSchedule**](ProfileAPI.md#profileupdatetargetrangeschedule) | **PUT** /api/v4/profile/target-range/{id} | Update an existing target range schedule
[**profileUpdateTherapySettings**](ProfileAPI.md#profileupdatetherapysettings) | **PUT** /api/v4/profile/settings/{id} | Update an existing therapy settings record


# **profileCreateBasalSchedule**
```swift
    open class func profileCreateBasalSchedule(basalSchedule: BasalSchedule, completion: @escaping (_ data: BasalSchedule?, _ error: Error?) -> Void)
```

Create a new basal schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let basalSchedule = BasalSchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [ScheduleEntry(time: "time_example", value: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // BasalSchedule | 

// Create a new basal schedule
ProfileAPI.profileCreateBasalSchedule(basalSchedule: basalSchedule) { (response, error) in
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
 **basalSchedule** | [**BasalSchedule**](BasalSchedule.md) |  | 

### Return type

[**BasalSchedule**](BasalSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileCreateCarbRatioSchedule**
```swift
    open class func profileCreateCarbRatioSchedule(carbRatioSchedule: CarbRatioSchedule, completion: @escaping (_ data: CarbRatioSchedule?, _ error: Error?) -> Void)
```

Create a new carb ratio schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let carbRatioSchedule = CarbRatioSchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [ScheduleEntry(time: "time_example", value: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // CarbRatioSchedule | 

// Create a new carb ratio schedule
ProfileAPI.profileCreateCarbRatioSchedule(carbRatioSchedule: carbRatioSchedule) { (response, error) in
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
 **carbRatioSchedule** | [**CarbRatioSchedule**](CarbRatioSchedule.md) |  | 

### Return type

[**CarbRatioSchedule**](CarbRatioSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileCreateSensitivitySchedule**
```swift
    open class func profileCreateSensitivitySchedule(sensitivitySchedule: SensitivitySchedule, completion: @escaping (_ data: SensitivitySchedule?, _ error: Error?) -> Void)
```

Create a new sensitivity schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let sensitivitySchedule = SensitivitySchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [ScheduleEntry(time: "time_example", value: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // SensitivitySchedule | 

// Create a new sensitivity schedule
ProfileAPI.profileCreateSensitivitySchedule(sensitivitySchedule: sensitivitySchedule) { (response, error) in
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
 **sensitivitySchedule** | [**SensitivitySchedule**](SensitivitySchedule.md) |  | 

### Return type

[**SensitivitySchedule**](SensitivitySchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileCreateTargetRangeSchedule**
```swift
    open class func profileCreateTargetRangeSchedule(targetRangeSchedule: TargetRangeSchedule, completion: @escaping (_ data: TargetRangeSchedule?, _ error: Error?) -> Void)
```

Create a new target range schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let targetRangeSchedule = TargetRangeSchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [TargetRangeEntry(time: "time_example", low: 123, high: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // TargetRangeSchedule | 

// Create a new target range schedule
ProfileAPI.profileCreateTargetRangeSchedule(targetRangeSchedule: targetRangeSchedule) { (response, error) in
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
 **targetRangeSchedule** | [**TargetRangeSchedule**](TargetRangeSchedule.md) |  | 

### Return type

[**TargetRangeSchedule**](TargetRangeSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileCreateTherapySettings**
```swift
    open class func profileCreateTherapySettings(therapySettings: TherapySettings, completion: @escaping (_ data: TherapySettings?, _ error: Error?) -> Void)
```

Create a new therapy settings record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let therapySettings = TherapySettings(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", timezone: "timezone_example", units: "units_example", dia: 123, carbsHr: 123, delay: 123, perGIValues: false, carbsHrHigh: 123, carbsHrMedium: 123, carbsHrLow: 123, delayHigh: 123, delayMedium: 123, delayLow: 123, loopSettings: LoopProfileSettings(deviceToken: "deviceToken_example", bundleIdentifier: "bundleIdentifier_example", overridePresets: [LoopOverridePreset(name: "name_example", symbol: "symbol_example", duration: 123, targetRange: LoopTargetRange(minValue: 123, maxValue: 123), insulinNeedsScaleFactor: 123)], dosingEnabled: false, minimumBGGuard: 123, preMealTargetRange: nil, workoutTargetRange: nil, maximumBolus: 123, maximumBasalRatePerHour: 123, dosingStrategy: "dosingStrategy_example", scheduleOverride: nil), isDefault: false, enteredBy: "enteredBy_example", isExternallyManaged: false, startDate: "startDate_example", additionalProperties: "TODO") // TherapySettings | 

// Create a new therapy settings record
ProfileAPI.profileCreateTherapySettings(therapySettings: therapySettings) { (response, error) in
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
 **therapySettings** | [**TherapySettings**](TherapySettings.md) |  | 

### Return type

[**TherapySettings**](TherapySettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileDeleteBasalSchedule**
```swift
    open class func profileDeleteBasalSchedule(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a basal schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a basal schedule
ProfileAPI.profileDeleteBasalSchedule(id: id) { (response, error) in
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

# **profileDeleteCarbRatioSchedule**
```swift
    open class func profileDeleteCarbRatioSchedule(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a carb ratio schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a carb ratio schedule
ProfileAPI.profileDeleteCarbRatioSchedule(id: id) { (response, error) in
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

# **profileDeleteSensitivitySchedule**
```swift
    open class func profileDeleteSensitivitySchedule(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a sensitivity schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a sensitivity schedule
ProfileAPI.profileDeleteSensitivitySchedule(id: id) { (response, error) in
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

# **profileDeleteTargetRangeSchedule**
```swift
    open class func profileDeleteTargetRangeSchedule(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a target range schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a target range schedule
ProfileAPI.profileDeleteTargetRangeSchedule(id: id) { (response, error) in
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

# **profileDeleteTherapySettings**
```swift
    open class func profileDeleteTherapySettings(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a therapy settings record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a therapy settings record
ProfileAPI.profileDeleteTherapySettings(id: id) { (response, error) in
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

# **profileGetBasalScheduleById**
```swift
    open class func profileGetBasalScheduleById(id: String, completion: @escaping (_ data: BasalSchedule?, _ error: Error?) -> Void)
```

Get a basal schedule by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a basal schedule by ID
ProfileAPI.profileGetBasalScheduleById(id: id) { (response, error) in
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

[**BasalSchedule**](BasalSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetBasalSchedulesByName**
```swift
    open class func profileGetBasalSchedulesByName(profileName: String, completion: @escaping (_ data: [BasalSchedule]?, _ error: Error?) -> Void)
```

Get basal schedules by profile name

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let profileName = "profileName_example" // String | 

// Get basal schedules by profile name
ProfileAPI.profileGetBasalSchedulesByName(profileName: profileName) { (response, error) in
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
 **profileName** | **String** |  | 

### Return type

[**[BasalSchedule]**](BasalSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetCarbRatioScheduleById**
```swift
    open class func profileGetCarbRatioScheduleById(id: String, completion: @escaping (_ data: CarbRatioSchedule?, _ error: Error?) -> Void)
```

Get a carb ratio schedule by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a carb ratio schedule by ID
ProfileAPI.profileGetCarbRatioScheduleById(id: id) { (response, error) in
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

[**CarbRatioSchedule**](CarbRatioSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetCarbRatioSchedulesByName**
```swift
    open class func profileGetCarbRatioSchedulesByName(profileName: String, completion: @escaping (_ data: [CarbRatioSchedule]?, _ error: Error?) -> Void)
```

Get carb ratio schedules by profile name

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let profileName = "profileName_example" // String | 

// Get carb ratio schedules by profile name
ProfileAPI.profileGetCarbRatioSchedulesByName(profileName: profileName) { (response, error) in
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
 **profileName** | **String** |  | 

### Return type

[**[CarbRatioSchedule]**](CarbRatioSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetProfileRecords**
```swift
    open class func profileGetProfileRecords(limit: Int? = nil, offset: Int? = nil, completion: @escaping (_ data: PaginatedResponseOfProfile?, _ error: Error?) -> Void)
```

Get legacy Nightscout-shaped profile records projected from V4 schedule data. Intended for connector consumption where the caller needs the monolithic Profile shape (store with basal/carbratio/sens/target arrays).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)

// Get legacy Nightscout-shaped profile records projected from V4 schedule data. Intended for connector consumption where the caller needs the monolithic Profile shape (store with basal/carbratio/sens/target arrays).
ProfileAPI.profileGetProfileRecords(limit: limit, offset: offset) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]

### Return type

[**PaginatedResponseOfProfile**](PaginatedResponseOfProfile.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetProfileSummary**
```swift
    open class func profileGetProfileSummary(from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: ProfileSummary?, _ error: Error?) -> Void)
```

Get a consolidated summary of all profile data across all profile names. Optionally provide a date range to include schedule change detection info.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)

// Get a consolidated summary of all profile data across all profile names. Optionally provide a date range to include schedule change detection info.
ProfileAPI.profileGetProfileSummary(from: from, to: to) { (response, error) in
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
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 

### Return type

[**ProfileSummary**](ProfileSummary.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetSensitivityScheduleById**
```swift
    open class func profileGetSensitivityScheduleById(id: String, completion: @escaping (_ data: SensitivitySchedule?, _ error: Error?) -> Void)
```

Get a sensitivity schedule by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a sensitivity schedule by ID
ProfileAPI.profileGetSensitivityScheduleById(id: id) { (response, error) in
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

[**SensitivitySchedule**](SensitivitySchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetSensitivitySchedulesByName**
```swift
    open class func profileGetSensitivitySchedulesByName(profileName: String, completion: @escaping (_ data: [SensitivitySchedule]?, _ error: Error?) -> Void)
```

Get sensitivity schedules by profile name

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let profileName = "profileName_example" // String | 

// Get sensitivity schedules by profile name
ProfileAPI.profileGetSensitivitySchedulesByName(profileName: profileName) { (response, error) in
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
 **profileName** | **String** |  | 

### Return type

[**[SensitivitySchedule]**](SensitivitySchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetTargetRangeScheduleById**
```swift
    open class func profileGetTargetRangeScheduleById(id: String, completion: @escaping (_ data: TargetRangeSchedule?, _ error: Error?) -> Void)
```

Get a target range schedule by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a target range schedule by ID
ProfileAPI.profileGetTargetRangeScheduleById(id: id) { (response, error) in
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

[**TargetRangeSchedule**](TargetRangeSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetTargetRangeSchedulesByName**
```swift
    open class func profileGetTargetRangeSchedulesByName(profileName: String, completion: @escaping (_ data: [TargetRangeSchedule]?, _ error: Error?) -> Void)
```

Get target range schedules by profile name

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let profileName = "profileName_example" // String | 

// Get target range schedules by profile name
ProfileAPI.profileGetTargetRangeSchedulesByName(profileName: profileName) { (response, error) in
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
 **profileName** | **String** |  | 

### Return type

[**[TargetRangeSchedule]**](TargetRangeSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetTherapySettings**
```swift
    open class func profileGetTherapySettings(from: Date? = nil, to: Date? = nil, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, device: String? = nil, source: String? = nil, completion: @escaping (_ data: PaginatedResponseOfTherapySettings?, _ error: Error?) -> Void)
```

Get all therapy settings with optional filtering

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let limit = 987 // Int |  (optional) (default to 100)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String |  (optional) (default to "timestamp_desc")
let device = "device_example" // String |  (optional)
let source = "source_example" // String |  (optional)

// Get all therapy settings with optional filtering
ProfileAPI.profileGetTherapySettings(from: from, to: to, limit: limit, offset: offset, sort: sort, device: device, source: source) { (response, error) in
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
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **limit** | **Int** |  | [optional] [default to 100]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** |  | [optional] [default to &quot;timestamp_desc&quot;]
 **device** | **String** |  | [optional] 
 **source** | **String** |  | [optional] 

### Return type

[**PaginatedResponseOfTherapySettings**](PaginatedResponseOfTherapySettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetTherapySettingsById**
```swift
    open class func profileGetTherapySettingsById(id: String, completion: @escaping (_ data: TherapySettings?, _ error: Error?) -> Void)
```

Get a therapy settings record by ID

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a therapy settings record by ID
ProfileAPI.profileGetTherapySettingsById(id: id) { (response, error) in
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

[**TherapySettings**](TherapySettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileGetTherapySettingsByName**
```swift
    open class func profileGetTherapySettingsByName(profileName: String, completion: @escaping (_ data: [TherapySettings]?, _ error: Error?) -> Void)
```

Get therapy settings by profile name

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let profileName = "profileName_example" // String | 

// Get therapy settings by profile name
ProfileAPI.profileGetTherapySettingsByName(profileName: profileName) { (response, error) in
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
 **profileName** | **String** |  | 

### Return type

[**[TherapySettings]**](TherapySettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileUpdateBasalSchedule**
```swift
    open class func profileUpdateBasalSchedule(id: String, basalSchedule: BasalSchedule, completion: @escaping (_ data: BasalSchedule?, _ error: Error?) -> Void)
```

Update an existing basal schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let basalSchedule = BasalSchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [ScheduleEntry(time: "time_example", value: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // BasalSchedule | 

// Update an existing basal schedule
ProfileAPI.profileUpdateBasalSchedule(id: id, basalSchedule: basalSchedule) { (response, error) in
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
 **basalSchedule** | [**BasalSchedule**](BasalSchedule.md) |  | 

### Return type

[**BasalSchedule**](BasalSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileUpdateCarbRatioSchedule**
```swift
    open class func profileUpdateCarbRatioSchedule(id: String, carbRatioSchedule: CarbRatioSchedule, completion: @escaping (_ data: CarbRatioSchedule?, _ error: Error?) -> Void)
```

Update an existing carb ratio schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let carbRatioSchedule = CarbRatioSchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [ScheduleEntry(time: "time_example", value: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // CarbRatioSchedule | 

// Update an existing carb ratio schedule
ProfileAPI.profileUpdateCarbRatioSchedule(id: id, carbRatioSchedule: carbRatioSchedule) { (response, error) in
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
 **carbRatioSchedule** | [**CarbRatioSchedule**](CarbRatioSchedule.md) |  | 

### Return type

[**CarbRatioSchedule**](CarbRatioSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileUpdateSensitivitySchedule**
```swift
    open class func profileUpdateSensitivitySchedule(id: String, sensitivitySchedule: SensitivitySchedule, completion: @escaping (_ data: SensitivitySchedule?, _ error: Error?) -> Void)
```

Update an existing sensitivity schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let sensitivitySchedule = SensitivitySchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [ScheduleEntry(time: "time_example", value: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // SensitivitySchedule | 

// Update an existing sensitivity schedule
ProfileAPI.profileUpdateSensitivitySchedule(id: id, sensitivitySchedule: sensitivitySchedule) { (response, error) in
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
 **sensitivitySchedule** | [**SensitivitySchedule**](SensitivitySchedule.md) |  | 

### Return type

[**SensitivitySchedule**](SensitivitySchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileUpdateTargetRangeSchedule**
```swift
    open class func profileUpdateTargetRangeSchedule(id: String, targetRangeSchedule: TargetRangeSchedule, completion: @escaping (_ data: TargetRangeSchedule?, _ error: Error?) -> Void)
```

Update an existing target range schedule

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let targetRangeSchedule = TargetRangeSchedule(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", entries: [TargetRangeEntry(time: "time_example", low: 123, high: 123, timeAsSeconds: 123)], additionalProperties: "TODO") // TargetRangeSchedule | 

// Update an existing target range schedule
ProfileAPI.profileUpdateTargetRangeSchedule(id: id, targetRangeSchedule: targetRangeSchedule) { (response, error) in
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
 **targetRangeSchedule** | [**TargetRangeSchedule**](TargetRangeSchedule.md) |  | 

### Return type

[**TargetRangeSchedule**](TargetRangeSchedule.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profileUpdateTherapySettings**
```swift
    open class func profileUpdateTherapySettings(id: String, therapySettings: TherapySettings, completion: @escaping (_ data: TherapySettings?, _ error: Error?) -> Void)
```

Update an existing therapy settings record

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let therapySettings = TherapySettings(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), profileName: "profileName_example", timezone: "timezone_example", units: "units_example", dia: 123, carbsHr: 123, delay: 123, perGIValues: false, carbsHrHigh: 123, carbsHrMedium: 123, carbsHrLow: 123, delayHigh: 123, delayMedium: 123, delayLow: 123, loopSettings: LoopProfileSettings(deviceToken: "deviceToken_example", bundleIdentifier: "bundleIdentifier_example", overridePresets: [LoopOverridePreset(name: "name_example", symbol: "symbol_example", duration: 123, targetRange: LoopTargetRange(minValue: 123, maxValue: 123), insulinNeedsScaleFactor: 123)], dosingEnabled: false, minimumBGGuard: 123, preMealTargetRange: nil, workoutTargetRange: nil, maximumBolus: 123, maximumBasalRatePerHour: 123, dosingStrategy: "dosingStrategy_example", scheduleOverride: nil), isDefault: false, enteredBy: "enteredBy_example", isExternallyManaged: false, startDate: "startDate_example", additionalProperties: "TODO") // TherapySettings | 

// Update an existing therapy settings record
ProfileAPI.profileUpdateTherapySettings(id: id, therapySettings: therapySettings) { (response, error) in
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
 **therapySettings** | [**TherapySettings**](TherapySettings.md) |  | 

### Return type

[**TherapySettings**](TherapySettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

