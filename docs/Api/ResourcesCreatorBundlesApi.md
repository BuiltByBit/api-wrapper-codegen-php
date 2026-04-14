# OpenAPI\Client\ResourcesCreatorBundlesApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesCreatorBundles()**](ResourcesCreatorBundlesApi.md#getV2ResourcesCreatorBundles) | **GET** /v2/resources/creator/bundles | Fetch a list of your bundles |
| [**getV2ResourcesCreatorBundlesEntries()**](ResourcesCreatorBundlesApi.md#getV2ResourcesCreatorBundlesEntries) | **GET** /v2/resources/creator/bundles/entries | Fetch a list of your bundle entries |


## `getV2ResourcesCreatorBundles()`

```php
getV2ResourcesCreatorBundles($bundle_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorBundles200Response
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


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorBundlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bundle_ids = NULL; // array | A comma-separated list of bundle IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorBundles($bundle_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorBundlesApi->getV2ResourcesCreatorBundles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bundle_ids** | [**array**](../Model/.md)| A comma-separated list of bundle IDs to filter on. No filter is applied if empty. | [optional] |

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

## `getV2ResourcesCreatorBundlesEntries()`

```php
getV2ResourcesCreatorBundlesEntries($bundle_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorBundlesEntries200Response
```

Fetch a list of your bundle entries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorBundlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bundle_ids = NULL; // array | A comma-separated list of bundle IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorBundlesEntries($bundle_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorBundlesApi->getV2ResourcesCreatorBundlesEntries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bundle_ids** | [**array**](../Model/.md)| A comma-separated list of bundle IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorBundlesEntries200Response**](../Model/GetV2ResourcesCreatorBundlesEntries200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
