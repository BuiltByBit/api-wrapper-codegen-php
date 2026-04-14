# OpenAPI\Client\ResourcesCreatorCouponsApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesCreatorCoupons()**](ResourcesCreatorCouponsApi.md#getV2ResourcesCreatorCoupons) | **GET** /v2/resources/creator/coupons | Fetch a list of your coupons |
| [**getV2ResourcesCreatorCouponsEntries()**](ResourcesCreatorCouponsApi.md#getV2ResourcesCreatorCouponsEntries) | **GET** /v2/resources/creator/coupons/entries | Fetch a list of your coupon entries |
| [**postV2ResourcesCreatorCoupons()**](ResourcesCreatorCouponsApi.md#postV2ResourcesCreatorCoupons) | **POST** /v2/resources/creator/coupons | Create a new coupon |


## `getV2ResourcesCreatorCoupons()`

```php
getV2ResourcesCreatorCoupons($coupon_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorCoupons200Response
```

Fetch a list of your coupons

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorCouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$coupon_ids = NULL; // array | A comma-separated list of coupon IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorCoupons($coupon_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorCouponsApi->getV2ResourcesCreatorCoupons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **coupon_ids** | [**array**](../Model/.md)| A comma-separated list of coupon IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorCoupons200Response**](../Model/GetV2ResourcesCreatorCoupons200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorCouponsEntries()`

```php
getV2ResourcesCreatorCouponsEntries($coupon_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorCouponsEntries200Response
```

Fetch a list of your coupon entries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorCouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$coupon_ids = NULL; // array | A comma-separated list of coupon IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorCouponsEntries($coupon_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorCouponsApi->getV2ResourcesCreatorCouponsEntries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **coupon_ids** | [**array**](../Model/.md)| A comma-separated list of coupon IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorCouponsEntries200Response**](../Model/GetV2ResourcesCreatorCouponsEntries200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesCreatorCoupons()`

```php
postV2ResourcesCreatorCoupons($post_v2_resources_creator_coupons_request): \OpenAPI\Client\Model\PostV2ResourcesCreatorCoupons200Response
```

Create a new coupon

This endpoint is currently limited to percent-based coupons with a maximum discount of 50%.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorCouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_resources_creator_coupons_request = new \OpenAPI\Client\Model\PostV2ResourcesCreatorCouponsRequest(); // \OpenAPI\Client\Model\PostV2ResourcesCreatorCouponsRequest

try {
    $result = $apiInstance->postV2ResourcesCreatorCoupons($post_v2_resources_creator_coupons_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorCouponsApi->postV2ResourcesCreatorCoupons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_creator_coupons_request** | [**\OpenAPI\Client\Model\PostV2ResourcesCreatorCouponsRequest**](../Model/PostV2ResourcesCreatorCouponsRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesCreatorCoupons200Response**](../Model/PostV2ResourcesCreatorCoupons200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
