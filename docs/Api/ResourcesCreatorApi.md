# OpenAPI\Client\ResourcesCreatorApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesCreatorAddons()**](ResourcesCreatorApi.md#getV2ResourcesCreatorAddons) | **GET** /v2/resources/creator/addons | Fetch a list of your resources&#39; addons |
| [**getV2ResourcesCreatorBundles()**](ResourcesCreatorApi.md#getV2ResourcesCreatorBundles) | **GET** /v2/resources/creator/bundles | Fetch a list of your bundles |
| [**getV2ResourcesCreatorCoupons()**](ResourcesCreatorApi.md#getV2ResourcesCreatorCoupons) | **GET** /v2/resources/creator/coupons | Fetch a list of your coupons |
| [**getV2ResourcesCreatorLicenses()**](ResourcesCreatorApi.md#getV2ResourcesCreatorLicenses) | **GET** /v2/resources/creator/licenses | Fetch a list of your resources&#39; licenses |
| [**getV2ResourcesCreatorPurchases()**](ResourcesCreatorApi.md#getV2ResourcesCreatorPurchases) | **GET** /v2/resources/creator/purchases | Fetch a list of your resources&#39; purchases |
| [**getV2ResourcesCreatorResources()**](ResourcesCreatorApi.md#getV2ResourcesCreatorResources) | **GET** /v2/resources/creator/resources | Fetch a list of your resources |
| [**getV2ResourcesCreatorReviews()**](ResourcesCreatorApi.md#getV2ResourcesCreatorReviews) | **GET** /v2/resources/creator/reviews | Fetch a list of your resources&#39; reviews |
| [**getV2ResourcesCreatorSaleEvents()**](ResourcesCreatorApi.md#getV2ResourcesCreatorSaleEvents) | **GET** /v2/resources/creator/sale-events | Fetch a list of your sale events |
| [**getV2ResourcesCreatorStores()**](ResourcesCreatorApi.md#getV2ResourcesCreatorStores) | **GET** /v2/resources/creator/stores | Fetch a list of your stores |
| [**getV2ResourcesCreatorUpdates()**](ResourcesCreatorApi.md#getV2ResourcesCreatorUpdates) | **GET** /v2/resources/creator/updates | Fetch a list of your resource&#39;s updates |
| [**getV2ResourcesCreatorVersions()**](ResourcesCreatorApi.md#getV2ResourcesCreatorVersions) | **GET** /v2/resources/creator/versions | Fetch a list of your resources&#39; versions |
| [**postV2ResourcesCreatorUpdate()**](ResourcesCreatorApi.md#postV2ResourcesCreatorUpdate) | **POST** /v2/resources/creator/update | Post a resource update |


## `getV2ResourcesCreatorAddons()`

```php
getV2ResourcesCreatorAddons($resource_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorAddons200Response
```

Fetch a list of your resources' addons

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$resource_ids = NULL; // array | A comma-separated list of resource IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorAddons($resource_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorAddons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resource_ids** | [**array**](../Model/.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorAddons200Response**](../Model/GetV2ResourcesCreatorAddons200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorBundles()`

```php
getV2ResourcesCreatorBundles(): \OpenAPI\Client\Model\GetV2ResourcesCreatorBundles200Response
```

Fetch a list of your bundles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2ResourcesCreatorBundles();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorBundles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorBundles200Response**](../Model/GetV2ResourcesCreatorBundles200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorCoupons()`

```php
getV2ResourcesCreatorCoupons(): \OpenAPI\Client\Model\GetV2ResourcesCreatorCoupons200Response
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


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2ResourcesCreatorCoupons();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorCoupons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `getV2ResourcesCreatorLicenses()`

```php
getV2ResourcesCreatorLicenses($resource_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorLicenses200Response
```

Fetch a list of your resources' licenses

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$resource_ids = NULL; // array | A comma-separated list of resource IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorLicenses($resource_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorLicenses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resource_ids** | [**array**](../Model/.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorLicenses200Response**](../Model/GetV2ResourcesCreatorLicenses200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorPurchases()`

```php
getV2ResourcesCreatorPurchases($resource_ids, $buyer_ids, $external_tids): \OpenAPI\Client\Model\GetV2ResourcesCreatorPurchases200Response
```

Fetch a list of your resources' purchases

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$resource_ids = NULL; // array | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
$buyer_ids = NULL; // array | A comma-separated list of buyer IDs to filter on. No filter is applied if empty
$external_tids = NULL; // array | A comma-separated list of external transaction IDs (TIDs) to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorPurchases($resource_ids, $buyer_ids, $external_tids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorPurchases: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resource_ids** | [**array**](../Model/.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |
| **buyer_ids** | [**array**](../Model/.md)| A comma-separated list of buyer IDs to filter on. No filter is applied if empty | [optional] |
| **external_tids** | [**array**](../Model/.md)| A comma-separated list of external transaction IDs (TIDs) to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorPurchases200Response**](../Model/GetV2ResourcesCreatorPurchases200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorResources()`

```php
getV2ResourcesCreatorResources($resource_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorResources200Response
```

Fetch a list of your resources

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$resource_ids = NULL; // array | A comma-separated list of resource IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorResources($resource_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorResources: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resource_ids** | [**array**](../Model/.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorResources200Response**](../Model/GetV2ResourcesCreatorResources200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorReviews()`

```php
getV2ResourcesCreatorReviews($resource_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorReviews200Response
```

Fetch a list of your resources' reviews

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$resource_ids = NULL; // array | A comma-separated list of resource IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorReviews($resource_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resource_ids** | [**array**](../Model/.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorReviews200Response**](../Model/GetV2ResourcesCreatorReviews200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorSaleEvents()`

```php
getV2ResourcesCreatorSaleEvents(): \OpenAPI\Client\Model\GetV2ResourcesCreatorSaleEvents200Response
```

Fetch a list of your sale events

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2ResourcesCreatorSaleEvents();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorSaleEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorSaleEvents200Response**](../Model/GetV2ResourcesCreatorSaleEvents200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorStores()`

```php
getV2ResourcesCreatorStores(): \OpenAPI\Client\Model\GetV2ResourcesCreatorStores200Response
```

Fetch a list of your stores

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2ResourcesCreatorStores();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorStores: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorStores200Response**](../Model/GetV2ResourcesCreatorStores200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorUpdates()`

```php
getV2ResourcesCreatorUpdates($resource_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorUpdates200Response
```

Fetch a list of your resource's updates

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$resource_ids = NULL; // array | A comma-separated list of resource IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorUpdates($resource_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorUpdates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resource_ids** | [**array**](../Model/.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorUpdates200Response**](../Model/GetV2ResourcesCreatorUpdates200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesCreatorVersions()`

```php
getV2ResourcesCreatorVersions($resource_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorVersions200Response
```

Fetch a list of your resources' versions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$resource_ids = NULL; // array | A comma-separated list of resource IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorVersions($resource_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->getV2ResourcesCreatorVersions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **resource_ids** | [**array**](../Model/.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorVersions200Response**](../Model/GetV2ResourcesCreatorVersions200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesCreatorUpdate()`

```php
postV2ResourcesCreatorUpdate($post_v2_resources_creator_update_request): \OpenAPI\Client\Model\PostV2ResourcesCreatorUpdate200Response
```

Post a resource update

Creates a new version for the resource and optionally posts a public update message. The uploaded file must be encoded using base64 as part of the JSON request body shown below.    The request body (including the base64 encoded file data) cannot exceed 100MB. This roughly equates to a 67MB upload limit for the raw file when taking into account base64 encoding losses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_resources_creator_update_request = new \OpenAPI\Client\Model\PostV2ResourcesCreatorUpdateRequest(); // \OpenAPI\Client\Model\PostV2ResourcesCreatorUpdateRequest

try {
    $result = $apiInstance->postV2ResourcesCreatorUpdate($post_v2_resources_creator_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorApi->postV2ResourcesCreatorUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_creator_update_request** | [**\OpenAPI\Client\Model\PostV2ResourcesCreatorUpdateRequest**](../Model/PostV2ResourcesCreatorUpdateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesCreatorUpdate200Response**](../Model/PostV2ResourcesCreatorUpdate200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
