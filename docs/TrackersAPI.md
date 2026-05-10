# TrackersAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**trackersAckInstance**](TrackersAPI.md#trackersackinstance) | **POST** /api/v4/trackers/instances/{id}/ack | Acknowledge/snooze a tracker notification
[**trackersApplyPreset**](TrackersAPI.md#trackersapplypreset) | **POST** /api/v4/trackers/presets/{id}/apply | Apply a preset (starts a new instance)
[**trackersCompleteInstance**](TrackersAPI.md#trackerscompleteinstance) | **PUT** /api/v4/trackers/instances/{id}/complete | Complete a tracker instance
[**trackersCreateDefinition**](TrackersAPI.md#trackerscreatedefinition) | **POST** /api/v4/trackers/definitions | Create a new tracker definition
[**trackersCreatePreset**](TrackersAPI.md#trackerscreatepreset) | **POST** /api/v4/trackers/presets | Create a new preset
[**trackersDeleteDefinition**](TrackersAPI.md#trackersdeletedefinition) | **DELETE** /api/v4/trackers/definitions/{id} | Delete a tracker definition
[**trackersDeleteInstance**](TrackersAPI.md#trackersdeleteinstance) | **DELETE** /api/v4/trackers/instances/{id} | Delete a tracker instance
[**trackersDeletePreset**](TrackersAPI.md#trackersdeletepreset) | **DELETE** /api/v4/trackers/presets/{id} | Delete a preset
[**trackersGetActiveInstances**](TrackersAPI.md#trackersgetactiveinstances) | **GET** /api/v4/trackers/instances | Get active tracker instances
[**trackersGetDefinition**](TrackersAPI.md#trackersgetdefinition) | **GET** /api/v4/trackers/definitions/{id} | Get a specific tracker definition
[**trackersGetDefinitions**](TrackersAPI.md#trackersgetdefinitions) | **GET** /api/v4/trackers/definitions | Get all tracker definitions. Returns public trackers for unauthenticated users, or all visible trackers for authenticated users.
[**trackersGetInstanceHistory**](TrackersAPI.md#trackersgetinstancehistory) | **GET** /api/v4/trackers/instances/history | Get completed tracker instances (history)
[**trackersGetPresets**](TrackersAPI.md#trackersgetpresets) | **GET** /api/v4/trackers/presets | Get all presets for the current user
[**trackersGetUpcomingInstances**](TrackersAPI.md#trackersgetupcominginstances) | **GET** /api/v4/trackers/instances/upcoming | Get upcoming tracker expirations for calendar
[**trackersStartInstance**](TrackersAPI.md#trackersstartinstance) | **POST** /api/v4/trackers/instances | Start a new tracker instance
[**trackersUpdateDefinition**](TrackersAPI.md#trackersupdatedefinition) | **PUT** /api/v4/trackers/definitions/{id} | Update a tracker definition


# **trackersAckInstance**
```swift
    open class func trackersAckInstance(id: String, ackTrackerRequest: AckTrackerRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Acknowledge/snooze a tracker notification

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let ackTrackerRequest = AckTrackerRequest(snoozeMins: 123, global: false) // AckTrackerRequest | 

// Acknowledge/snooze a tracker notification
TrackersAPI.trackersAckInstance(id: id, ackTrackerRequest: ackTrackerRequest) { (response, error) in
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
 **ackTrackerRequest** | [**AckTrackerRequest**](AckTrackerRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersApplyPreset**
```swift
    open class func trackersApplyPreset(id: String, applyPresetRequest: ApplyPresetRequest? = nil, completion: @escaping (_ data: TrackerInstanceDto?, _ error: Error?) -> Void)
```

Apply a preset (starts a new instance)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let applyPresetRequest = ApplyPresetRequest(overrideNotes: "overrideNotes_example") // ApplyPresetRequest |  (optional)

// Apply a preset (starts a new instance)
TrackersAPI.trackersApplyPreset(id: id, applyPresetRequest: applyPresetRequest) { (response, error) in
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
 **applyPresetRequest** | [**ApplyPresetRequest**](ApplyPresetRequest.md) |  | [optional] 

### Return type

[**TrackerInstanceDto**](TrackerInstanceDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersCompleteInstance**
```swift
    open class func trackersCompleteInstance(id: String, completeTrackerInstanceRequest: CompleteTrackerInstanceRequest, completion: @escaping (_ data: TrackerInstanceDto?, _ error: Error?) -> Void)
```

Complete a tracker instance

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let completeTrackerInstanceRequest = CompleteTrackerInstanceRequest(reason: CompletionReason(), completionNotes: "completionNotes_example", completeTreatmentId: "completeTreatmentId_example", completedAt: Date()) // CompleteTrackerInstanceRequest | 

// Complete a tracker instance
TrackersAPI.trackersCompleteInstance(id: id, completeTrackerInstanceRequest: completeTrackerInstanceRequest) { (response, error) in
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
 **completeTrackerInstanceRequest** | [**CompleteTrackerInstanceRequest**](CompleteTrackerInstanceRequest.md) |  | 

### Return type

[**TrackerInstanceDto**](TrackerInstanceDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersCreateDefinition**
```swift
    open class func trackersCreateDefinition(createTrackerDefinitionRequest: CreateTrackerDefinitionRequest, completion: @escaping (_ data: TrackerDefinitionDto?, _ error: Error?) -> Void)
```

Create a new tracker definition

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createTrackerDefinitionRequest = CreateTrackerDefinitionRequest(name: "name_example", description: "description_example", category: TrackerCategory(), icon: "icon_example", triggerEventTypes: ["triggerEventTypes_example"], triggerNotesContains: "triggerNotesContains_example", lifespanHours: 123, notificationThresholds: [CreateNotificationThresholdRequest(urgency: NotificationUrgency(), hours: 123, description: "description_example", displayOrder: 123, pushEnabled: false, audioEnabled: false, audioSound: "audioSound_example", vibrateEnabled: false, repeatIntervalMins: 123, maxRepeats: 123, respectQuietHours: false)], isFavorite: false, dashboardVisibility: DashboardVisibility(), visibility: TrackerVisibility(), startEventType: "startEventType_example", completionEventType: "completionEventType_example", mode: TrackerMode()) // CreateTrackerDefinitionRequest | 

// Create a new tracker definition
TrackersAPI.trackersCreateDefinition(createTrackerDefinitionRequest: createTrackerDefinitionRequest) { (response, error) in
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
 **createTrackerDefinitionRequest** | [**CreateTrackerDefinitionRequest**](CreateTrackerDefinitionRequest.md) |  | 

### Return type

[**TrackerDefinitionDto**](TrackerDefinitionDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersCreatePreset**
```swift
    open class func trackersCreatePreset(createTrackerPresetRequest: CreateTrackerPresetRequest, completion: @escaping (_ data: TrackerPresetDto?, _ error: Error?) -> Void)
```

Create a new preset

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createTrackerPresetRequest = CreateTrackerPresetRequest(name: "name_example", definitionId: "definitionId_example", defaultStartNotes: "defaultStartNotes_example") // CreateTrackerPresetRequest | 

// Create a new preset
TrackersAPI.trackersCreatePreset(createTrackerPresetRequest: createTrackerPresetRequest) { (response, error) in
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
 **createTrackerPresetRequest** | [**CreateTrackerPresetRequest**](CreateTrackerPresetRequest.md) |  | 

### Return type

[**TrackerPresetDto**](TrackerPresetDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersDeleteDefinition**
```swift
    open class func trackersDeleteDefinition(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a tracker definition

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a tracker definition
TrackersAPI.trackersDeleteDefinition(id: id) { (response, error) in
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

# **trackersDeleteInstance**
```swift
    open class func trackersDeleteInstance(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a tracker instance

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a tracker instance
TrackersAPI.trackersDeleteInstance(id: id) { (response, error) in
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

# **trackersDeletePreset**
```swift
    open class func trackersDeletePreset(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a preset

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete a preset
TrackersAPI.trackersDeletePreset(id: id) { (response, error) in
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

# **trackersGetActiveInstances**
```swift
    open class func trackersGetActiveInstances(completion: @escaping (_ data: [TrackerInstanceDto]?, _ error: Error?) -> Void)
```

Get active tracker instances

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get active tracker instances
TrackersAPI.trackersGetActiveInstances() { (response, error) in
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

[**[TrackerInstanceDto]**](TrackerInstanceDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersGetDefinition**
```swift
    open class func trackersGetDefinition(id: String, completion: @escaping (_ data: TrackerDefinitionDto?, _ error: Error?) -> Void)
```

Get a specific tracker definition

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a specific tracker definition
TrackersAPI.trackersGetDefinition(id: id) { (response, error) in
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

[**TrackerDefinitionDto**](TrackerDefinitionDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersGetDefinitions**
```swift
    open class func trackersGetDefinitions(category: TrackersGetDefinitionsCategoryParameter? = nil, completion: @escaping (_ data: [TrackerDefinitionDto]?, _ error: Error?) -> Void)
```

Get all tracker definitions. Returns public trackers for unauthenticated users, or all visible trackers for authenticated users.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let category = Trackers_GetDefinitions_category_parameter() // TrackersGetDefinitionsCategoryParameter |  (optional)

// Get all tracker definitions. Returns public trackers for unauthenticated users, or all visible trackers for authenticated users.
TrackersAPI.trackersGetDefinitions(category: category) { (response, error) in
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
 **category** | [**TrackersGetDefinitionsCategoryParameter**](.md) |  | [optional] 

### Return type

[**[TrackerDefinitionDto]**](TrackerDefinitionDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersGetInstanceHistory**
```swift
    open class func trackersGetInstanceHistory(limit: Int? = nil, completion: @escaping (_ data: [TrackerInstanceDto]?, _ error: Error?) -> Void)
```

Get completed tracker instances (history)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let limit = 987 // Int |  (optional) (default to 100)

// Get completed tracker instances (history)
TrackersAPI.trackersGetInstanceHistory(limit: limit) { (response, error) in
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

### Return type

[**[TrackerInstanceDto]**](TrackerInstanceDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersGetPresets**
```swift
    open class func trackersGetPresets(completion: @escaping (_ data: [TrackerPresetDto]?, _ error: Error?) -> Void)
```

Get all presets for the current user

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all presets for the current user
TrackersAPI.trackersGetPresets() { (response, error) in
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

[**[TrackerPresetDto]**](TrackerPresetDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersGetUpcomingInstances**
```swift
    open class func trackersGetUpcomingInstances(from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [TrackerInstanceDto]?, _ error: Error?) -> Void)
```

Get upcoming tracker expirations for calendar

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)

// Get upcoming tracker expirations for calendar
TrackersAPI.trackersGetUpcomingInstances(from: from, to: to) { (response, error) in
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

[**[TrackerInstanceDto]**](TrackerInstanceDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersStartInstance**
```swift
    open class func trackersStartInstance(startTrackerInstanceRequest: StartTrackerInstanceRequest, completion: @escaping (_ data: TrackerInstanceDto?, _ error: Error?) -> Void)
```

Start a new tracker instance

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startTrackerInstanceRequest = StartTrackerInstanceRequest(definitionId: "definitionId_example", startNotes: "startNotes_example", startTreatmentId: "startTreatmentId_example", startedAt: Date(), scheduledAt: Date()) // StartTrackerInstanceRequest | 

// Start a new tracker instance
TrackersAPI.trackersStartInstance(startTrackerInstanceRequest: startTrackerInstanceRequest) { (response, error) in
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
 **startTrackerInstanceRequest** | [**StartTrackerInstanceRequest**](StartTrackerInstanceRequest.md) |  | 

### Return type

[**TrackerInstanceDto**](TrackerInstanceDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackersUpdateDefinition**
```swift
    open class func trackersUpdateDefinition(id: String, updateTrackerDefinitionRequest: UpdateTrackerDefinitionRequest, completion: @escaping (_ data: TrackerDefinitionDto?, _ error: Error?) -> Void)
```

Update a tracker definition

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateTrackerDefinitionRequest = UpdateTrackerDefinitionRequest(name: "name_example", description: "description_example", category: TrackerCategory(), icon: "icon_example", triggerEventTypes: ["triggerEventTypes_example"], triggerNotesContains: "triggerNotesContains_example", lifespanHours: 123, notificationThresholds: [CreateNotificationThresholdRequest(urgency: NotificationUrgency(), hours: 123, description: "description_example", displayOrder: 123, pushEnabled: false, audioEnabled: false, audioSound: "audioSound_example", vibrateEnabled: false, repeatIntervalMins: 123, maxRepeats: 123, respectQuietHours: false)], isFavorite: false, dashboardVisibility: DashboardVisibility(), visibility: TrackerVisibility(), startEventType: "startEventType_example", completionEventType: "completionEventType_example", mode: TrackerMode()) // UpdateTrackerDefinitionRequest | 

// Update a tracker definition
TrackersAPI.trackersUpdateDefinition(id: id, updateTrackerDefinitionRequest: updateTrackerDefinitionRequest) { (response, error) in
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
 **updateTrackerDefinitionRequest** | [**UpdateTrackerDefinitionRequest**](UpdateTrackerDefinitionRequest.md) |  | 

### Return type

[**TrackerDefinitionDto**](TrackerDefinitionDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

