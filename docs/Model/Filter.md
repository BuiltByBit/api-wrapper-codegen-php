# # Filter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**filter_id** | **string** |  |
**order** | **int** | The display order of this filter. Filters on BuiltByBit are displayed in ascending order of their order value. |
**primary** | **bool** | Whether or not BuiltByBit considers this a primary filter. Primary filters are displayed more prominently. |
**title** | **string** |  |
**type** | **string** | Supported types:    &#39;radio&#39;: a finite choice set (see &#x60;choices&#x60;). You&#39;ll likely want to use the radio HTML tag.    &#39;select&#39;: a finite choice set (see &#x60;choices&#x60;). You&#39;ll likely want to use the select HTML tag.  &#39;text&#39;: user text input. |
**choices** | [**\OpenAPI\Client\Model\FilterChoice[]**](FilterChoice.md) |  | [optional]
**query_field** | **string** |  | [optional]
**value** | **string** | The pass-through value of this filter, only applicable where type &#x3D; &#x60;text&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
