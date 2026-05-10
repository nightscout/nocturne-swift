# UISettingsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**uISettingsAddOrUpdateAlarmProfile**](UISettingsAPI.md#uisettingsaddorupdatealarmprofile) | **POST** /api/v4/ui-settings/notifications/alarms/profiles | Save a specific alarm profile.
[**uISettingsDeleteAlarmProfile**](UISettingsAPI.md#uisettingsdeletealarmprofile) | **DELETE** /api/v4/ui-settings/notifications/alarms/profiles/{profileId} | Delete an alarm profile by ID.
[**uISettingsGetAlarmConfiguration**](UISettingsAPI.md#uisettingsgetalarmconfiguration) | **GET** /api/v4/ui-settings/notifications/alarms | Get alarm profiles configuration (xDrip+-style).
[**uISettingsGetSectionSettings**](UISettingsAPI.md#uisettingsgetsectionsettings) | **GET** /api/v4/ui-settings/{section} | Get settings for a specific section.
[**uISettingsGetUISettings**](UISettingsAPI.md#uisettingsgetuisettings) | **GET** /api/v4/ui-settings | Get all UI settings configuration for frontend settings pages. In demo mode, this fetches from the demo service.
[**uISettingsSaveAlarmConfiguration**](UISettingsAPI.md#uisettingssavealarmconfiguration) | **PUT** /api/v4/ui-settings/notifications/alarms | Save alarm profiles configuration (xDrip+-style).
[**uISettingsSaveNotificationSettings**](UISettingsAPI.md#uisettingssavenotificationsettings) | **PUT** /api/v4/ui-settings/notifications | Save notification settings including alarm configuration.
[**uISettingsSaveUISettings**](UISettingsAPI.md#uisettingssaveuisettings) | **PUT** /api/v4/ui-settings | Save complete UI settings configuration.


# **uISettingsAddOrUpdateAlarmProfile**
```swift
    open class func uISettingsAddOrUpdateAlarmProfile(alarmProfileConfiguration: AlarmProfileConfiguration, completion: @escaping (_ data: UserAlarmConfiguration?, _ error: Error?) -> Void)
```

Save a specific alarm profile.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let alarmProfileConfiguration = AlarmProfileConfiguration(id: "id_example", name: "name_example", description: "description_example", enabled: false, alarmType: AlarmTriggerType(), threshold: 123, thresholdHigh: 123, forecastLeadTimeMinutes: 123, persistenceMinutes: 123, audio: AlarmAudioSettings(enabled: false, soundId: "soundId_example", customSoundUrl: "customSoundUrl_example", ascendingVolume: false, startVolume: 123, maxVolume: 123, ascendDurationSeconds: 123, repeatCount: 123), vibration: AlarmVibrationSettings(enabled: false, pattern: "pattern_example", customPattern: [123]), visual: AlarmVisualSettings(screenFlash: false, flashColor: "flashColor_example", flashIntervalMs: 123, persistentBanner: false, wakeScreen: false), snooze: AlarmSnoozeSettings(defaultMinutes: 123, options: [123], maxMinutes: 123, maxSnoozeCount: 123), reraise: AlarmReraiseSettings(enabled: false, intervalMinutes: 123, escalate: false, escalationVolumeStep: 123), smartSnooze: SmartSnoozeSettings(enabled: false, extendWhenTrendingCorrect: false, minDeltaThreshold: 123, extensionMinutes: 123, maxTotalMinutes: 123), schedule: AlarmScheduleSettings(enabled: false, activeRanges: [TimeRange(startTime: "startTime_example", endTime: "endTime_example")], activeDays: [123], timezone: "timezone_example"), priority: AlarmPriority(), overrideQuietHours: false, displayOrder: 123, createdAt: Date(), updatedAt: Date()) // AlarmProfileConfiguration | The alarm profile to save

// Save a specific alarm profile.
UISettingsAPI.uISettingsAddOrUpdateAlarmProfile(alarmProfileConfiguration: alarmProfileConfiguration) { (response, error) in
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
 **alarmProfileConfiguration** | [**AlarmProfileConfiguration**](AlarmProfileConfiguration.md) | The alarm profile to save | 

### Return type

[**UserAlarmConfiguration**](UserAlarmConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uISettingsDeleteAlarmProfile**
```swift
    open class func uISettingsDeleteAlarmProfile(profileId: String, completion: @escaping (_ data: UserAlarmConfiguration?, _ error: Error?) -> Void)
```

Delete an alarm profile by ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let profileId = "profileId_example" // String | The profile ID to delete

// Delete an alarm profile by ID.
UISettingsAPI.uISettingsDeleteAlarmProfile(profileId: profileId) { (response, error) in
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
 **profileId** | **String** | The profile ID to delete | 

### Return type

[**UserAlarmConfiguration**](UserAlarmConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uISettingsGetAlarmConfiguration**
```swift
    open class func uISettingsGetAlarmConfiguration(completion: @escaping (_ data: UserAlarmConfiguration?, _ error: Error?) -> Void)
```

Get alarm profiles configuration (xDrip+-style).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get alarm profiles configuration (xDrip+-style).
UISettingsAPI.uISettingsGetAlarmConfiguration() { (response, error) in
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

[**UserAlarmConfiguration**](UserAlarmConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uISettingsGetSectionSettings**
```swift
    open class func uISettingsGetSectionSettings(section: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Get settings for a specific section.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let section = "section_example" // String | Section name: devices, therapy, algorithm, features, notifications, or services

// Get settings for a specific section.
UISettingsAPI.uISettingsGetSectionSettings(section: section) { (response, error) in
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
 **section** | **String** | Section name: devices, therapy, algorithm, features, notifications, or services | 

### Return type

Void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uISettingsGetUISettings**
```swift
    open class func uISettingsGetUISettings(completion: @escaping (_ data: UISettingsConfiguration?, _ error: Error?) -> Void)
```

Get all UI settings configuration for frontend settings pages. In demo mode, this fetches from the demo service.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Get all UI settings configuration for frontend settings pages. In demo mode, this fetches from the demo service.
UISettingsAPI.uISettingsGetUISettings() { (response, error) in
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

[**UISettingsConfiguration**](UISettingsConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uISettingsSaveAlarmConfiguration**
```swift
    open class func uISettingsSaveAlarmConfiguration(userAlarmConfiguration: UserAlarmConfiguration, completion: @escaping (_ data: UserAlarmConfiguration?, _ error: Error?) -> Void)
```

Save alarm profiles configuration (xDrip+-style).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let userAlarmConfiguration = UserAlarmConfiguration(version: 123, enabled: false, soundEnabled: false, vibrationEnabled: false, globalVolume: 123, profiles: [AlarmProfileConfiguration(id: "id_example", name: "name_example", description: "description_example", enabled: false, alarmType: AlarmTriggerType(), threshold: 123, thresholdHigh: 123, forecastLeadTimeMinutes: 123, persistenceMinutes: 123, audio: AlarmAudioSettings(enabled: false, soundId: "soundId_example", customSoundUrl: "customSoundUrl_example", ascendingVolume: false, startVolume: 123, maxVolume: 123, ascendDurationSeconds: 123, repeatCount: 123), vibration: AlarmVibrationSettings(enabled: false, pattern: "pattern_example", customPattern: [123]), visual: AlarmVisualSettings(screenFlash: false, flashColor: "flashColor_example", flashIntervalMs: 123, persistentBanner: false, wakeScreen: false), snooze: AlarmSnoozeSettings(defaultMinutes: 123, options: [123], maxMinutes: 123, maxSnoozeCount: 123), reraise: AlarmReraiseSettings(enabled: false, intervalMinutes: 123, escalate: false, escalationVolumeStep: 123), smartSnooze: SmartSnoozeSettings(enabled: false, extendWhenTrendingCorrect: false, minDeltaThreshold: 123, extensionMinutes: 123, maxTotalMinutes: 123), schedule: AlarmScheduleSettings(enabled: false, activeRanges: [TimeRange(startTime: "startTime_example", endTime: "endTime_example")], activeDays: [123], timezone: "timezone_example"), priority: AlarmPriority(), overrideQuietHours: false, displayOrder: 123, createdAt: Date(), updatedAt: Date())], customSounds: [CustomSoundReference(id: "id_example", name: "name_example", url: "url_example", durationSeconds: 123, uploadedAt: Date())], emergencyContacts: [EmergencyContactConfig(id: "id_example", name: "name_example", phone: "phone_example", email: "email_example", criticalOnly: false, delayMinutes: 123, enabled: false)], channels: NotificationChannelsConfig(push: ChannelConfig(enabled: false, minPriority: nil), email: nil, sms: nil, pushover: PushoverChannelConfig(enabled: false, minPriority: nil, userKey: "userKey_example", apiToken: "apiToken_example"))) // UserAlarmConfiguration | The alarm configuration to save

// Save alarm profiles configuration (xDrip+-style).
UISettingsAPI.uISettingsSaveAlarmConfiguration(userAlarmConfiguration: userAlarmConfiguration) { (response, error) in
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
 **userAlarmConfiguration** | [**UserAlarmConfiguration**](UserAlarmConfiguration.md) | The alarm configuration to save | 

### Return type

[**UserAlarmConfiguration**](UserAlarmConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uISettingsSaveNotificationSettings**
```swift
    open class func uISettingsSaveNotificationSettings(notificationSettings: NotificationSettings, completion: @escaping (_ data: NotificationSettings?, _ error: Error?) -> Void)
```

Save notification settings including alarm configuration.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let notificationSettings = NotificationSettings(alarmConfiguration: UserAlarmConfiguration(version: 123, enabled: false, soundEnabled: false, vibrationEnabled: false, globalVolume: 123, profiles: [AlarmProfileConfiguration(id: "id_example", name: "name_example", description: "description_example", enabled: false, alarmType: AlarmTriggerType(), threshold: 123, thresholdHigh: 123, forecastLeadTimeMinutes: 123, persistenceMinutes: 123, audio: AlarmAudioSettings(enabled: false, soundId: "soundId_example", customSoundUrl: "customSoundUrl_example", ascendingVolume: false, startVolume: 123, maxVolume: 123, ascendDurationSeconds: 123, repeatCount: 123), vibration: AlarmVibrationSettings(enabled: false, pattern: "pattern_example", customPattern: [123]), visual: AlarmVisualSettings(screenFlash: false, flashColor: "flashColor_example", flashIntervalMs: 123, persistentBanner: false, wakeScreen: false), snooze: AlarmSnoozeSettings(defaultMinutes: 123, options: [123], maxMinutes: 123, maxSnoozeCount: 123), reraise: AlarmReraiseSettings(enabled: false, intervalMinutes: 123, escalate: false, escalationVolumeStep: 123), smartSnooze: SmartSnoozeSettings(enabled: false, extendWhenTrendingCorrect: false, minDeltaThreshold: 123, extensionMinutes: 123, maxTotalMinutes: 123), schedule: AlarmScheduleSettings(enabled: false, activeRanges: [TimeRange(startTime: "startTime_example", endTime: "endTime_example")], activeDays: [123], timezone: "timezone_example"), priority: AlarmPriority(), overrideQuietHours: false, displayOrder: 123, createdAt: Date(), updatedAt: Date())], customSounds: [CustomSoundReference(id: "id_example", name: "name_example", url: "url_example", durationSeconds: 123, uploadedAt: Date())], emergencyContacts: [EmergencyContactConfig(id: "id_example", name: "name_example", phone: "phone_example", email: "email_example", criticalOnly: false, delayMinutes: 123, enabled: false)], channels: NotificationChannelsConfig(push: ChannelConfig(enabled: false, minPriority: nil), email: nil, sms: nil, pushover: PushoverChannelConfig(enabled: false, minPriority: nil, userKey: "userKey_example", apiToken: "apiToken_example")))) // NotificationSettings | The notification settings to save

// Save notification settings including alarm configuration.
UISettingsAPI.uISettingsSaveNotificationSettings(notificationSettings: notificationSettings) { (response, error) in
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
 **notificationSettings** | [**NotificationSettings**](NotificationSettings.md) | The notification settings to save | 

### Return type

[**NotificationSettings**](NotificationSettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uISettingsSaveUISettings**
```swift
    open class func uISettingsSaveUISettings(uISettingsConfiguration: UISettingsConfiguration, completion: @escaping (_ data: UISettingsConfiguration?, _ error: Error?) -> Void)
```

Save complete UI settings configuration.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let uISettingsConfiguration = UISettingsConfiguration(devices: DeviceSettings(connectedDevices: [ConnectedDevice(id: "id_example", name: "name_example", type: "type_example", status: "status_example", battery: 123, lastSync: Date(), serialNumber: "serialNumber_example")], autoConnect: false, showRawData: false, uploadEnabled: false, cgmConfiguration: CgmConfiguration(dataSourcePriority: "dataSourcePriority_example", sensorWarmupHours: 123)), algorithm: AlgorithmSettings(prediction: PredictionSettings(enabled: false, minutes: 123, model: "model_example"), autosens: AutosensSettings(enabled: false, min: 123, max: 123), carbAbsorption: CarbAbsorptionSettings(defaultMinutes: 123, minRateGramsPerHour: 123), loop: LoopSettings(enabled: false, mode: "mode_example", maxBasalRate: 123, maxBolus: 123, smbEnabled: false, uamEnabled: false), safetyLimits: SafetyLimits(maxIOB: 123, maxDailyBasalMultiplier: 123)), features: FeatureSettings(display: DisplaySettings(nightMode: false, theme: "theme_example", timeFormat: "timeFormat_example", units: "units_example", showRawBG: false, focusHours: 123), widgets: [WidgetConfig(id: WidgetId(), enabled: false, placement: WidgetPlacement(), size: WidgetSize(), settings: "TODO")], plugins: "TODO", battery: BatteryDisplaySettings(warnThreshold: 123, urgentThreshold: 123, enableAlerts: false, recentMinutes: 123, showVoltage: false, showStatistics: false), trackerPills: TrackerPillsSettings(enabled: false, visibility: "visibility_example")), notifications: NotificationSettings(alarmConfiguration: UserAlarmConfiguration(version: 123, enabled: false, soundEnabled: false, vibrationEnabled: false, globalVolume: 123, profiles: [AlarmProfileConfiguration(id: "id_example", name: "name_example", description: "description_example", enabled: false, alarmType: AlarmTriggerType(), threshold: 123, thresholdHigh: 123, forecastLeadTimeMinutes: 123, persistenceMinutes: 123, audio: AlarmAudioSettings(enabled: false, soundId: "soundId_example", customSoundUrl: "customSoundUrl_example", ascendingVolume: false, startVolume: 123, maxVolume: 123, ascendDurationSeconds: 123, repeatCount: 123), vibration: AlarmVibrationSettings(enabled: false, pattern: "pattern_example", customPattern: [123]), visual: AlarmVisualSettings(screenFlash: false, flashColor: "flashColor_example", flashIntervalMs: 123, persistentBanner: false, wakeScreen: false), snooze: AlarmSnoozeSettings(defaultMinutes: 123, options: [123], maxMinutes: 123, maxSnoozeCount: 123), reraise: AlarmReraiseSettings(enabled: false, intervalMinutes: 123, escalate: false, escalationVolumeStep: 123), smartSnooze: SmartSnoozeSettings(enabled: false, extendWhenTrendingCorrect: false, minDeltaThreshold: 123, extensionMinutes: 123, maxTotalMinutes: 123), schedule: AlarmScheduleSettings(enabled: false, activeRanges: [TimeRange(startTime: "startTime_example", endTime: "endTime_example")], activeDays: [123], timezone: "timezone_example"), priority: AlarmPriority(), overrideQuietHours: false, displayOrder: 123, createdAt: Date(), updatedAt: Date())], customSounds: [CustomSoundReference(id: "id_example", name: "name_example", url: "url_example", durationSeconds: 123, uploadedAt: Date())], emergencyContacts: [EmergencyContactConfig(id: "id_example", name: "name_example", phone: "phone_example", email: "email_example", criticalOnly: false, delayMinutes: 123, enabled: false)], channels: NotificationChannelsConfig(push: ChannelConfig(enabled: false, minPriority: nil), email: nil, sms: nil, pushover: PushoverChannelConfig(enabled: false, minPriority: nil, userKey: "userKey_example", apiToken: "apiToken_example")))), services: ServicesSettings(connectedServices: [ConnectedService(id: "id_example", name: "name_example", type: "type_example", description: "description_example", status: "status_example", lastSync: Date(), icon: "icon_example", configured: false, enabled: false)], availableServices: [AvailableService(id: "id_example", name: "name_example", type: "type_example", description: "description_example", icon: "icon_example")], syncSettings: SyncSettings(autoSync: false, syncOnAppOpen: false, backgroundRefresh: false)), dataQuality: DataQualitySettings(sleepSchedule: SleepScheduleSettings(bedtimeHour: 123, wakeTimeHour: 123, timezone: "timezone_example"), compressionLowDetection: CompressionLowDetectionSettings(enabled: false, excludeFromStatistics: false)), security: SecuritySettings(requireAuthForPublicAccess: false, hideGlucoseInFavicon: false)) // UISettingsConfiguration | The complete settings to save

// Save complete UI settings configuration.
UISettingsAPI.uISettingsSaveUISettings(uISettingsConfiguration: uISettingsConfiguration) { (response, error) in
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
 **uISettingsConfiguration** | [**UISettingsConfiguration**](UISettingsConfiguration.md) | The complete settings to save | 

### Return type

[**UISettingsConfiguration**](UISettingsConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

