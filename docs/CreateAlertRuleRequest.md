# CreateAlertRuleRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | [optional] 
**description** | **String** |  | [optional] 
**conditionType** | [**AlertConditionType**](AlertConditionType.md) |  | [optional] 
**conditionParams** | **JSONValue** |  | [optional] 
**hysteresisMinutes** | **Int** |  | [optional] 
**confirmationReadings** | **Int** |  | [optional] 
**isEnabled** | **Bool** |  | [optional] 
**sortOrder** | **Int** |  | [optional] 
**severity** | [**AlertRuleSeverity**](AlertRuleSeverity.md) |  | [optional] 
**clientConfiguration** | **JSONValue** |  | [optional] 
**schedules** | [CreateAlertScheduleRequest] |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


