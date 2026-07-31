# OpenAPI\Client\ResourcesEmbedApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesEmbedDownloadInitiate()**](ResourcesEmbedApi.md#getV2ResourcesEmbedDownloadInitiate) | **GET** /v2/resources/embed/download/initiate | Initiate a download request |
| [**getV2ResourcesEmbedDownloadStatus()**](ResourcesEmbedApi.md#getV2ResourcesEmbedDownloadStatus) | **GET** /v2/resources/embed/download/status | Fetch the status of a download request |
| [**getV2ResourcesEmbedLatest()**](ResourcesEmbedApi.md#getV2ResourcesEmbedLatest) | **GET** /v2/resources/embed/latest | Fetches the latest versions &amp; license information |


## `getV2ResourcesEmbedDownloadInitiate()`

```php
getV2ResourcesEmbedDownloadInitiate($content_type, $content_id, $nonce): \OpenAPI\Client\Model\GetV2ResourcesEmbedDownloadInitiate200Response
```

Initiate a download request

See: https://builtbybit.com/help/developers/resource-apis/embed/

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
$content_type = 'content_type_example'; // string | Either 'resource', 'resource_version', 'api_asset'
$content_id = 56; // int
$nonce = 'nonce_example'; // string | 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc).

try {
    $result = $apiInstance->getV2ResourcesEmbedDownloadInitiate($content_type, $content_id, $nonce);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesEmbedApi->getV2ResourcesEmbedDownloadInitiate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **content_type** | **string**| Either &#39;resource&#39;, &#39;resource_version&#39;, &#39;api_asset&#39; | |
| **content_id** | **int**|  | |
| **nonce** | **string**| 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc). | |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesEmbedDownloadInitiate200Response**](../Model/GetV2ResourcesEmbedDownloadInitiate200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesEmbedDownloadStatus()`

```php
getV2ResourcesEmbedDownloadStatus($token): \OpenAPI\Client\Model\GetV2ResourcesEmbedDownloadStatus200Response
```

Fetch the status of a download request

See: https://builtbybit.com/help/developers/resource-apis/embed/

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
$token = 'token_example'; // string | The download request token returned from an initiate request.

try {
    $result = $apiInstance->getV2ResourcesEmbedDownloadStatus($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesEmbedApi->getV2ResourcesEmbedDownloadStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **string**| The download request token returned from an initiate request. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesEmbedDownloadStatus200Response**](../Model/GetV2ResourcesEmbedDownloadStatus200Response.md)

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

See: https://builtbybit.com/help/developers/resource-apis/embed/

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
