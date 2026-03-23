# OpenAPI\Client\ResourcesCreatorApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postV2ResourcesCreatorUpdate()**](ResourcesCreatorApi.md#postV2ResourcesCreatorUpdate) | **POST** /v2/resources/creator/update | Post a resource update |


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
