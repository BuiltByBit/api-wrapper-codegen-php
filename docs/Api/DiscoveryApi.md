# OpenAPI\Client\DiscoveryApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getResourcesDiscoverCategories()**](DiscoveryApi.md#getResourcesDiscoverCategories) | **GET** /v2/resources/discover/categories | Fetch a list of categories |
| [**getResourcesDiscoverResources()**](DiscoveryApi.md#getResourcesDiscoverResources) | **GET** /v2/resources/discover/resources | Fetch a list of resources |
| [**getV2ResourcesDiscoverCartView()**](DiscoveryApi.md#getV2ResourcesDiscoverCartView) | **GET** /v2/resources/discover/cart/view | View the user&#39;s cart items |
| [**getV2ResourcesDiscoverLicenses()**](DiscoveryApi.md#getV2ResourcesDiscoverLicenses) | **GET** /v2/resources/discover/licenses | Fetch a list of the user&#39;s licenses |
| [**postV2ResourcesDiscoverCartAdd()**](DiscoveryApi.md#postV2ResourcesDiscoverCartAdd) | **POST** /v2/resources/discover/cart/add | Add items to a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCheckout()**](DiscoveryApi.md#postV2ResourcesDiscoverCartCheckout) | **POST** /v2/resources/discover/cart/checkout | Initiate a checkout of a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponAdd()**](DiscoveryApi.md#postV2ResourcesDiscoverCartCouponAdd) | **POST** /v2/resources/discover/cart/coupon/add | Add a coupon to the user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponRemove()**](DiscoveryApi.md#postV2ResourcesDiscoverCartCouponRemove) | **POST** /v2/resources/discover/cart/coupon/remove | Remove a coupon from the user&#39;s cart |
| [**postV2ResourcesDiscoverCartRemove()**](DiscoveryApi.md#postV2ResourcesDiscoverCartRemove) | **POST** /v2/resources/discover/cart/remove | Remove an item from the user&#39;s cart |


## `getResourcesDiscoverCategories()`

```php
getResourcesDiscoverCategories($category_id, $with): \OpenAPI\Client\Model\GetResourcesDiscoverCategories200Response
```

Fetch a list of categories

Supported 'with' hints:  - Children: includes all subcategories and their children

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$category_id = 'category_id_example'; // string | A category ID to filter on.
$with = 'with_example'; // string | A comma-separated list of submodels to include.

try {
    $result = $apiInstance->getResourcesDiscoverCategories($category_id, $with);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->getResourcesDiscoverCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**| A category ID to filter on. | [optional] |
| **with** | **string**| A comma-separated list of submodels to include. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetResourcesDiscoverCategories200Response**](../Model/GetResourcesDiscoverCategories200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResourcesDiscoverResources()`

```php
getResourcesDiscoverResources($category_id, $with, $filters, $resource_ids, $page, $per_page, $no_dependencies): \OpenAPI\Client\Model\GetResourcesDiscoverResources200Response
```

Fetch a list of resources

Supported 'with' hints:  - `filters`: include dynamic filter information in the response.  - See 'Resource' model for additional 'with' hints.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string | A category ID to filter on. If the provided category is a parent, resources from subcategories will also be included.
$with = Description,Creator; // string | A comma-separated list of additional data to include. See endpoint documentation for more information.
$filters = array('key' => new \stdClass); // object | A list of dynamic filters to apply.
$resource_ids = 'resource_ids_example'; // string | A comma-separated list of resource IDs to filter on.
$page = 1; // int | The page number to return.
$per_page = 25; // float | The number of resources to return per page.
$no_dependencies = True; // bool

try {
    $result = $apiInstance->getResourcesDiscoverResources($category_id, $with, $filters, $resource_ids, $page, $per_page, $no_dependencies);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->getResourcesDiscoverResources: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**| A category ID to filter on. If the provided category is a parent, resources from subcategories will also be included. | [optional] |
| **with** | **string**| A comma-separated list of additional data to include. See endpoint documentation for more information. | [optional] |
| **filters** | [**object**](../Model/.md)| A list of dynamic filters to apply. | [optional] |
| **resource_ids** | **string**| A comma-separated list of resource IDs to filter on. | [optional] |
| **page** | **int**| The page number to return. | [optional] [default to 1] |
| **per_page** | **float**| The number of resources to return per page. | [optional] [default to 25] |
| **no_dependencies** | **bool**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetResourcesDiscoverResources200Response**](../Model/GetResourcesDiscoverResources200Response.md)

### Authorization

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesDiscoverCartView()`

```php
getV2ResourcesDiscoverCartView(): \OpenAPI\Client\Model\GetV2ResourcesDiscoverCartView200Response
```

View the user's cart items

Supported 'with hints':

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getV2ResourcesDiscoverCartView();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->getV2ResourcesDiscoverCartView: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesDiscoverCartView200Response**](../Model/GetV2ResourcesDiscoverCartView200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesDiscoverLicenses()`

```php
getV2ResourcesDiscoverLicenses($page, $per_page, $with): \OpenAPI\Client\Model\GetV2ResourcesDiscoverLicenses200Response
```

Fetch a list of the user's licenses

Supported 'with' hints:  - Resource: the resource the license is for if content_type = `resource`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 56; // int | The page number/offset to return items for.
$per_page = 25; // int | The number of items per page to return.
$with = 'with_example'; // string | A comma-separated list of supported 'with hints'. See model & endpoint-level docs for more info.

try {
    $result = $apiInstance->getV2ResourcesDiscoverLicenses($page, $per_page, $with);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->getV2ResourcesDiscoverLicenses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The page number/offset to return items for. | [optional] |
| **per_page** | **int**| The number of items per page to return. | [optional] [default to 25] |
| **with** | **string**| A comma-separated list of supported &#39;with hints&#39;. See model &amp; endpoint-level docs for more info. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesDiscoverLicenses200Response**](../Model/GetV2ResourcesDiscoverLicenses200Response.md)

### Authorization

No authorization required

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



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_resources_discover_cart_add_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAddRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAddRequest | A list of content to add to the user's cart. The outer list is keyed by the content type and the inner list are the content IDs.    For instance, if adding a resource with the ID 555, the body becomes:  ```json  {\"add\": {\"resource\": [555]}}  ```

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartAdd($post_v2_resources_discover_cart_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->postV2ResourcesDiscoverCartAdd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_add_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAddRequest**](../Model/PostV2ResourcesDiscoverCartAddRequest.md)| A list of content to add to the user&#39;s cart. The outer list is keyed by the content type and the inner list are the content IDs.    For instance, if adding a resource with the ID 555, the body becomes:  &#x60;&#x60;&#x60;json  {\&quot;add\&quot;: {\&quot;resource\&quot;: [555]}}  &#x60;&#x60;&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartAdd2XXResponse**](../Model/PostV2ResourcesDiscoverCartAdd2XXResponse.md)

### Authorization

No authorization required

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



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartCheckout($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->postV2ResourcesDiscoverCartCheckout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | **object**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCheckout200Response**](../Model/PostV2ResourcesDiscoverCartCheckout200Response.md)

### Authorization

No authorization required

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



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_resources_discover_cart_coupon_add_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAddRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAddRequest

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartCouponAdd($post_v2_resources_discover_cart_coupon_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->postV2ResourcesDiscoverCartCouponAdd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_coupon_add_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAddRequest**](../Model/PostV2ResourcesDiscoverCartCouponAddRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponAdd200Response**](../Model/PostV2ResourcesDiscoverCartCouponAdd200Response.md)

### Authorization

No authorization required

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



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_resources_discover_cart_coupon_remove_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemoveRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemoveRequest

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartCouponRemove($post_v2_resources_discover_cart_coupon_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->postV2ResourcesDiscoverCartCouponRemove: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_coupon_remove_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemoveRequest**](../Model/PostV2ResourcesDiscoverCartCouponRemoveRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartCouponRemove200Response**](../Model/PostV2ResourcesDiscoverCartCouponRemove200Response.md)

### Authorization

No authorization required

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



$apiInstance = new OpenAPI\Client\Api\DiscoveryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$post_v2_resources_discover_cart_remove_request = new \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemoveRequest(); // \OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemoveRequest

try {
    $result = $apiInstance->postV2ResourcesDiscoverCartRemove($post_v2_resources_discover_cart_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscoveryApi->postV2ResourcesDiscoverCartRemove: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_v2_resources_discover_cart_remove_request** | [**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemoveRequest**](../Model/PostV2ResourcesDiscoverCartRemoveRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PostV2ResourcesDiscoverCartRemove200Response**](../Model/PostV2ResourcesDiscoverCartRemove200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
