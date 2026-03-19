# OpenAPI\Client\DefaultApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2Analytics()**](DefaultApi.md#getV2Analytics) | **GET** /v2/analytics | Fetch a list of analytics definitions |
| [**getV2AnalyticsGraph()**](DefaultApi.md#getV2AnalyticsGraph) | **GET** /v2/analytics/graph | Fetch analytics graph data |
| [**getV2Events()**](DefaultApi.md#getV2Events) | **GET** /v2/events | Fetch a list of pending events |
| [**postV2EventsComplete()**](DefaultApi.md#postV2EventsComplete) | **POST** /v2/events/complete | Mark events as complete |
| [**postV2ResourcesCreatorUpdate()**](DefaultApi.md#postV2ResourcesCreatorUpdate) | **POST** /v2/resources/creator/update | Post a resource update |


## `getV2Analytics()`

```php
getV2Analytics(): \OpenAPI\Client\Model\GetV2Analytics200Response
```

Fetch a list of analytics definitions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getV2Analytics();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getV2Analytics: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2Analytics200Response**](../Model/GetV2Analytics200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2AnalyticsGraph()`

```php
getV2AnalyticsGraph($analytics, $period, $grouping, $filters, $start_date, $end_date): \OpenAPI\Client\Model\GetV2AnalyticsGraph200Response
```

Fetch analytics graph data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$analytics = NULL; // array
$period = 'period_example'; // string
$grouping = 'grouping_example'; // string
$filters = 'filters_example'; // string
$start_date = 'start_date_example'; // string | Only respected when 'period' = 'custom_range'.
$end_date = 'end_date_example'; // string | Only respected when 'period' = 'custom_range'.

try {
    $result = $apiInstance->getV2AnalyticsGraph($analytics, $period, $grouping, $filters, $start_date, $end_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getV2AnalyticsGraph: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **analytics** | [**array**](../Model/.md)|  | [optional] |
| **period** | **string**|  | [optional] |
| **grouping** | **string**|  | [optional] |
| **filters** | **string**|  | [optional] |
| **start_date** | **string**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;. | [optional] |
| **end_date** | **string**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2AnalyticsGraph200Response**](../Model/GetV2AnalyticsGraph200Response.md)

### Authorization

No authorization required

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



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getV2Events();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getV2Events: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2Events200Response**](../Model/GetV2Events200Response.md)

### Authorization

No authorization required

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



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_events_complete_request = new \OpenAPI\Client\Model\PostV2EventsCompleteRequest(); // \OpenAPI\Client\Model\PostV2EventsCompleteRequest

try {
    $result = $apiInstance->postV2EventsComplete($post_v2_events_complete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->postV2EventsComplete: ', $e->getMessage(), PHP_EOL;
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



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_resources_creator_update_request = new \OpenAPI\Client\Model\PostV2ResourcesCreatorUpdateRequest(); // \OpenAPI\Client\Model\PostV2ResourcesCreatorUpdateRequest

try {
    $result = $apiInstance->postV2ResourcesCreatorUpdate($post_v2_resources_creator_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->postV2ResourcesCreatorUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_creator_update_request** | [**\OpenAPI\Client\Model\PostV2ResourcesCreatorUpdateRequest**](../Model/PostV2ResourcesCreatorUpdateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesCreatorUpdate200Response**](../Model/PostV2ResourcesCreatorUpdate200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
