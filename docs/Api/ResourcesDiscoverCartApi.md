# OpenAPI\Client\ResourcesDiscoverCartApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getV2ResourcesDiscoverCartView()**](ResourcesDiscoverCartApi.md#getV2ResourcesDiscoverCartView) | **GET** /v2/resources/discover/cart/view | View the user&#39;s cart items |
| [**postV2ResourcesDiscoverCartAdd()**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartAdd) | **POST** /v2/resources/discover/cart/add | Add items to a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCheckout()**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartCheckout) | **POST** /v2/resources/discover/cart/checkout | Initiate a checkout of a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponAdd()**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartCouponAdd) | **POST** /v2/resources/discover/cart/coupon/add | Add a coupon to the user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponRemove()**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartCouponRemove) | **POST** /v2/resources/discover/cart/coupon/remove | Remove a coupon from the user&#39;s cart |
| [**postV2ResourcesDiscoverCartRemove()**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartRemove) | **POST** /v2/resources/discover/cart/remove | Remove an item from the user&#39;s cart |


## `getV2ResourcesDiscoverCartView()`

```php
getV2ResourcesDiscoverCartView(): \OpenAPI\Client\Model\GetV2ResourcesDiscoverCartView200Response
```

View the user's cart items



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverCartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2ResourcesDiscoverCartView();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverCartApi->getV2ResourcesDiscoverCartView: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesDiscoverCartView200Response**](../Model/GetV2ResourcesDiscoverCartView200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesDiscoverCartAdd()`

```php
postV2ResourcesDiscoverCartAdd($post_v2_resources_discover_cart_add_request): \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAdd2XXResponse
```

Add items to a user's cart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverCartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_resources_discover_cart_add_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAddRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAddRequest | A list of content to add to the user's cart. The outer list is keyed by the content type and the inner list are the content IDs.    For instance, if adding a resource with the ID 555, the body becomes:  ```json  {\"add\": {\"resource\": [555]}}  ```

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartAdd($post_v2_resources_discover_cart_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverCartApi->postV2ResourcesDiscoverCartAdd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_add_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAddRequest**](../Model/PostV2ResourcesDiscoverCartAddRequest.md)| A list of content to add to the user&#39;s cart. The outer list is keyed by the content type and the inner list are the content IDs.    For instance, if adding a resource with the ID 555, the body becomes:  &#x60;&#x60;&#x60;json  {\&quot;add\&quot;: {\&quot;resource\&quot;: [555]}}  &#x60;&#x60;&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAdd2XXResponse**](../Model/PostV2ResourcesDiscoverCartAdd2XXResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesDiscoverCartCheckout()`

```php
postV2ResourcesDiscoverCartCheckout($body): \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCheckout200Response
```

Initiate a checkout of a user's cart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverCartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartCheckout($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverCartApi->postV2ResourcesDiscoverCartCheckout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | **object**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCheckout200Response**](../Model/PostV2ResourcesDiscoverCartCheckout200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesDiscoverCartCouponAdd()`

```php
postV2ResourcesDiscoverCartCouponAdd($post_v2_resources_discover_cart_coupon_add_request): \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAdd200Response
```

Add a coupon to the user's cart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverCartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_resources_discover_cart_coupon_add_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAddRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAddRequest

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartCouponAdd($post_v2_resources_discover_cart_coupon_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverCartApi->postV2ResourcesDiscoverCartCouponAdd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_coupon_add_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAddRequest**](../Model/PostV2ResourcesDiscoverCartCouponAddRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAdd200Response**](../Model/PostV2ResourcesDiscoverCartCouponAdd200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesDiscoverCartCouponRemove()`

```php
postV2ResourcesDiscoverCartCouponRemove($post_v2_resources_discover_cart_coupon_remove_request): \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemove200Response
```

Remove a coupon from the user's cart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverCartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_resources_discover_cart_coupon_remove_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemoveRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemoveRequest

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartCouponRemove($post_v2_resources_discover_cart_coupon_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverCartApi->postV2ResourcesDiscoverCartCouponRemove: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_coupon_remove_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemoveRequest**](../Model/PostV2ResourcesDiscoverCartCouponRemoveRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemove200Response**](../Model/PostV2ResourcesDiscoverCartCouponRemove200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postV2ResourcesDiscoverCartRemove()`

```php
postV2ResourcesDiscoverCartRemove($post_v2_resources_discover_cart_remove_request): \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemove200Response
```

Remove an item from the user's cart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverCartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_v2_resources_discover_cart_remove_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemoveRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemoveRequest

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartRemove($post_v2_resources_discover_cart_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverCartApi->postV2ResourcesDiscoverCartRemove: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_remove_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemoveRequest**](../Model/PostV2ResourcesDiscoverCartRemoveRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemove200Response**](../Model/PostV2ResourcesDiscoverCartRemove200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
