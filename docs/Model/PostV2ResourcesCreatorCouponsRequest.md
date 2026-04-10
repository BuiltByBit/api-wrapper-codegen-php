# # PostV2ResourcesCreatorCouponsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Must be &#39;perecent&#39;. |
**discount** | **float** |  |
**label** | **string** | The trailing part of the coupon code (without &#39;{user_id}-&#39;). |
**do_expiry** | **bool** | Whether or not to respect the &#39;expiry_date&#39; field. No expiry date is set otherwise. | [optional]
**expiry_date** | **string** |  | [optional]
**limited_uses** | **bool** | Whether or not to respect the &#39;max_uses&#39; field. No max use limit is set otherwise. | [optional]
**max_uses** | **int** |  | [optional]
**limited_user_uses** | **bool** | Whether or not to respect the &#39;max_per_user_uses&#39; field. No max uses per user limit is set otherwise. | [optional]
**max_per_user_uses** | **int** |  | [optional]
**all_content_types** | **string[]** | If a content type is included, all of the creator&#39;s content (of that type) can be used against this coupon.  Support values include: &#39;resource&#39;, &#39;addon&#39;, and &#39;bundle&#39; | [optional]
**resources** | **string** | A comma-separated list of resource IDs which this coupon can be used against. | [optional]
**addons** | **string** | A comma-separated list of addon IDs which this coupon can be used against. | [optional]
**bundles** | **string** | A comma-separated list of bundle IDs which this coupon can be used against. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
