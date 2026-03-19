# # PostV2ResourcesDiscoverCartCheckout200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | &#x60;initiated&#x60; - the checkout request was successful and returned a Tebex basket identifier stored in the &#x60;ident&#x60; field.    &#x60;bypassed&#x60; - the checkout was successful but no Tebex basket identifier was generated as it was not needed (perhaps because the buyer used a 100% off coupon). |
**ident** | **string** | The Tebex cart identifier which you can use to redirect to or open a Tebex.js overlay. | [optional]
**url** | **string** | The Tebex checkout link to redirect to if not using Tebex.js (built from the included ident). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
