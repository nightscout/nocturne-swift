# StatisticsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**statisticsAnalyzeGlucoseData**](StatisticsAPI.md#statisticsanalyzeglucosedata) | **POST** /api/v4/Statistics/comprehensive-analytics | Master glucose analytics function that calculates comprehensive metrics
[**statisticsAnalyzeGlucoseDataExtended**](StatisticsAPI.md#statisticsanalyzeglucosedataextended) | **POST** /api/v4/Statistics/extended-analytics | Extended glucose analytics including GMI, GRI, and clinical target assessment
[**statisticsAssessAgainstTargets**](StatisticsAPI.md#statisticsassessagainsttargets) | **POST** /api/v4/Statistics/clinical-assessment | Assess glucose data against clinical targets for a specific population
[**statisticsAssessDataSufficiency**](StatisticsAPI.md#statisticsassessdatasufficiency) | **POST** /api/v4/Statistics/data-sufficiency | Assess data sufficiency for a valid clinical report
[**statisticsCalculateAveragedStats**](StatisticsAPI.md#statisticscalculateaveragedstats) | **POST** /api/v4/Statistics/averaged-stats | Calculate averaged statistics for each hour of the day (0-23)
[**statisticsCalculateBasicStats**](StatisticsAPI.md#statisticscalculatebasicstats) | **POST** /api/v4/Statistics/basic-stats | Calculate basic glucose statistics from provided glucose values
[**statisticsCalculateEstimatedA1C**](StatisticsAPI.md#statisticscalculateestimateda1c) | **GET** /api/v4/Statistics/estimated-a1c/{averageGlucose} | Calculate estimated A1C from average glucose
[**statisticsCalculateGMI**](StatisticsAPI.md#statisticscalculategmi) | **GET** /api/v4/Statistics/gmi/{meanGlucose} | Calculate Glucose Management Indicator (GMI)
[**statisticsCalculateGRI**](StatisticsAPI.md#statisticscalculategri) | **POST** /api/v4/Statistics/gri | Calculate Glycemic Risk Index (GRI) from time in range metrics
[**statisticsCalculateGlucoseDistribution**](StatisticsAPI.md#statisticscalculateglucosedistribution) | **POST** /api/v4/Statistics/glucose-distribution | Calculate glucose distribution across configurable bins
[**statisticsCalculateGlycemicVariability**](StatisticsAPI.md#statisticscalculateglycemicvariability) | **POST** /api/v4/Statistics/glycemic-variability | Calculate comprehensive glycemic variability metrics
[**statisticsCalculateOverallAverages**](StatisticsAPI.md#statisticscalculateoverallaverages) | **POST** /api/v4/Statistics/overall-averages | Calculate overall averages across multiple days
[**statisticsCalculateSiteChangeImpact**](StatisticsAPI.md#statisticscalculatesitechangeimpact) | **POST** /api/v4/Statistics/site-change-impact | Analyze glucose patterns around site changes to identify impact of site age on control
[**statisticsCalculateTimeInRange**](StatisticsAPI.md#statisticscalculatetimeinrange) | **POST** /api/v4/Statistics/time-in-range | Calculate time in range metrics
[**statisticsCalculateTreatmentSummary**](StatisticsAPI.md#statisticscalculatetreatmentsummary) | **POST** /api/v4/Statistics/treatment-summary | Calculate treatment summary for a collection of boluses and carb intakes
[**statisticsCleanTreatmentData**](StatisticsAPI.md#statisticscleantreatmentdata) | **POST** /api/v4/Statistics/clean/treatments | Clean and filter treatment data
[**statisticsFormatCarbDisplay**](StatisticsAPI.md#statisticsformatcarbdisplay) | **GET** /api/v4/Statistics/format/carb/{value} | Format carb value for display
[**statisticsFormatInsulinDisplay**](StatisticsAPI.md#statisticsformatinsulindisplay) | **GET** /api/v4/Statistics/format/insulin/{value} | Format insulin value for display
[**statisticsGetAidSystemMetrics**](StatisticsAPI.md#statisticsgetaidsystemmetrics) | **GET** /api/v4/Statistics/aid-system-metrics | Calculates AID (Automated Insulin Delivery) system metrics for a date range. Uses patient device records to segment the period by algorithm and compute time-weighted metrics via IAidMetricsService.
[**statisticsGetBasalAnalysis**](StatisticsAPI.md#statisticsgetbasalanalysis) | **GET** /api/v4/Statistics/basal-analysis | Calculate comprehensive basal analysis statistics for a date range
[**statisticsGetClinicalTargets**](StatisticsAPI.md#statisticsgetclinicaltargets) | **GET** /api/v4/Statistics/clinical-targets/{population} | Get clinical targets for a specific diabetes population
[**statisticsGetDailyBasalBolusRatios**](StatisticsAPI.md#statisticsgetdailybasalbolusratios) | **GET** /api/v4/Statistics/daily-basal-bolus-ratios | Calculate daily basal/bolus ratio statistics for a date range
[**statisticsGetInsulinDeliveryStatistics**](StatisticsAPI.md#statisticsgetinsulindeliverystatistics) | **GET** /api/v4/Statistics/insulin-delivery-stats | Calculate comprehensive insulin delivery statistics for a date range
[**statisticsGetMultiPeriodStatistics**](StatisticsAPI.md#statisticsgetmultiperiodstatistics) | **GET** /api/v4/Statistics/periods | Gets comprehensive statistics for multiple time periods (1, 3, 7, 30, and 90 days). Fetches sensor glucose, bolus, carb, and temp-basal data from the database for each period, computes GlucoseAnalytics, TreatmentSummary, and InsulinDeliveryStatistics, and caches the result for 5 minutes.
[**statisticsMgdlToMMOL**](StatisticsAPI.md#statisticsmgdltommol) | **GET** /api/v4/Statistics/convert/mgdl-to-mmol/{mgdl} | Convert mg/dL to mmol/L
[**statisticsMmolToMGDL**](StatisticsAPI.md#statisticsmmoltomgdl) | **GET** /api/v4/Statistics/convert/mmol-to-mgdl/{mmol} | Convert mmol/L to mg/dL
[**statisticsValidateTreatmentData**](StatisticsAPI.md#statisticsvalidatetreatmentdata) | **POST** /api/v4/Statistics/validate/treatment | Validate treatment data for completeness and consistency


# **statisticsAnalyzeGlucoseData**
```swift
    open class func statisticsAnalyzeGlucoseData(glucoseAnalyticsRequest: GlucoseAnalyticsRequest, completion: @escaping (_ data: GlucoseAnalytics?, _ error: Error?) -> Void)
```

Master glucose analytics function that calculates comprehensive metrics

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let glucoseAnalyticsRequest = GlucoseAnalyticsRequest(entries: [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")], boluses: [Bolus(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), insulin: 123, programmed: 123, delivered: 123, bolusType: BolusType(), automatic: false, kind: BolusKind(), duration: 123, syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123), unabsorbed: 123, deviceId: "deviceId_example", pumpRecordId: "pumpRecordId_example", bolusCalculationId: "bolusCalculationId_example", apsSnapshotId: "apsSnapshotId_example", additionalProperties: "TODO")], carbIntakes: [CarbIntake(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), carbs: 123, syncIdentifier: "syncIdentifier_example", carbTime: 123, absorptionTime: 123, additionalProperties: "TODO")], config: ExtendedAnalysisConfig(thresholds: GlycemicThresholds(veryLow: 123, low: 123, targetBottom: 123, targetTop: 123, tightTargetBottom: 123, tightTargetTop: 123, high: 123, veryHigh: 123), sensorType: "sensorType_example", includeLoopingMetrics: false, units: "units_example")) // GlucoseAnalyticsRequest | Request containing sensor glucose readings, boluses, carb intakes, and configuration

// Master glucose analytics function that calculates comprehensive metrics
StatisticsAPI.statisticsAnalyzeGlucoseData(glucoseAnalyticsRequest: glucoseAnalyticsRequest) { (response, error) in
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
 **glucoseAnalyticsRequest** | [**GlucoseAnalyticsRequest**](GlucoseAnalyticsRequest.md) | Request containing sensor glucose readings, boluses, carb intakes, and configuration | 

### Return type

[**GlucoseAnalytics**](GlucoseAnalytics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsAnalyzeGlucoseDataExtended**
```swift
    open class func statisticsAnalyzeGlucoseDataExtended(extendedGlucoseAnalyticsRequest: ExtendedGlucoseAnalyticsRequest, completion: @escaping (_ data: ExtendedGlucoseAnalytics?, _ error: Error?) -> Void)
```

Extended glucose analytics including GMI, GRI, and clinical target assessment

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let extendedGlucoseAnalyticsRequest = ExtendedGlucoseAnalyticsRequest(entries: [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")], boluses: [Bolus(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), insulin: 123, programmed: 123, delivered: 123, bolusType: BolusType(), automatic: false, kind: BolusKind(), duration: 123, syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123), unabsorbed: 123, deviceId: "deviceId_example", pumpRecordId: "pumpRecordId_example", bolusCalculationId: "bolusCalculationId_example", apsSnapshotId: "apsSnapshotId_example", additionalProperties: "TODO")], carbIntakes: [CarbIntake(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), carbs: 123, syncIdentifier: "syncIdentifier_example", carbTime: 123, absorptionTime: 123, additionalProperties: "TODO")], population: DiabetesPopulation(), config: ExtendedAnalysisConfig(thresholds: GlycemicThresholds(veryLow: 123, low: 123, targetBottom: 123, targetTop: 123, tightTargetBottom: 123, tightTargetTop: 123, high: 123, veryHigh: 123), sensorType: "sensorType_example", includeLoopingMetrics: false, units: "units_example")) // ExtendedGlucoseAnalyticsRequest | Request containing sensor glucose readings, boluses, carb intakes, population type, and configuration

// Extended glucose analytics including GMI, GRI, and clinical target assessment
StatisticsAPI.statisticsAnalyzeGlucoseDataExtended(extendedGlucoseAnalyticsRequest: extendedGlucoseAnalyticsRequest) { (response, error) in
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
 **extendedGlucoseAnalyticsRequest** | [**ExtendedGlucoseAnalyticsRequest**](ExtendedGlucoseAnalyticsRequest.md) | Request containing sensor glucose readings, boluses, carb intakes, population type, and configuration | 

### Return type

[**ExtendedGlucoseAnalytics**](ExtendedGlucoseAnalytics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsAssessAgainstTargets**
```swift
    open class func statisticsAssessAgainstTargets(clinicalAssessmentRequest: ClinicalAssessmentRequest, completion: @escaping (_ data: ClinicalTargetAssessment?, _ error: Error?) -> Void)
```

Assess glucose data against clinical targets for a specific population

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let clinicalAssessmentRequest = ClinicalAssessmentRequest(analytics: GlucoseAnalytics(basicStats: BasicGlucoseStats(count: 123, mean: 123, median: 123, min: 123, max: 123, standardDeviation: 123, percentiles: GlucosePercentiles(p5: 123, p10: 123, p25: 123, p50: 123, p75: 123, p90: 123, p95: 123)), timeInRange: TimeInRangeMetrics(percentages: TimeInRangePercentages(veryLow: 123, low: 123, target: 123, tightTarget: 123, high: 123, veryHigh: 123), durations: TimeInRangeDurations(veryLow: 123, low: 123, target: 123, tightTarget: 123, high: 123, veryHigh: 123), episodes: TimeInRangeEpisodes(veryLow: 123, low: 123, high: 123, veryHigh: 123), rangeStats: TimeInRangeDetailedStats(low: PeriodMetrics(periodName: "periodName_example", startHour: 123, endHour: 123, readingCount: 123, mean: 123, median: 123, standardDeviation: 123, coefficientOfVariation: 123, timeInRange: 123, timeBelowRange: 123, timeVeryLow: 123, timeAboveRange: 123, timeVeryHigh: 123, hypoglycemiaEvents: 123, hyperglycemiaEvents: 123, min: 123, max: 123), target: nil, high: nil)), glycemicVariability: GlycemicVariability(coefficientOfVariation: 123, standardDeviation: 123, meanAmplitudeGlycemicExcursions: 123, continuousOverlappingNetGlycemicAction: 123, averageDailyRiskRange: 123, labilityIndex: 123, jIndex: 123, highBloodGlucoseIndex: 123, lowBloodGlucoseIndex: 123, glycemicVariabilityIndex: 123, patientGlycemicStatus: 123, estimatedA1c: 123, gmi: GlucoseManagementIndicator(value: 123, meanGlucose: 123, interpretation: GlucoseManagementIndicatorLevel(), reliability: StatisticReliability(meetsReliabilityCriteria: false, daysOfData: 123, recommendedMinimumDays: 123, readingCount: 123)), meanTotalDailyChange: 123, timeInFluctuation: 123), dataQuality: DataQuality(totalReadings: 123, missingReadings: 123, dataCompleteness: 123, cgmActivePercent: 123, gapAnalysis: GapAnalysis(gaps: [DataGap(start: 123, end: 123, duration: 123)], longestGap: 123, averageGap: 123), noiseLevel: 123, calibrationEvents: 123, sensorWarmups: 123), reliability: nil, time: AnalysisTime(start: 123, end: 123, timeOfAnalysis: 123), clinicalAssessment: ClinicalTargetAssessment(population: DiabetesPopulation(), targets: ClinicalTargets(targetTIR: 123, maxTBR: 123, maxTBRVeryLow: 123, maxTAR: 123, maxTARVeryHigh: 123, targetCV: 123, targetLow: 123, targetHigh: 123), tirAssessment: TargetAssessment(metricName: "metricName_example", currentValue: 123, targetValue: 123, isMaximumTarget: false, status: TargetStatus(), differenceFromTarget: 123, progressPercentage: 123), tbrAssessment: nil, veryLowAssessment: nil, tarAssessment: nil, veryHighAssessment: nil, cvAssessment: nil, targetsMet: 123, totalTargets: 123, overallAssessment: ClinicalAssessmentLevel(), actionableInsights: [LocalizedInsight(key: InsightKey(), context: "TODO")], priorityAreas: [nil], strengths: [nil])), population: nil) // ClinicalAssessmentRequest | Request containing analytics and population type

// Assess glucose data against clinical targets for a specific population
StatisticsAPI.statisticsAssessAgainstTargets(clinicalAssessmentRequest: clinicalAssessmentRequest) { (response, error) in
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
 **clinicalAssessmentRequest** | [**ClinicalAssessmentRequest**](ClinicalAssessmentRequest.md) | Request containing analytics and population type | 

### Return type

[**ClinicalTargetAssessment**](ClinicalTargetAssessment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsAssessDataSufficiency**
```swift
    open class func statisticsAssessDataSufficiency(dataSufficiencyRequest: DataSufficiencyRequest, completion: @escaping (_ data: DataSufficiencyAssessment?, _ error: Error?) -> Void)
```

Assess data sufficiency for a valid clinical report

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let dataSufficiencyRequest = DataSufficiencyRequest(entries: [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")], days: 123, expectedReadingsPerDay: 123) // DataSufficiencyRequest | Request containing entries and optional period settings

// Assess data sufficiency for a valid clinical report
StatisticsAPI.statisticsAssessDataSufficiency(dataSufficiencyRequest: dataSufficiencyRequest) { (response, error) in
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
 **dataSufficiencyRequest** | [**DataSufficiencyRequest**](DataSufficiencyRequest.md) | Request containing entries and optional period settings | 

### Return type

[**DataSufficiencyAssessment**](DataSufficiencyAssessment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateAveragedStats**
```swift
    open class func statisticsCalculateAveragedStats(sensorGlucose: [SensorGlucose], completion: @escaping (_ data: [AveragedStats]?, _ error: Error?) -> Void)
```

Calculate averaged statistics for each hour of the day (0-23)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let sensorGlucose = [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")] // [SensorGlucose] | Array of sensor glucose readings

// Calculate averaged statistics for each hour of the day (0-23)
StatisticsAPI.statisticsCalculateAveragedStats(sensorGlucose: sensorGlucose) { (response, error) in
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
 **sensorGlucose** | [**[SensorGlucose]**](SensorGlucose.md) | Array of sensor glucose readings | 

### Return type

[**[AveragedStats]**](AveragedStats.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateBasicStats**
```swift
    open class func statisticsCalculateBasicStats(requestBody: [Double], completion: @escaping (_ data: BasicGlucoseStats?, _ error: Error?) -> Void)
```

Calculate basic glucose statistics from provided glucose values

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let requestBody = [123] // [Double] | Array of glucose values in mg/dL

// Calculate basic glucose statistics from provided glucose values
StatisticsAPI.statisticsCalculateBasicStats(requestBody: requestBody) { (response, error) in
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
 **requestBody** | [**[Double]**](Double.md) | Array of glucose values in mg/dL | 

### Return type

[**BasicGlucoseStats**](BasicGlucoseStats.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateEstimatedA1C**
```swift
    open class func statisticsCalculateEstimatedA1C(averageGlucose: Double, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Calculate estimated A1C from average glucose

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let averageGlucose = 987 // Double | Average glucose in mg/dL

// Calculate estimated A1C from average glucose
StatisticsAPI.statisticsCalculateEstimatedA1C(averageGlucose: averageGlucose) { (response, error) in
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
 **averageGlucose** | **Double** | Average glucose in mg/dL | 

### Return type

**Double**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateGMI**
```swift
    open class func statisticsCalculateGMI(meanGlucose: Double, completion: @escaping (_ data: GlucoseManagementIndicator?, _ error: Error?) -> Void)
```

Calculate Glucose Management Indicator (GMI)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let meanGlucose = 987 // Double | Mean glucose in mg/dL

// Calculate Glucose Management Indicator (GMI)
StatisticsAPI.statisticsCalculateGMI(meanGlucose: meanGlucose) { (response, error) in
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
 **meanGlucose** | **Double** | Mean glucose in mg/dL | 

### Return type

[**GlucoseManagementIndicator**](GlucoseManagementIndicator.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateGRI**
```swift
    open class func statisticsCalculateGRI(timeInRangeMetrics: TimeInRangeMetrics, completion: @escaping (_ data: GlycemicRiskIndex?, _ error: Error?) -> Void)
```

Calculate Glycemic Risk Index (GRI) from time in range metrics

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let timeInRangeMetrics = TimeInRangeMetrics(percentages: TimeInRangePercentages(veryLow: 123, low: 123, target: 123, tightTarget: 123, high: 123, veryHigh: 123), durations: TimeInRangeDurations(veryLow: 123, low: 123, target: 123, tightTarget: 123, high: 123, veryHigh: 123), episodes: TimeInRangeEpisodes(veryLow: 123, low: 123, high: 123, veryHigh: 123), rangeStats: TimeInRangeDetailedStats(low: PeriodMetrics(periodName: "periodName_example", startHour: 123, endHour: 123, readingCount: 123, mean: 123, median: 123, standardDeviation: 123, coefficientOfVariation: 123, timeInRange: 123, timeBelowRange: 123, timeVeryLow: 123, timeAboveRange: 123, timeVeryHigh: 123, hypoglycemiaEvents: 123, hyperglycemiaEvents: 123, min: 123, max: 123), target: nil, high: nil)) // TimeInRangeMetrics | Time in range metrics

// Calculate Glycemic Risk Index (GRI) from time in range metrics
StatisticsAPI.statisticsCalculateGRI(timeInRangeMetrics: timeInRangeMetrics) { (response, error) in
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
 **timeInRangeMetrics** | [**TimeInRangeMetrics**](TimeInRangeMetrics.md) | Time in range metrics | 

### Return type

[**GlycemicRiskIndex**](GlycemicRiskIndex.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateGlucoseDistribution**
```swift
    open class func statisticsCalculateGlucoseDistribution(glucoseDistributionRequest: GlucoseDistributionRequest, completion: @escaping (_ data: [DistributionDataPoint]?, _ error: Error?) -> Void)
```

Calculate glucose distribution across configurable bins

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let glucoseDistributionRequest = GlucoseDistributionRequest(entries: [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")], bins: [DistributionBin(range: "range_example", min: 123, max: 123)]) // GlucoseDistributionRequest | Request containing entries and optional bins

// Calculate glucose distribution across configurable bins
StatisticsAPI.statisticsCalculateGlucoseDistribution(glucoseDistributionRequest: glucoseDistributionRequest) { (response, error) in
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
 **glucoseDistributionRequest** | [**GlucoseDistributionRequest**](GlucoseDistributionRequest.md) | Request containing entries and optional bins | 

### Return type

[**[DistributionDataPoint]**](DistributionDataPoint.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateGlycemicVariability**
```swift
    open class func statisticsCalculateGlycemicVariability(glycemicVariabilityRequest: GlycemicVariabilityRequest, completion: @escaping (_ data: GlycemicVariability?, _ error: Error?) -> Void)
```

Calculate comprehensive glycemic variability metrics

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let glycemicVariabilityRequest = GlycemicVariabilityRequest(values: [123], entries: [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")]) // GlycemicVariabilityRequest | Request containing glucose values and entries

// Calculate comprehensive glycemic variability metrics
StatisticsAPI.statisticsCalculateGlycemicVariability(glycemicVariabilityRequest: glycemicVariabilityRequest) { (response, error) in
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
 **glycemicVariabilityRequest** | [**GlycemicVariabilityRequest**](GlycemicVariabilityRequest.md) | Request containing glucose values and entries | 

### Return type

[**GlycemicVariability**](GlycemicVariability.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateOverallAverages**
```swift
    open class func statisticsCalculateOverallAverages(dayData: [DayData], completion: @escaping (_ data: OverallAverages?, _ error: Error?) -> Void)
```

Calculate overall averages across multiple days

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let dayData = [DayData(date: "date_example", treatments: [Treatment(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, identifier: "identifier_example", srvModified: 123, srvCreated: 123, eventType: "eventType_example", reason: "reason_example", glucose: 123, glucoseType: "glucoseType_example", carbs: 123, insulin: 123, protein: 123, fat: 123, foodType: "foodType_example", units: "units_example", duration: 123, percent: 123, absolute: 123, notes: "notes_example", enteredBy: "enteredBy_example", targetTop: 123, targetBottom: 123, profile: "profile_example", split: "split_example", date: 123, carbTime: 123, boluscalc: "TODO", timestamp: "timestamp_example", cuttedby: "cuttedby_example", cutting: "cutting_example", eventTime: "eventTime_example", preBolus: 123, rate: 123, mgdl: 123, mmol: 123, endmills: 123, durationType: "durationType_example", isAnnouncement: false, profileJson: "profileJson_example", endprofile: "endprofile_example", insulinNeedsScaleFactor: 123, absorptionTime: 123, enteredinsulin: 123, splitNow: 123, splitExt: 123, status: "status_example", relative: 123, CR: 123, NSCLIENT_ID: "NSCLIENT_ID_example", first: false, end: false, circadianPercentageProfile: false, percentage: 123, timeshift: 123, transmitterId: "transmitterId_example", remoteCarbs: 123, remoteAbsorption: 123, remoteBolus: 123, reasonDisplay: "reasonDisplay_example", otp: "otp_example", syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", automatic: false, temp: "temp_example", amount: 123, programmed: 123, unabsorbed: 123, type: "type_example", bolusType: "bolusType_example", dataSource: "dataSource_example", insulinRecommendationForCarbs: 123, insulinRecommendationForCorrection: 123, insulinProgrammed: 123, insulinDelivered: 123, insulinOnBoard: 123, bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", calculationType: CalculationType2(), durationInMilliseconds: 123, pumpId: 123, pumpSerial: "pumpSerial_example", pumpType: "pumpType_example", endId: 123, isValid: false, isReadOnly: false, isBasalInsulin: false, bolusCalculatorResult: "bolusCalculatorResult_example", originalDuration: 123, originalProfileName: "originalProfileName_example", originalPercentage: 123, originalTimeshift: 123, originalCustomizedName: "originalCustomizedName_example", originalEnd: 123, canonicalId: "canonicalId_example", dbId: "dbId_example", sources: ["sources_example"], insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123))], treatmentSummary: TreatmentSummary(totals: TreatmentTotals(food: FoodTotals(carbs: 123, protein: 123, fat: 123), insulin: InsulinTotals(bolus: 123, basal: 123, scheduledBasal: 123, additionalBasal: 123)), treatmentCount: 123, carbToInsulinRatio: 123), timeInRanges: TimeInRangeMetrics(percentages: TimeInRangePercentages(veryLow: 123, low: 123, target: 123, tightTarget: 123, high: 123, veryHigh: 123), durations: TimeInRangeDurations(veryLow: 123, low: 123, target: 123, tightTarget: 123, high: 123, veryHigh: 123), episodes: TimeInRangeEpisodes(veryLow: 123, low: 123, high: 123, veryHigh: 123), rangeStats: TimeInRangeDetailedStats(low: PeriodMetrics(periodName: "periodName_example", startHour: 123, endHour: 123, readingCount: 123, mean: 123, median: 123, standardDeviation: 123, coefficientOfVariation: 123, timeInRange: 123, timeBelowRange: 123, timeVeryLow: 123, timeAboveRange: 123, timeVeryHigh: 123, hypoglycemiaEvents: 123, hyperglycemiaEvents: 123, min: 123, max: 123), target: nil, high: nil)))] // [DayData] | Array of daily data points

// Calculate overall averages across multiple days
StatisticsAPI.statisticsCalculateOverallAverages(dayData: dayData) { (response, error) in
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
 **dayData** | [**[DayData]**](DayData.md) | Array of daily data points | 

### Return type

[**OverallAverages**](OverallAverages.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateSiteChangeImpact**
```swift
    open class func statisticsCalculateSiteChangeImpact(siteChangeImpactRequest: SiteChangeImpactRequest, completion: @escaping (_ data: SiteChangeImpactAnalysis?, _ error: Error?) -> Void)
```

Analyze glucose patterns around site changes to identify impact of site age on control

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let siteChangeImpactRequest = SiteChangeImpactRequest(entries: [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")], deviceEvents: [DeviceEvent(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), eventType: DeviceEventType(), notes: "notes_example", syncIdentifier: "syncIdentifier_example", additionalProperties: "TODO")], hoursBeforeChange: 123, hoursAfterChange: 123, bucketSizeMinutes: 123) // SiteChangeImpactRequest | Request containing sensor glucose readings, device events, and analysis parameters

// Analyze glucose patterns around site changes to identify impact of site age on control
StatisticsAPI.statisticsCalculateSiteChangeImpact(siteChangeImpactRequest: siteChangeImpactRequest) { (response, error) in
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
 **siteChangeImpactRequest** | [**SiteChangeImpactRequest**](SiteChangeImpactRequest.md) | Request containing sensor glucose readings, device events, and analysis parameters | 

### Return type

[**SiteChangeImpactAnalysis**](SiteChangeImpactAnalysis.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateTimeInRange**
```swift
    open class func statisticsCalculateTimeInRange(timeInRangeRequest: TimeInRangeRequest, completion: @escaping (_ data: TimeInRangeMetrics?, _ error: Error?) -> Void)
```

Calculate time in range metrics

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let timeInRangeRequest = TimeInRangeRequest(entries: [SensorGlucose(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", patientDeviceId: "patientDeviceId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), mgdl: 123, mmol: 123, direction: GlucoseDirection(), trend: GlucoseTrend(), trendRate: 123, noise: 123, filtered: 123, unfiltered: 123, delta: 123, glucoseProcessing: GlucoseProcessing(), smoothedMgdl: 123, smoothedMmol: 123, unsmoothedMgdl: 123, unsmoothedMmol: 123, additionalProperties: "TODO")], thresholds: GlycemicThresholds(veryLow: 123, low: 123, targetBottom: 123, targetTop: 123, tightTargetBottom: 123, tightTargetTop: 123, high: 123, veryHigh: 123)) // TimeInRangeRequest | Request containing entries and optional thresholds

// Calculate time in range metrics
StatisticsAPI.statisticsCalculateTimeInRange(timeInRangeRequest: timeInRangeRequest) { (response, error) in
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
 **timeInRangeRequest** | [**TimeInRangeRequest**](TimeInRangeRequest.md) | Request containing entries and optional thresholds | 

### Return type

[**TimeInRangeMetrics**](TimeInRangeMetrics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCalculateTreatmentSummary**
```swift
    open class func statisticsCalculateTreatmentSummary(treatmentSummaryRequest: TreatmentSummaryRequest, completion: @escaping (_ data: TreatmentSummary?, _ error: Error?) -> Void)
```

Calculate treatment summary for a collection of boluses and carb intakes

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let treatmentSummaryRequest = TreatmentSummaryRequest(boluses: [Bolus(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), insulin: 123, programmed: 123, delivered: 123, bolusType: BolusType(), automatic: false, kind: BolusKind(), duration: 123, syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123), unabsorbed: 123, deviceId: "deviceId_example", pumpRecordId: "pumpRecordId_example", bolusCalculationId: "bolusCalculationId_example", apsSnapshotId: "apsSnapshotId_example", additionalProperties: "TODO")], carbIntakes: [CarbIntake(id: "id_example", timestamp: Date(), mills: 123, utcOffset: 123, device: "device_example", app: "app_example", dataSource: "dataSource_example", correlationId: "correlationId_example", legacyId: "legacyId_example", createdAt: Date(), modifiedAt: Date(), carbs: 123, syncIdentifier: "syncIdentifier_example", carbTime: 123, absorptionTime: 123, additionalProperties: "TODO")]) // TreatmentSummaryRequest | Request containing boluses and carb intakes

// Calculate treatment summary for a collection of boluses and carb intakes
StatisticsAPI.statisticsCalculateTreatmentSummary(treatmentSummaryRequest: treatmentSummaryRequest) { (response, error) in
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
 **treatmentSummaryRequest** | [**TreatmentSummaryRequest**](TreatmentSummaryRequest.md) | Request containing boluses and carb intakes | 

### Return type

[**TreatmentSummary**](TreatmentSummary.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsCleanTreatmentData**
```swift
    open class func statisticsCleanTreatmentData(treatment: [Treatment], completion: @escaping (_ data: [Treatment]?, _ error: Error?) -> Void)
```

Clean and filter treatment data

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let treatment = [Treatment(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, identifier: "identifier_example", srvModified: 123, srvCreated: 123, eventType: "eventType_example", reason: "reason_example", glucose: 123, glucoseType: "glucoseType_example", carbs: 123, insulin: 123, protein: 123, fat: 123, foodType: "foodType_example", units: "units_example", duration: 123, percent: 123, absolute: 123, notes: "notes_example", enteredBy: "enteredBy_example", targetTop: 123, targetBottom: 123, profile: "profile_example", split: "split_example", date: 123, carbTime: 123, boluscalc: "TODO", timestamp: "timestamp_example", cuttedby: "cuttedby_example", cutting: "cutting_example", eventTime: "eventTime_example", preBolus: 123, rate: 123, mgdl: 123, mmol: 123, endmills: 123, durationType: "durationType_example", isAnnouncement: false, profileJson: "profileJson_example", endprofile: "endprofile_example", insulinNeedsScaleFactor: 123, absorptionTime: 123, enteredinsulin: 123, splitNow: 123, splitExt: 123, status: "status_example", relative: 123, CR: 123, NSCLIENT_ID: "NSCLIENT_ID_example", first: false, end: false, circadianPercentageProfile: false, percentage: 123, timeshift: 123, transmitterId: "transmitterId_example", remoteCarbs: 123, remoteAbsorption: 123, remoteBolus: 123, reasonDisplay: "reasonDisplay_example", otp: "otp_example", syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", automatic: false, temp: "temp_example", amount: 123, programmed: 123, unabsorbed: 123, type: "type_example", bolusType: "bolusType_example", dataSource: "dataSource_example", insulinRecommendationForCarbs: 123, insulinRecommendationForCorrection: 123, insulinProgrammed: 123, insulinDelivered: 123, insulinOnBoard: 123, bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", calculationType: CalculationType2(), durationInMilliseconds: 123, pumpId: 123, pumpSerial: "pumpSerial_example", pumpType: "pumpType_example", endId: 123, isValid: false, isReadOnly: false, isBasalInsulin: false, bolusCalculatorResult: "bolusCalculatorResult_example", originalDuration: 123, originalProfileName: "originalProfileName_example", originalPercentage: 123, originalTimeshift: 123, originalCustomizedName: "originalCustomizedName_example", originalEnd: 123, canonicalId: "canonicalId_example", dbId: "dbId_example", sources: ["sources_example"], insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123))] // [Treatment] | Array of treatments to clean

// Clean and filter treatment data
StatisticsAPI.statisticsCleanTreatmentData(treatment: treatment) { (response, error) in
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
 **treatment** | [**[Treatment]**](Treatment.md) | Array of treatments to clean | 

### Return type

[**[Treatment]**](Treatment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsFormatCarbDisplay**
```swift
    open class func statisticsFormatCarbDisplay(value: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Format carb value for display

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let value = 987 // Double | Carb value

// Format carb value for display
StatisticsAPI.statisticsFormatCarbDisplay(value: value) { (response, error) in
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
 **value** | **Double** | Carb value | 

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsFormatInsulinDisplay**
```swift
    open class func statisticsFormatInsulinDisplay(value: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Format insulin value for display

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let value = 987 // Double | Insulin value

// Format insulin value for display
StatisticsAPI.statisticsFormatInsulinDisplay(value: value) { (response, error) in
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
 **value** | **Double** | Insulin value | 

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsGetAidSystemMetrics**
```swift
    open class func statisticsGetAidSystemMetrics(startDate: Date? = nil, endDate: Date? = nil, completion: @escaping (_ data: AidSystemMetrics?, _ error: Error?) -> Void)
```

Calculates AID (Automated Insulin Delivery) system metrics for a date range. Uses patient device records to segment the period by algorithm and compute time-weighted metrics via IAidMetricsService.

Fetches APS snapshots, temp basals, device events, glucose readings, and target-range schedules from their respective repositories. CGM metrics are derived from AnalyzeGlucoseData. Target range is optional; the method continues without it if the repository throws.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startDate = Date() // Date | Inclusive start of the analysis period (UTC). (optional)
let endDate = Date() // Date | Inclusive end of the analysis period (UTC). (optional)

// Calculates AID (Automated Insulin Delivery) system metrics for a date range. Uses patient device records to segment the period by algorithm and compute time-weighted metrics via IAidMetricsService.
StatisticsAPI.statisticsGetAidSystemMetrics(startDate: startDate, endDate: endDate) { (response, error) in
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
 **startDate** | **Date** | Inclusive start of the analysis period (UTC). | [optional] 
 **endDate** | **Date** | Inclusive end of the analysis period (UTC). | [optional] 

### Return type

[**AidSystemMetrics**](AidSystemMetrics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsGetBasalAnalysis**
```swift
    open class func statisticsGetBasalAnalysis(startDate: Date? = nil, endDate: Date? = nil, completion: @escaping (_ data: BasalAnalysisResponse?, _ error: Error?) -> Void)
```

Calculate comprehensive basal analysis statistics for a date range

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startDate = Date() // Date | Start date of the analysis period (optional)
let endDate = Date() // Date | End date of the analysis period (optional)

// Calculate comprehensive basal analysis statistics for a date range
StatisticsAPI.statisticsGetBasalAnalysis(startDate: startDate, endDate: endDate) { (response, error) in
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
 **startDate** | **Date** | Start date of the analysis period | [optional] 
 **endDate** | **Date** | End date of the analysis period | [optional] 

### Return type

[**BasalAnalysisResponse**](BasalAnalysisResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsGetClinicalTargets**
```swift
    open class func statisticsGetClinicalTargets(population: DiabetesPopulation, completion: @escaping (_ data: ClinicalTargets?, _ error: Error?) -> Void)
```

Get clinical targets for a specific diabetes population

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let population = DiabetesPopulation() // DiabetesPopulation | Population type (Type1Adult, Type2Adult, Elderly, Pregnancy, etc.)

// Get clinical targets for a specific diabetes population
StatisticsAPI.statisticsGetClinicalTargets(population: population) { (response, error) in
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
 **population** | [**DiabetesPopulation**](.md) | Population type (Type1Adult, Type2Adult, Elderly, Pregnancy, etc.) | 

### Return type

[**ClinicalTargets**](ClinicalTargets.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsGetDailyBasalBolusRatios**
```swift
    open class func statisticsGetDailyBasalBolusRatios(startDate: Date? = nil, endDate: Date? = nil, completion: @escaping (_ data: DailyBasalBolusRatioResponse?, _ error: Error?) -> Void)
```

Calculate daily basal/bolus ratio statistics for a date range

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startDate = Date() // Date | Start date of the analysis period (optional)
let endDate = Date() // Date | End date of the analysis period (optional)

// Calculate daily basal/bolus ratio statistics for a date range
StatisticsAPI.statisticsGetDailyBasalBolusRatios(startDate: startDate, endDate: endDate) { (response, error) in
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
 **startDate** | **Date** | Start date of the analysis period | [optional] 
 **endDate** | **Date** | End date of the analysis period | [optional] 

### Return type

[**DailyBasalBolusRatioResponse**](DailyBasalBolusRatioResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsGetInsulinDeliveryStatistics**
```swift
    open class func statisticsGetInsulinDeliveryStatistics(startDate: Date? = nil, endDate: Date? = nil, completion: @escaping (_ data: InsulinDeliveryStatistics?, _ error: Error?) -> Void)
```

Calculate comprehensive insulin delivery statistics for a date range

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let startDate = Date() // Date | Start date of the analysis period (optional)
let endDate = Date() // Date | End date of the analysis period (optional)

// Calculate comprehensive insulin delivery statistics for a date range
StatisticsAPI.statisticsGetInsulinDeliveryStatistics(startDate: startDate, endDate: endDate) { (response, error) in
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
 **startDate** | **Date** | Start date of the analysis period | [optional] 
 **endDate** | **Date** | End date of the analysis period | [optional] 

### Return type

[**InsulinDeliveryStatistics**](InsulinDeliveryStatistics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsGetMultiPeriodStatistics**
```swift
    open class func statisticsGetMultiPeriodStatistics(completion: @escaping (_ data: MultiPeriodStatistics?, _ error: Error?) -> Void)
```

Gets comprehensive statistics for multiple time periods (1, 3, 7, 30, and 90 days). Fetches sensor glucose, bolus, carb, and temp-basal data from the database for each period, computes GlucoseAnalytics, TreatmentSummary, and InsulinDeliveryStatistics, and caches the result for 5 minutes.

When no TempBasal or algorithm bolus records are found but a profile is loaded, the method falls back to computing scheduled basal from the active profile schedule via IBasalRateResolver. GMI reliability is assessed per-period using context-appropriate recommended-day minimums (e.g., 1-day periods cannot require 14 days of data).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Gets comprehensive statistics for multiple time periods (1, 3, 7, 30, and 90 days). Fetches sensor glucose, bolus, carb, and temp-basal data from the database for each period, computes GlucoseAnalytics, TreatmentSummary, and InsulinDeliveryStatistics, and caches the result for 5 minutes.
StatisticsAPI.statisticsGetMultiPeriodStatistics() { (response, error) in
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

[**MultiPeriodStatistics**](MultiPeriodStatistics.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsMgdlToMMOL**
```swift
    open class func statisticsMgdlToMMOL(mgdl: Double, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Convert mg/dL to mmol/L

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let mgdl = 987 // Double | Glucose value in mg/dL

// Convert mg/dL to mmol/L
StatisticsAPI.statisticsMgdlToMMOL(mgdl: mgdl) { (response, error) in
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
 **mgdl** | **Double** | Glucose value in mg/dL | 

### Return type

**Double**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsMmolToMGDL**
```swift
    open class func statisticsMmolToMGDL(mmol: Double, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Convert mmol/L to mg/dL

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let mmol = 987 // Double | Glucose value in mmol/L

// Convert mmol/L to mg/dL
StatisticsAPI.statisticsMmolToMGDL(mmol: mmol) { (response, error) in
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
 **mmol** | **Double** | Glucose value in mmol/L | 

### Return type

**Double**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **statisticsValidateTreatmentData**
```swift
    open class func statisticsValidateTreatmentData(treatment: Treatment, completion: @escaping (_ data: Bool?, _ error: Error?) -> Void)
```

Validate treatment data for completeness and consistency

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK

let treatment = Treatment(id: "id_example", createdAt: "createdAt_example", mills: 123, utcOffset: 123, identifier: "identifier_example", srvModified: 123, srvCreated: 123, eventType: "eventType_example", reason: "reason_example", glucose: 123, glucoseType: "glucoseType_example", carbs: 123, insulin: 123, protein: 123, fat: 123, foodType: "foodType_example", units: "units_example", duration: 123, percent: 123, absolute: 123, notes: "notes_example", enteredBy: "enteredBy_example", targetTop: 123, targetBottom: 123, profile: "profile_example", split: "split_example", date: 123, carbTime: 123, boluscalc: "TODO", timestamp: "timestamp_example", cuttedby: "cuttedby_example", cutting: "cutting_example", eventTime: "eventTime_example", preBolus: 123, rate: 123, mgdl: 123, mmol: 123, endmills: 123, durationType: "durationType_example", isAnnouncement: false, profileJson: "profileJson_example", endprofile: "endprofile_example", insulinNeedsScaleFactor: 123, absorptionTime: 123, enteredinsulin: 123, splitNow: 123, splitExt: 123, status: "status_example", relative: 123, CR: 123, NSCLIENT_ID: "NSCLIENT_ID_example", first: false, end: false, circadianPercentageProfile: false, percentage: 123, timeshift: 123, transmitterId: "transmitterId_example", remoteCarbs: 123, remoteAbsorption: 123, remoteBolus: 123, reasonDisplay: "reasonDisplay_example", otp: "otp_example", syncIdentifier: "syncIdentifier_example", insulinType: "insulinType_example", automatic: false, temp: "temp_example", amount: 123, programmed: 123, unabsorbed: 123, type: "type_example", bolusType: "bolusType_example", dataSource: "dataSource_example", insulinRecommendationForCarbs: 123, insulinRecommendationForCorrection: 123, insulinProgrammed: 123, insulinDelivered: 123, insulinOnBoard: 123, bloodGlucoseInput: 123, bloodGlucoseInputSource: "bloodGlucoseInputSource_example", calculationType: CalculationType2(), durationInMilliseconds: 123, pumpId: 123, pumpSerial: "pumpSerial_example", pumpType: "pumpType_example", endId: 123, isValid: false, isReadOnly: false, isBasalInsulin: false, bolusCalculatorResult: "bolusCalculatorResult_example", originalDuration: 123, originalProfileName: "originalProfileName_example", originalPercentage: 123, originalTimeshift: 123, originalCustomizedName: "originalCustomizedName_example", originalEnd: 123, canonicalId: "canonicalId_example", dbId: "dbId_example", sources: ["sources_example"], insulinContext: TreatmentInsulinContext(patientInsulinId: "patientInsulinId_example", insulinName: "insulinName_example", dia: 123, peak: 123, curve: "curve_example", concentration: 123)) // Treatment | Treatment to validate

// Validate treatment data for completeness and consistency
StatisticsAPI.statisticsValidateTreatmentData(treatment: treatment) { (response, error) in
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
 **treatment** | [**Treatment**](Treatment.md) | Treatment to validate | 

### Return type

**Bool**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

