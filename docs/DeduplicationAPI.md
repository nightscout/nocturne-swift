# DeduplicationAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deduplicationCancelJob**](DeduplicationAPI.md#deduplicationcanceljob) | **POST** /api/v4/admin/deduplication/cancel/{jobId} | 
[**deduplicationGetEntryLinkedRecords**](DeduplicationAPI.md#deduplicationgetentrylinkedrecords) | **GET** /api/v4/admin/deduplication/entries/{entryId}/sources | 
[**deduplicationGetJobStatus**](DeduplicationAPI.md#deduplicationgetjobstatus) | **GET** /api/v4/admin/deduplication/status/{jobId} | 
[**deduplicationGetRecordLinkedRecords**](DeduplicationAPI.md#deduplicationgetrecordlinkedrecords) | **GET** /api/v4/admin/deduplication/records/{recordType}/{recordId}/sources | 
[**deduplicationGetStateSpanLinkedRecords**](DeduplicationAPI.md#deduplicationgetstatespanlinkedrecords) | **GET** /api/v4/admin/deduplication/state-spans/{stateSpanId}/sources | 
[**deduplicationGetTreatmentLinkedRecords**](DeduplicationAPI.md#deduplicationgettreatmentlinkedrecords) | **GET** /api/v4/admin/deduplication/treatments/{treatmentId}/sources | 
[**deduplicationStartDeduplicationJob**](DeduplicationAPI.md#deduplicationstartdeduplicationjob) | **POST** /api/v4/admin/deduplication/run | 


# **deduplicationCancelJob**
```swift
    open class func deduplicationCancelJob(jobId: String, completion: @escaping (_ data: CancelJobResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let jobId = "jobId_example" // String | 

DeduplicationAPI.deduplicationCancelJob(jobId: jobId) { (response, error) in
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
 **jobId** | **String** |  | 

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let entryId = "entryId_example" // String | 

DeduplicationAPI.deduplicationGetEntryLinkedRecords(entryId: entryId) { (response, error) in
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
 **entryId** | **String** |  | 

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let jobId = "jobId_example" // String | 

DeduplicationAPI.deduplicationGetJobStatus(jobId: jobId) { (response, error) in
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
 **jobId** | **String** |  | 

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let recordType = RecordType() // RecordType | 
let recordId = "recordId_example" // String | 

DeduplicationAPI.deduplicationGetRecordLinkedRecords(recordType: recordType, recordId: recordId) { (response, error) in
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
 **recordType** | [**RecordType**](.md) |  | 
 **recordId** | **String** |  | 

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let stateSpanId = "stateSpanId_example" // String | 

DeduplicationAPI.deduplicationGetStateSpanLinkedRecords(stateSpanId: stateSpanId) { (response, error) in
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
 **stateSpanId** | **String** |  | 

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let treatmentId = "treatmentId_example" // String | 

DeduplicationAPI.deduplicationGetTreatmentLinkedRecords(treatmentId: treatmentId) { (response, error) in
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
 **treatmentId** | **String** |  | 

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



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


DeduplicationAPI.deduplicationStartDeduplicationJob() { (response, error) in
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

