# OpenAPI\Client\ResourcesBuyerApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesBuyerLatest()**](ResourcesBuyerApi.md#getV2ResourcesBuyerLatest) | **GET** /v2/resources/buyer/latest | Fetches the latest versions &amp; license information |


## `getV2ResourcesBuyerLatest()`

```php
getV2ResourcesBuyerLatest($nonce): \OpenAPI\Client\Model\GetV2ResourcesBuyerLatest200Response
```

Fetches the latest versions & license information

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesBuyerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$nonce = 'nonce_example'; // string | 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc).

try {
    $result = $apiInstance->getV2ResourcesBuyerLatest($nonce);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesBuyerApi->getV2ResourcesBuyerLatest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **nonce** | **string**| 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc). | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesBuyerLatest200Response**](../Model/GetV2ResourcesBuyerLatest200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
