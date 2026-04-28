# OpenAPI\Client\DeploymentsApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postV2DeploymentsUpgrade()**](DeploymentsApi.md#postV2DeploymentsUpgrade) | **POST** /v2/deployments/upgrade | Upgrade a short-lived token |


## `postV2DeploymentsUpgrade()`

```php
postV2DeploymentsUpgrade($post_v2_deployments_upgrade_request): \OpenAPI\Client\Model\PostV2DeploymentsUpgrade200Response
```

Upgrade a short-lived token



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_deployments_upgrade_request = new \OpenAPI\Client\Model\PostV2DeploymentsUpgradeRequest(); // \OpenAPI\Client\Model\PostV2DeploymentsUpgradeRequest

try {
    $result = $apiInstance->postV2DeploymentsUpgrade($post_v2_deployments_upgrade_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->postV2DeploymentsUpgrade: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_deployments_upgrade_request** | [**\OpenAPI\Client\Model\PostV2DeploymentsUpgradeRequest**](../Model/PostV2DeploymentsUpgradeRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2DeploymentsUpgrade200Response**](../Model/PostV2DeploymentsUpgrade200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
