# OpenAPI\Client\EventsApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2Events()**](EventsApi.md#getV2Events) | **GET** /v2/events | Fetch a list of pending events |
| [**postV2EventsComplete()**](EventsApi.md#postV2EventsComplete) | **POST** /v2/events/complete | Mark events as complete |


## `getV2Events()`

```php
getV2Events(): \OpenAPI\Client\Model\GetV2Events200Response
```

Fetch a list of pending events

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2Events();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->getV2Events: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2Events200Response**](../Model/GetV2Events200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2EventsComplete()`

```php
postV2EventsComplete($post_v2_events_complete_request): \OpenAPI\Client\Model\PostV2EventsComplete200Response
```

Mark events as complete

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_events_complete_request = new \OpenAPI\Client\Model\PostV2EventsCompleteRequest(); // \OpenAPI\Client\Model\PostV2EventsCompleteRequest

try {
    $result = $apiInstance->postV2EventsComplete($post_v2_events_complete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->postV2EventsComplete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_events_complete_request** | [**\OpenAPI\Client\Model\PostV2EventsCompleteRequest**](../Model/PostV2EventsCompleteRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2EventsComplete200Response**](../Model/PostV2EventsComplete200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
