# OpenAPI\Client\ResourcesEmbedApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesEmbedDownload()**](ResourcesEmbedApi.md#getV2ResourcesEmbedDownload) | **GET** /v2/resources/embed/download | Fetch the status of a download request |
| [**getV2ResourcesEmbedLatest()**](ResourcesEmbedApi.md#getV2ResourcesEmbedLatest) | **GET** /v2/resources/embed/latest | Fetches the latest versions &amp; license information |
| [**postV2ResourcesEmbedDownload()**](ResourcesEmbedApi.md#postV2ResourcesEmbedDownload) | **POST** /v2/resources/embed/download | Submit a new download request |


## `getV2ResourcesEmbedDownload()`

```php
getV2ResourcesEmbedDownload($token): \OpenAPI\Client\Model\GetV2ResourcesEmbedDownload200Response
```

Fetch the status of a download request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesEmbedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token = 'token_example'; // string | The token provided when submitting a download request.

try {
    $result = $apiInstance->getV2ResourcesEmbedDownload($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesEmbedApi->getV2ResourcesEmbedDownload: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **string**| The token provided when submitting a download request. | |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesEmbedDownload200Response**](../Model/GetV2ResourcesEmbedDownload200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesEmbedLatest()`

```php
getV2ResourcesEmbedLatest($nonce): \OpenAPI\Client\Model\GetV2ResourcesEmbedLatest200Response
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


$apiInstance = new OpenAPI\Client\Api\ResourcesEmbedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$nonce = 'nonce_example'; // string | 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc).

try {
    $result = $apiInstance->getV2ResourcesEmbedLatest($nonce);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesEmbedApi->getV2ResourcesEmbedLatest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **nonce** | **string**| 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc). | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesEmbedLatest200Response**](../Model/GetV2ResourcesEmbedLatest200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesEmbedDownload()`

```php
postV2ResourcesEmbedDownload($post_v2_resources_embed_download_request): \OpenAPI\Client\Model\PostV2ResourcesEmbedDownload200Response
```

Submit a new download request

Supported content types:  - 'resource_version'  - 'api_asset'

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesEmbedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_resources_embed_download_request = new \OpenAPI\Client\Model\PostV2ResourcesEmbedDownloadRequest(); // \OpenAPI\Client\Model\PostV2ResourcesEmbedDownloadRequest

try {
    $result = $apiInstance->postV2ResourcesEmbedDownload($post_v2_resources_embed_download_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesEmbedApi->postV2ResourcesEmbedDownload: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_embed_download_request** | [**\OpenAPI\Client\Model\PostV2ResourcesEmbedDownloadRequest**](../Model/PostV2ResourcesEmbedDownloadRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesEmbedDownload200Response**](../Model/PostV2ResourcesEmbedDownload200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
