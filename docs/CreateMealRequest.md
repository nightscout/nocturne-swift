# CreateMealRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the meal occurred. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**insulin** | **Double** | Total insulin amount in units for the meal bolus. | [optional] 
**carbs** | **Double** | Amount of carbohydrates consumed in grams. | [optional] 
**bolusType** | [**BolusType**](BolusType.md) | Bolus delivery pattern (normal, square wave, dual wave, etc.). | [optional] 
**duration** | **Double** | Extended/square bolus duration in minutes. | [optional] 
**absorptionTime** | **Int** | Expected carb absorption duration in minutes. | [optional] 
**carbTime** | **Double** | Minutes from bolus time to expected carb absorption start (pre-bolus offset). | [optional] 
**insulinType** | **String** | Type or brand of insulin used (e.g. \&quot;Humalog\&quot;, \&quot;NovoRapid\&quot;). | [optional] 
**device** | **String** | Identifier of the device that delivered the bolus. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier; required when SyncIdentifier is supplied. | [optional] 
**syncIdentifier** | **String** | Upstream sync identifier for deduplication, paired with DataSource. | [optional] 
**bolusCalculationId** | **String** | Links this meal to the bolus calculation that recommended the insulin dose. | [optional] 
**correlationId** | **String** | Caller-supplied correlation identifier; if omitted, the server generates one. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


