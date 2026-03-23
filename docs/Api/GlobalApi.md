# OpenAPI\Client\GlobalApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2Analytics()**](GlobalApi.md#getV2Analytics) | **GET** /v2/analytics | Fetch a list of analytics definitions |
| [**getV2AnalyticsGraph()**](GlobalApi.md#getV2AnalyticsGraph) | **GET** /v2/analytics/graph | Fetch analytics graph data |
| [**getV2AnalyticsSingle()**](GlobalApi.md#getV2AnalyticsSingle) | **GET** /v2/analytics/single | Fetch a single analytics value |
| [**getV2Events()**](GlobalApi.md#getV2Events) | **GET** /v2/events | Fetch a list of pending events |
| [**postV2EventsComplete()**](GlobalApi.md#postV2EventsComplete) | **POST** /v2/events/complete | Mark events as complete |


## `getV2Analytics()`

```php
getV2Analytics(): \OpenAPI\Client\Model\GetV2Analytics200Response
```

Fetch a list of analytics definitions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GlobalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2Analytics();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GlobalApi->getV2Analytics: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2Analytics200Response**](../Model/GetV2Analytics200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2AnalyticsGraph()`

```php
getV2AnalyticsGraph($analytics, $period, $filters, $start_date, $end_date): \OpenAPI\Client\Model\GetV2AnalyticsGraph200Response
```

Fetch analytics graph data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GlobalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$analytics = NULL; // array | A list of analytic IDs to fetch data for.
$period = 'period_example'; // string | The time period to fetch data over.
$filters = NULL; // array | A set of filters which may be used for the analytics.
$start_date = 'start_date_example'; // string | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.
$end_date = 'end_date_example'; // string | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.

try {
    $result = $apiInstance->getV2AnalyticsGraph($analytics, $period, $filters, $start_date, $end_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GlobalApi->getV2AnalyticsGraph: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **analytics** | [**array**](../Model/.md)| A list of analytic IDs to fetch data for. | [optional] |
| **period** | **string**| The time period to fetch data over. | [optional] |
| **filters** | [**array**](../Model/.md)| A set of filters which may be used for the analytics. | [optional] |
| **start_date** | **string**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |
| **end_date** | **string**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2AnalyticsGraph200Response**](../Model/GetV2AnalyticsGraph200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2AnalyticsSingle()`

```php
getV2AnalyticsSingle($analytics, $period, $filters, $start_date, $end_date): \OpenAPI\Client\Model\GetV2AnalyticsSingle200Response
```

Fetch a single analytics value

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GlobalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$analytics = NULL; // array | A list of analytic IDs to fetch data for.
$period = 'period_example'; // string | The time period to fetch data over.
$filters = NULL; // array | A set of filters which may be used for the analytics.
$start_date = 'start_date_example'; // string | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.
$end_date = 'end_date_example'; // string | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.

try {
    $result = $apiInstance->getV2AnalyticsSingle($analytics, $period, $filters, $start_date, $end_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GlobalApi->getV2AnalyticsSingle: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **analytics** | [**array**](../Model/.md)| A list of analytic IDs to fetch data for. | [optional] |
| **period** | **string**| The time period to fetch data over. | [optional] |
| **filters** | [**array**](../Model/.md)| A set of filters which may be used for the analytics. | [optional] |
| **start_date** | **string**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |
| **end_date** | **string**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2AnalyticsSingle200Response**](../Model/GetV2AnalyticsSingle200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

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


$apiInstance = new OpenAPI\Client\Api\GlobalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2Events();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GlobalApi->getV2Events: ', $e->getMessage(), PHP_EOL;
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



$apiInstance = new OpenAPI\Client\Api\GlobalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_events_complete_request = new \OpenAPI\Client\Model\PostV2EventsCompleteRequest(); // \OpenAPI\Client\Model\PostV2EventsCompleteRequest

try {
    $result = $apiInstance->postV2EventsComplete($post_v2_events_complete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GlobalApi->postV2EventsComplete: ', $e->getMessage(), PHP_EOL;
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
