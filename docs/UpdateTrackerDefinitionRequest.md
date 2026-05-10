# UpdateTrackerDefinitionRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | [optional] 
**description** | **String** |  | [optional] 
**category** | [**TrackerCategory**](TrackerCategory.md) |  | [optional] 
**icon** | **String** |  | [optional] 
**triggerEventTypes** | **[String]** |  | [optional] 
**triggerNotesContains** | **String** |  | [optional] 
**lifespanHours** | **Int** |  | [optional] 
**notificationThresholds** | [CreateNotificationThresholdRequest] |  | [optional] 
**isFavorite** | **Bool** |  | [optional] 
**dashboardVisibility** | [**DashboardVisibility**](DashboardVisibility.md) | Dashboard visibility: Off, Always, Info, Warn, Hazard, Urgent | [optional] 
**visibility** | [**TrackerVisibility**](TrackerVisibility.md) | Visibility level for this tracker (Public, Private, RoleRestricted) | [optional] 
**startEventType** | **String** | Event type to create when tracker is started (for Nightscout compatibility) | [optional] 
**completionEventType** | **String** | Event type to create when tracker is completed (for Nightscout compatibility) | [optional] 
**mode** | [**TrackerMode**](TrackerMode.md) | Tracker mode: Duration (time-based) or Event (scheduled datetime) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


