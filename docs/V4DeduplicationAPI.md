# V4DeduplicationAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deduplicationCancelJob**](V4DeduplicationAPI.md#deduplicationcanceljob) | **POST** /api/v4/admin/deduplication/cancel/{jobId} | Cancel a running deduplication job.
[**deduplicationGetEntryLinkedRecords**](V4DeduplicationAPI.md#deduplicationgetentrylinkedrecords) | **GET** /api/v4/admin/deduplication/entries/{entryId}/sources | Get linked records for a specific entry by its canonical group.
[**deduplicationGetJobStatus**](V4DeduplicationAPI.md#deduplicationgetjobstatus) | **GET** /api/v4/admin/deduplication/status/{jobId} | Get the status of a deduplication job.
[**deduplicationGetRecordLinkedRecords**](V4DeduplicationAPI.md#deduplicationgetrecordlinkedrecords) | **GET** /api/v4/admin/deduplication/records/{recordType}/{recordId}/sources | Get linked records for any V4 record type by its canonical group.
[**deduplicationGetStateSpanLinkedRecords**](V4DeduplicationAPI.md#deduplicationgetstatespanlinkedrecords) | **GET** /api/v4/admin/deduplication/state-spans/{stateSpanId}/sources | Get linked records for a specific state span by its canonical group.
[**deduplicationGetTreatmentLinkedRecords**](V4DeduplicationAPI.md#deduplicationgettreatmentlinkedrecords) | **GET** /api/v4/admin/deduplication/treatments/{treatmentId}/sources | Get linked records for a specific treatment by its canonical group.
[**deduplicationStartDeduplicationJob**](V4DeduplicationAPI.md#deduplicationstartdeduplicationjob) | **POST** /api/v4/admin/deduplication/run | Start a deduplication job to link related records from different data sources. The job runs in the background and can be monitored using the status endpoint.


# **deduplicationCancelJob**
```swift
    open class func deduplicationCancelJob(jobId: String, completion: @escaping (_ data: CancelJobResponse?, _ error: Error?) -> Void)
```

Cancel a running deduplication job.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let jobId = "jobId_example" // String | The job ID to cancel

// Cancel a running deduplication job.
V4DeduplicationAPI.deduplicationCancelJob(jobId: jobId) { (response, error) in
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
 **jobId** | **String** | The job ID to cancel | 

### Return type

[**CancelJobResponse**](CancelJobResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deduplicationGetEntryLinkedRecords**
```swift
    open class func deduplicationGetEntryLinkedRecords(entryId: String, completion: @escaping (_ data: LinkedRecordsResponse?, _ error: Error?) -> Void)
```

Get linked records for a specific entry by its canonical group.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let entryId = "entryId_example" // String | The entry ID

// Get linked records for a specific entry by its canonical group.
V4DeduplicationAPI.deduplicationGetEntryLinkedRecords(entryId: entryId) { (response, error) in
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
 **entryId** | **String** | The entry ID | 

### Return type

[**LinkedRecordsResponse**](LinkedRecordsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deduplicationGetJobStatus**
```swift
    open class func deduplicationGetJobStatus(jobId: String, completion: @escaping (_ data: DeduplicationJobStatus?, _ error: Error?) -> Void)
```

Get the status of a deduplication job.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let jobId = "jobId_example" // String | The job ID returned from the run endpoint

// Get the status of a deduplication job.
V4DeduplicationAPI.deduplicationGetJobStatus(jobId: jobId) { (response, error) in
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
 **jobId** | **String** | The job ID returned from the run endpoint | 

### Return type

[**DeduplicationJobStatus**](DeduplicationJobStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deduplicationGetRecordLinkedRecords**
```swift
    open class func deduplicationGetRecordLinkedRecords(recordType: RecordType, recordId: String, completion: @escaping (_ data: LinkedRecordsResponse?, _ error: Error?) -> Void)
```

Get linked records for any V4 record type by its canonical group.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let recordType = RecordType() // RecordType | The record type (e.g. SensorGlucose, Bolus, CarbIntake)
let recordId = "recordId_example" // String | The record ID

// Get linked records for any V4 record type by its canonical group.
V4DeduplicationAPI.deduplicationGetRecordLinkedRecords(recordType: recordType, recordId: recordId) { (response, error) in
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
 **recordType** | [**RecordType**](.md) | The record type (e.g. SensorGlucose, Bolus, CarbIntake) | 
 **recordId** | **String** | The record ID | 

### Return type

[**LinkedRecordsResponse**](LinkedRecordsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deduplicationGetStateSpanLinkedRecords**
```swift
    open class func deduplicationGetStateSpanLinkedRecords(stateSpanId: String, completion: @escaping (_ data: LinkedRecordsResponse?, _ error: Error?) -> Void)
```

Get linked records for a specific state span by its canonical group.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let stateSpanId = "stateSpanId_example" // String | The state span ID

// Get linked records for a specific state span by its canonical group.
V4DeduplicationAPI.deduplicationGetStateSpanLinkedRecords(stateSpanId: stateSpanId) { (response, error) in
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
 **stateSpanId** | **String** | The state span ID | 

### Return type

[**LinkedRecordsResponse**](LinkedRecordsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deduplicationGetTreatmentLinkedRecords**
```swift
    open class func deduplicationGetTreatmentLinkedRecords(treatmentId: String, completion: @escaping (_ data: LinkedRecordsResponse?, _ error: Error?) -> Void)
```

Get linked records for a specific treatment by its canonical group.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let treatmentId = "treatmentId_example" // String | The treatment ID

// Get linked records for a specific treatment by its canonical group.
V4DeduplicationAPI.deduplicationGetTreatmentLinkedRecords(treatmentId: treatmentId) { (response, error) in
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
 **treatmentId** | **String** | The treatment ID | 

### Return type

[**LinkedRecordsResponse**](LinkedRecordsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deduplicationStartDeduplicationJob**
```swift
    open class func deduplicationStartDeduplicationJob(completion: @escaping (_ data: DeduplicationJobResponse?, _ error: Error?) -> Void)
```

Start a deduplication job to link related records from different data sources. The job runs in the background and can be monitored using the status endpoint.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Start a deduplication job to link related records from different data sources. The job runs in the background and can be monitored using the status endpoint.
V4DeduplicationAPI.deduplicationStartDeduplicationJob() { (response, error) in
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

[**DeduplicationJobResponse**](DeduplicationJobResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

