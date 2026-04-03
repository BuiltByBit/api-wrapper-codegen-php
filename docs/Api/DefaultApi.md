# OpenAPI\Client\DefaultApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesCreatorBatch()**](DefaultApi.md#getV2ResourcesCreatorBatch) | **GET** /v2/resources/creator/batch | Fetch a list of your batches edits |
| [**postV2ResourcesCreatorBatch()**](DefaultApi.md#postV2ResourcesCreatorBatch) | **POST** /v2/resources/creator/batch | Submit a new batch edit |


## `getV2ResourcesCreatorBatch()`

```php
getV2ResourcesCreatorBatch($batch_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorBatch200Response
```

Fetch a list of your batches edits

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_ids = NULL; // array | A comma-separated list of batch IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorBatch($batch_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getV2ResourcesCreatorBatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_ids** | [**array**](../Model/.md)| A comma-separated list of batch IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorBatch200Response**](../Model/GetV2ResourcesCreatorBatch200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesCreatorBatch()`

```php
postV2ResourcesCreatorBatch($post_v2_resources_creator_batch_request): \OpenAPI\Client\Model\PostV2ResourcesCreatorBatch200Response
```

Submit a new batch edit

Batch edits will be processed in the background meaning a successful call to this endpoint does not guarantee that the edits have been completed. You will instead receive an identifier to a batch edit which you can then use to fetch the status of via the below endpoint. This is not an atomic operation meaning some resources may be edited successfully and others may not be due to an error. You may only batch edit resources you own currently.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_resources_creator_batch_request = new \OpenAPI\Client\Model\PostV2ResourcesCreatorBatchRequest(); // \OpenAPI\Client\Model\PostV2ResourcesCreatorBatchRequest

try {
    $result = $apiInstance->postV2ResourcesCreatorBatch($post_v2_resources_creator_batch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->postV2ResourcesCreatorBatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_creator_batch_request** | [**\OpenAPI\Client\Model\PostV2ResourcesCreatorBatchRequest**](../Model/PostV2ResourcesCreatorBatchRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesCreatorBatch200Response**](../Model/PostV2ResourcesCreatorBatch200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
