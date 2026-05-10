# UpsertNoteRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the note was created. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the device that created the note. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier. | [optional] 
**text** | **String** | Note body text (capped at 10,000 characters). | [optional] 
**eventType** | **String** | Nightscout-compatible event type string (capped at 200 characters). | [optional] 
**isAnnouncement** | **Bool** | When true, the note is displayed as a prominent announcement. | [optional] 
**syncIdentifier** | **String** | Upstream sync identifier for deduplication. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


