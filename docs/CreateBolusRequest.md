# CreateBolusRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the bolus was delivered. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the device that delivered the bolus (e.g. pump serial number). | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier; required when SyncIdentifier is supplied. | [optional] 
**insulin** | **Double** | Total insulin amount in units. | [optional] 
**programmed** | **Double** | Programmed insulin amount in units (may differ from delivered for interrupted boluses). | [optional] 
**delivered** | **Double** | Actually delivered insulin amount in units. | [optional] 
**bolusType** | [**BolusType**](BolusType.md) | Bolus delivery pattern (normal, square wave, dual wave, etc.). | [optional] 
**kind** | [**BolusKind**](BolusKind.md) | Whether this bolus was manually entered or originated from a pump/loop system. | [optional] 
**automatic** | **Bool** | Whether this bolus was delivered automatically by an APS/loop system. | [optional] 
**duration** | **Double** | Extended/square bolus duration in minutes. | [optional] 
**syncIdentifier** | **String** | Upstream sync identifier for deduplication, paired with DataSource. | [optional] 
**insulinType** | **String** | Type or brand of insulin used (e.g. \&quot;Humalog\&quot;, \&quot;NovoRapid\&quot;). | [optional] 
**patientInsulinId** | **String** | Optional reference to a PatientInsulin. When provided, the server resolves it to a TreatmentInsulinContext snapshot and overwrites InsulinType with the insulin&#39;s name. | [optional] 
**unabsorbed** | **Double** | Insulin on board (unabsorbed) at the time of the bolus, in units. | [optional] 
**bolusCalculationId** | **String** | Links this bolus to the bolus calculation that recommended it. | [optional] 
**apsSnapshotId** | **String** | Links this bolus to the APS decision snapshot that triggered it. | [optional] 
**correlationId** | **String** | Correlation identifier for grouping related events (e.g. a meal bolus and carb intake). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


