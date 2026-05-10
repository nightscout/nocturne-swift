# V4AdminAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**backfillTriggerBackfill**](V4AdminAPI.md#backfilltriggerbackfill) | **POST** /api/v4/admin/backfill | Trigger a full backfill of legacy entries and treatments into v4 granular tables. This operation is idempotent and safe to re-run. Records are matched by LegacyId to avoid creating duplicates. Only one backfill can run at a time.


# **backfillTriggerBackfill**
```swift
    open class func backfillTriggerBackfill(completion: @escaping (_ data: BackfillResult?, _ error: Error?) -> Void)
```

Trigger a full backfill of legacy entries and treatments into v4 granular tables. This operation is idempotent and safe to re-run. Records are matched by LegacyId to avoid creating duplicates. Only one backfill can run at a time.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import NocturneSDK


// Trigger a full backfill of legacy entries and treatments into v4 granular tables. This operation is idempotent and safe to re-run. Records are matched by LegacyId to avoid creating duplicates. Only one backfill can run at a time.
V4AdminAPI.backfillTriggerBackfill() { (response, error) in
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

[**BackfillResult**](BackfillResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

