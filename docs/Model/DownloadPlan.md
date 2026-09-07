# # DownloadPlan

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**level** | **string** |  |
**actions** | [**\OpenAPI\Client\Model\DownloadPlanAction[]**](DownloadPlanAction.md) |  | [optional]
**notices** | [**\OpenAPI\Client\Model\DownloadPlanNotice[]**](DownloadPlanNotice.md) |  | [optional]
**unsupported** | **string[]** | A list of features which were unsupported (not passed into the &#39;supported&#39; query paramter) which were needed, resulting in the plan level being downgraded to &#39;manual&#39;. | [optional]
**requires_empty_server** | **string** | Whether the server files must be empty before exeucting the plan steps. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
