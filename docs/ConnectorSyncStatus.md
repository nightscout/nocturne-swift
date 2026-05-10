# ConnectorSyncStatus

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connectorId** | **String** | The connector ID (e.g., \&quot;dexcom\&quot;, \&quot;libre\&quot;) | [optional] 
**dataSource** | **String** | The data source name used in the database (e.g., \&quot;dexcom-connector\&quot;) | [optional] 
**latestEntryTimestamp** | **Date** | The timestamp of the latest entry, or null if no entries exist | [optional] 
**oldestEntryTimestamp** | **Date** | The timestamp of the oldest entry, or null if no entries exist | [optional] 
**latestTreatmentTimestamp** | **Date** | The timestamp of the latest treatment, or null if no treatments exist | [optional] 
**oldestTreatmentTimestamp** | **Date** | The timestamp of the oldest treatment, or null if no treatments exist | [optional] 
**hasEntries** | **Bool** | Whether any entries exist for this connector | [optional] 
**hasTreatments** | **Bool** | Whether any treatments exist for this connector | [optional] 
**state** | **String** | Current connector state (Idle, Syncing, BackingOff, Error) | [optional] 
**stateMessage** | **String** | Optional message describing the current state | [optional] 
**isHealthy** | **Bool** | Whether the connector is healthy | [optional] 
**queriedAt** | **Date** | When this status was queried | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


