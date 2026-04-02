# # Coupon

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**coupon_id** | **int** |  | [optional]
**user_id** | **int** |  | [optional]
**label** | **string** | This is the code a buyer would enter at checkout. | [optional]
**discount** | **float** | The discount to apply. Either a fixed value, or a decimal percent. Depends on the &#39;percent&#39; field. | [optional]
**percent** | **bool** | If true, the &#39;discount&#39; field represents a decimal percentage.  If false, the &#39;discount&#39; field represents an absolute $ USD value. | [optional]
**all_content_types** | **string[]** | A list of content types for which this coupon code applies to without requiring an entry. Eg. if you created the coupon with the &#39;All resources&#39; option selected, this list will include \&quot;resource\&quot;. | [optional]
**created_at** | **int** | A UNIX timestamp. | [optional]
**expires_at** | **int** | A UNIX timestamp. | [optional]
**max_uses** | **int** |  | [optional]
**max_per_user_uses** | **int** |  | [optional]
**uses** | **int** |  | [optional]
**active** | **bool** | Whether or not the coupon code is active and can still be used at checkout. Accounts for the expiry date if set and the max use limit if set. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
