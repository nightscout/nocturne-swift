# UpsertBolusCalculationRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **Date** | When the bolus calculation was performed. | [optional] 
**utcOffset** | **Int** | UTC offset in minutes at the time of the event, for local-time display. | [optional] 
**device** | **String** | Identifier of the device that ran the calculation. | [optional] 
**app** | **String** | Name of the application that submitted this record. | [optional] 
**dataSource** | **String** | Upstream data source identifier. | [optional] 
**bloodGlucoseInput** | **Double** | Blood glucose value used as input to the calculator. | [optional] 
**bloodGlucoseInputSource** | **String** | Source of the BG input (e.g. \&quot;CGM\&quot;, \&quot;Manual\&quot;, \&quot;Meter\&quot;). | [optional] 
**carbInput** | **Double** | Carbohydrate amount (grams) used as input to the calculator. | [optional] 
**insulinOnBoard** | **Double** | Insulin on board at the time of calculation, in units. | [optional] 
**insulinRecommendation** | **Double** | Total insulin dose recommended by the calculator, in units. | [optional] 
**carbRatio** | **Double** | Insulin-to-carb ratio used in the calculation (grams per unit). Must be strictly positive. | [optional] 
**calculationType** | [**CalculationType**](CalculationType.md) | Type of calculation performed (e.g. correction only, meal only, combined). | [optional] 
**insulinRecommendationForCarbs** | **Double** | Portion of the recommendation attributable to carb coverage. | [optional] 
**insulinProgrammed** | **Double** | Insulin amount actually programmed into the pump. | [optional] 
**enteredInsulin** | **Double** | Insulin amount manually entered by the user. | [optional] 
**splitNow** | **Double** | Percentage of a dual-wave bolus delivered immediately. | [optional] 
**splitExt** | **Double** | Percentage of a dual-wave bolus delivered as extended. | [optional] 
**preBolus** | **Double** | Pre-bolus time in minutes (insulin given before eating). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


