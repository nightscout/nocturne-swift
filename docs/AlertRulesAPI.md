# AlertRulesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**alertRulesCreateRule**](AlertRulesAPI.md#alertrulescreaterule) | **POST** /api/v4/alert-rules | Create an alert rule with nested schedules, escalation steps, and channels.
[**alertRulesDeleteRule**](AlertRulesAPI.md#alertrulesdeleterule) | **DELETE** /api/v4/alert-rules/{id} | Delete an alert rule (cascades to schedules, steps, channels).
[**alertRulesGetRule**](AlertRulesAPI.md#alertrulesgetrule) | **GET** /api/v4/alert-rules/{id} | Get a single alert rule with full schedule/escalation tree.
[**alertRulesGetRules**](AlertRulesAPI.md#alertrulesgetrules) | **GET** /api/v4/alert-rules | List all alert rules for the current tenant with schedules and escalation steps.
[**alertRulesToggleRule**](AlertRulesAPI.md#alertrulestogglerule) | **PATCH** /api/v4/alert-rules/{id}/toggle | Toggle an alert rule enabled/disabled.
[**alertRulesUpdateRule**](AlertRulesAPI.md#alertrulesupdaterule) | **PUT** /api/v4/alert-rules/{id} | Update an alert rule.


# **alertRulesCreateRule**
```swift
    open class func alertRulesCreateRule(createAlertRuleRequest: CreateAlertRuleRequest, completion: @escaping (_ data: AlertRuleResponse?, _ error: Error?) -> Void)
```

Create an alert rule with nested schedules, escalation steps, and channels.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let createAlertRuleRequest = CreateAlertRuleRequest(name: "name_example", description: "description_example", conditionType: AlertConditionType(), conditionParams: 123, hysteresisMinutes: 123, confirmationReadings: 123, isEnabled: false, sortOrder: 123, severity: AlertRuleSeverity(), clientConfiguration: 123, schedules: [CreateAlertScheduleRequest(name: "name_example", isDefault: false, daysOfWeek: [123], startTime: "startTime_example", endTime: "endTime_example", timezone: "timezone_example", quietHoursEnabled: false, quietHoursStart: "quietHoursStart_example", quietHoursEnd: "quietHoursEnd_example", quietHoursOverrideCritical: false, escalationSteps: [CreateAlertEscalationStepRequest(stepOrder: 123, delaySeconds: 123, channels: [CreateAlertStepChannelRequest(channelType: ChannelType(), destination: "destination_example", destinationLabel: "destinationLabel_example")])])]) // CreateAlertRuleRequest | 

// Create an alert rule with nested schedules, escalation steps, and channels.
AlertRulesAPI.alertRulesCreateRule(createAlertRuleRequest: createAlertRuleRequest) { (response, error) in
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
 **createAlertRuleRequest** | [**CreateAlertRuleRequest**](CreateAlertRuleRequest.md) |  | 

### Return type

[**AlertRuleResponse**](AlertRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertRulesDeleteRule**
```swift
    open class func alertRulesDeleteRule(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete an alert rule (cascades to schedules, steps, channels).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Delete an alert rule (cascades to schedules, steps, channels).
AlertRulesAPI.alertRulesDeleteRule(id: id) { (response, error) in
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

# **alertRulesGetRule**
```swift
    open class func alertRulesGetRule(id: String, completion: @escaping (_ data: AlertRuleResponse?, _ error: Error?) -> Void)
```

Get a single alert rule with full schedule/escalation tree.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Get a single alert rule with full schedule/escalation tree.
AlertRulesAPI.alertRulesGetRule(id: id) { (response, error) in
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

[**AlertRuleResponse**](AlertRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertRulesGetRules**
```swift
    open class func alertRulesGetRules(completion: @escaping (_ data: [AlertRuleResponse]?, _ error: Error?) -> Void)
```

List all alert rules for the current tenant with schedules and escalation steps.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// List all alert rules for the current tenant with schedules and escalation steps.
AlertRulesAPI.alertRulesGetRules() { (response, error) in
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

[**[AlertRuleResponse]**](AlertRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertRulesToggleRule**
```swift
    open class func alertRulesToggleRule(id: String, completion: @escaping (_ data: AlertRuleResponse?, _ error: Error?) -> Void)
```

Toggle an alert rule enabled/disabled.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 

// Toggle an alert rule enabled/disabled.
AlertRulesAPI.alertRulesToggleRule(id: id) { (response, error) in
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

[**AlertRuleResponse**](AlertRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **alertRulesUpdateRule**
```swift
    open class func alertRulesUpdateRule(id: String, updateAlertRuleRequest: UpdateAlertRuleRequest, completion: @escaping (_ data: AlertRuleResponse?, _ error: Error?) -> Void)
```

Update an alert rule.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let id = "id_example" // String | 
let updateAlertRuleRequest = UpdateAlertRuleRequest(name: "name_example", description: "description_example", conditionType: AlertConditionType(), conditionParams: 123, hysteresisMinutes: 123, confirmationReadings: 123, isEnabled: false, sortOrder: 123, severity: AlertRuleSeverity(), clientConfiguration: 123, schedules: [CreateAlertScheduleRequest(name: "name_example", isDefault: false, daysOfWeek: [123], startTime: "startTime_example", endTime: "endTime_example", timezone: "timezone_example", quietHoursEnabled: false, quietHoursStart: "quietHoursStart_example", quietHoursEnd: "quietHoursEnd_example", quietHoursOverrideCritical: false, escalationSteps: [CreateAlertEscalationStepRequest(stepOrder: 123, delaySeconds: 123, channels: [CreateAlertStepChannelRequest(channelType: ChannelType(), destination: "destination_example", destinationLabel: "destinationLabel_example")])])]) // UpdateAlertRuleRequest | 

// Update an alert rule.
AlertRulesAPI.alertRulesUpdateRule(id: id, updateAlertRuleRequest: updateAlertRuleRequest) { (response, error) in
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
 **updateAlertRuleRequest** | [**UpdateAlertRuleRequest**](UpdateAlertRuleRequest.md) |  | 

### Return type

[**AlertRuleResponse**](AlertRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

