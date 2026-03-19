# # CartSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**list_price** | **float** | The combined listed price of all items in the cart (ie. the original prices without any discounts applied). |
**list_price_formatted** | **string** | The list price formatted as a string using the given currency.  A list price of 5 would be formatted as &#x60;$5.00&#x60;. |
**final_price** | **float** | The combined final price of all items in the cart (ie. with discounts applied). This is the subtotal the user would pay upon checkout initiation, minus any applicable sales tax. |
**final_price_formatted** | **string** | The final price formatted as a string using the given currency.  A final price of 5 would be formatted as &#x60;$5.00&#x60;. |
**currency** | **string** | The currency code (ISO 4217) of the prices in this summary.  Will be USD for all transactions through BuiltByBit. |
**notice** | **string** | A message to display to the user as a notice regarding their current cart items. We may use this to inform the user that they have a previous pending checkout which is yet to be fulfilled (either because the payment is still pending or because they closed out of the checkout). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
