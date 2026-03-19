# # FilterChoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **string** |  |
**count** | **int** | The dynamic count of relevant resources based on the already-applied filter options.  This may be *null* if we&#39;re unable to provide a count for a specific filter combination. | [optional]
**query_field** | **string** | This is the query string field name to use when attempting to filter on this option. Pass this name as the query string field name and the &#39;option_key&#39; value as the query string field key.    Eg, if &#39;option_key&#39; &#x3D; &#39;action&#39; and &#39;query_field&#39; &#x3D; &#39;rf[genre]&#39;, you should be the query string as &#x60;?rf[genre]&#x3D;action&#x60;. |
**title** | **string** |  |
**selected** | **bool** | Whether or not this option was selected, but only applicable where type &#x3D; &#x60;radio&#x60; or &#x60;checkbox&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
