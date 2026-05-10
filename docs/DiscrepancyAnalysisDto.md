# DiscrepancyAnalysisDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | [optional] 
**correlationId** | **String** |  | [optional] 
**analysisTimestamp** | **Date** |  | [optional] 
**requestMethod** | **String** |  | [optional] 
**requestPath** | **String** |  | [optional] 
**overallMatch** | **Int** |  | [optional] 
**statusCodeMatch** | **Bool** |  | [optional] 
**bodyMatch** | **Bool** |  | [optional] 
**nightscoutStatusCode** | **Int** |  | [optional] 
**nocturneStatusCode** | **Int** |  | [optional] 
**nightscoutResponseTimeMs** | **Int64** |  | [optional] 
**nocturneResponseTimeMs** | **Int64** |  | [optional] 
**totalProcessingTimeMs** | **Int64** |  | [optional] 
**summary** | **String** |  | [optional] 
**selectedResponseTarget** | **String** |  | [optional] 
**selectionReason** | **String** |  | [optional] 
**criticalDiscrepancyCount** | **Int** |  | [optional] 
**majorDiscrepancyCount** | **Int** |  | [optional] 
**minorDiscrepancyCount** | **Int** |  | [optional] 
**nightscoutMissing** | **Bool** |  | [optional] 
**nocturneMissing** | **Bool** |  | [optional] 
**errorMessage** | **String** |  | [optional] 
**discrepancies** | [DiscrepancyDetailDto] |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


