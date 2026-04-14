# OpenAPI\Client\ResourcesCreatorSaleEventsApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesCreatorSaleEvents()**](ResourcesCreatorSaleEventsApi.md#getV2ResourcesCreatorSaleEvents) | **GET** /v2/resources/creator/sale-events | Fetch a list of your sale events |
| [**getV2ResourcesCreatorSaleEventsEntries()**](ResourcesCreatorSaleEventsApi.md#getV2ResourcesCreatorSaleEventsEntries) | **GET** /v2/resources/creator/sale-events/entries | Fetch a list of your sale event entries |


## `getV2ResourcesCreatorSaleEvents()`

```php
getV2ResourcesCreatorSaleEvents($sale_event_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorSaleEvents200Response
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


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorSaleEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sale_event_ids = NULL; // array | A comma-separated list of sale event IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorSaleEvents($sale_event_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorSaleEventsApi->getV2ResourcesCreatorSaleEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sale_event_ids** | [**array**](../Model/.md)| A comma-separated list of sale event IDs to filter on. No filter is applied if empty. | [optional] |

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

## `getV2ResourcesCreatorSaleEventsEntries()`

```php
getV2ResourcesCreatorSaleEventsEntries($sale_event_ids): \OpenAPI\Client\Model\GetV2ResourcesCreatorSaleEventsEntries200Response
```

Fetch a list of your sale event entries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesCreatorSaleEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sale_event_ids = NULL; // array | A comma-separated list of sale event IDs to filter on. No filter is applied if empty.

try {
    $result = $apiInstance->getV2ResourcesCreatorSaleEventsEntries($sale_event_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesCreatorSaleEventsApi->getV2ResourcesCreatorSaleEventsEntries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sale_event_ids** | [**array**](../Model/.md)| A comma-separated list of sale event IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesCreatorSaleEventsEntries200Response**](../Model/GetV2ResourcesCreatorSaleEventsEntries200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
