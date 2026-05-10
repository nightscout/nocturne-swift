# ConnectorStatusDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Unique identifier of the connector configuration. | [optional] 
**name** | **String** | Human-readable connector name (e.g. \&quot;Dexcom Share\&quot;, \&quot;LibreLink\&quot;). | [optional] 
**status** | **String** | High-level status label (e.g. \&quot;Active\&quot;, \&quot;Error\&quot;, \&quot;Disabled\&quot;). | [optional] 
**totalEntries** | **Int64** | Total number of entries imported by this connector over its lifetime. | [optional] 
**lastEntryTime** | **Date** | Timestamp of the most recent entry imported by this connector. | [optional] 
**entriesLast24Hours** | **Int** | Number of entries imported in the last 24 hours. | [optional] 
**state** | **String** | Current operational state of the connector. | [optional] 
**stateMessage** | **String** | Optional message providing detail about the current state (e.g. error description). | [optional] 
**isHealthy** | **Bool** | Whether the connector is considered healthy based on recent sync activity. | [optional] 
**lastSyncAttempt** | **Date** | When the connector last attempted to sync | [optional] 
**lastSuccessfulSync** | **Date** | When the connector last successfully completed a sync | [optional] 
**lastErrorAt** | **Date** | When the last error occurred | [optional] 
**totalItemsBreakdown** | **[String: Int64]** | Breakdown of total items processed by data type Keys are data type names (e.g., \&quot;Glucose\&quot;, \&quot;Treatments\&quot;, \&quot;Food\&quot;) | [optional] 
**itemsLast24HoursBreakdown** | **[String: Int]** | Breakdown of items processed in the last 24 hours by data type Keys are data type names (e.g., \&quot;Glucose\&quot;, \&quot;Treatments\&quot;, \&quot;Food\&quot;) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


