# OpenAPI\Client\ResourcesDiscoverApi

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getResourcesDiscoverCategories()**](ResourcesDiscoverApi.md#getResourcesDiscoverCategories) | **GET** /v2/resources/discover/categories | Fetch a list of categories |
| [**getResourcesDiscoverResources()**](ResourcesDiscoverApi.md#getResourcesDiscoverResources) | **GET** /v2/resources/discover/resources | Fetch a list of resources |
| [**getV2ResourcesDiscoverDownloadDirectInitiate()**](ResourcesDiscoverApi.md#getV2ResourcesDiscoverDownloadDirectInitiate) | **GET** /v2/resources/discover/download/direct/initiate | Initiate a direct download request |
| [**getV2ResourcesDiscoverDownloadDirectPoll()**](ResourcesDiscoverApi.md#getV2ResourcesDiscoverDownloadDirectPoll) | **GET** /v2/resources/discover/download/direct/status | Fetch the status of a direct download request |
| [**getV2ResourcesDiscoverLicenses()**](ResourcesDiscoverApi.md#getV2ResourcesDiscoverLicenses) | **GET** /v2/resources/discover/licenses | Fetch a list of the user&#39;s licenses |


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


// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string | A category ID to filter on.
$with = 'with_example'; // string | A comma-separated list of submodels to include.

try {
    $result = $apiInstance->getResourcesDiscoverCategories($category_id, $with);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverApi->getResourcesDiscoverCategories: ', $e->getMessage(), PHP_EOL;
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

[token](../../README.md#token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResourcesDiscoverResources()`

```php
getResourcesDiscoverResources($category_id, $with, $filters, $resource_ids, $page, $per_page, $no_dependencies, $excluded_resource_ids, $excluded_creator_ids): \OpenAPI\Client\Model\GetResourcesDiscoverResources200Response
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


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverApi(
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
$no_dependencies = True; // bool | Whether or not to exclude resources with dependencies listed.
$excluded_resource_ids = 'excluded_resource_ids_example'; // string | A comma-separated list of resource IDs to exclude. No filter will be applied if empty.
$excluded_creator_ids = 'excluded_creator_ids_example'; // string | A comma-separated list of creator IDs to exclude. No filter will be applied if empty.

try {
    $result = $apiInstance->getResourcesDiscoverResources($category_id, $with, $filters, $resource_ids, $page, $per_page, $no_dependencies, $excluded_resource_ids, $excluded_creator_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverApi->getResourcesDiscoverResources: ', $e->getMessage(), PHP_EOL;
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
| **no_dependencies** | **bool**| Whether or not to exclude resources with dependencies listed. | [optional] |
| **excluded_resource_ids** | **string**| A comma-separated list of resource IDs to exclude. No filter will be applied if empty. | [optional] |
| **excluded_creator_ids** | **string**| A comma-separated list of creator IDs to exclude. No filter will be applied if empty. | [optional] |

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

## `getV2ResourcesDiscoverDownloadDirectInitiate()`

```php
getV2ResourcesDiscoverDownloadDirectInitiate($content_type, $content_id): \OpenAPI\Client\Model\GetV2ResourcesDiscoverDownloadDirectInitiate200Response
```

Initiate a direct download request

See: https://builtbybit.com/help/developers/discovery-api/downloading-and-one-click/

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$content_type = 'content_type_example'; // string | Either 'resource' or 'resource_version'
$content_id = 56; // int

try {
    $result = $apiInstance->getV2ResourcesDiscoverDownloadDirectInitiate($content_type, $content_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverApi->getV2ResourcesDiscoverDownloadDirectInitiate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **content_type** | **string**| Either &#39;resource&#39; or &#39;resource_version&#39; | |
| **content_id** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesDiscoverDownloadDirectInitiate200Response**](../Model/GetV2ResourcesDiscoverDownloadDirectInitiate200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getV2ResourcesDiscoverDownloadDirectPoll()`

```php
getV2ResourcesDiscoverDownloadDirectPoll($token): \OpenAPI\Client\Model\GetV2ResourcesDiscoverDownloadDirectPoll200Response
```

Fetch the status of a direct download request

See: https://builtbybit.com/help/developers/discovery-api/downloading-and-one-click/

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token = 'token_example'; // string | The download request token returned from an initiate request.

try {
    $result = $apiInstance->getV2ResourcesDiscoverDownloadDirectPoll($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverApi->getV2ResourcesDiscoverDownloadDirectPoll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **string**| The download request token returned from an initiate request. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetV2ResourcesDiscoverDownloadDirectPoll200Response**](../Model/GetV2ResourcesDiscoverDownloadDirectPoll200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

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


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ResourcesDiscoverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int | The page number/offset to return items for.
$per_page = 25; // int | The number of items per page to return.
$with = 'with_example'; // string | A comma-separated list of supported 'with hints'. See model & endpoint-level docs for more info.

try {
    $result = $apiInstance->getV2ResourcesDiscoverLicenses($page, $per_page, $with);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResourcesDiscoverApi->getV2ResourcesDiscoverLicenses: ', $e->getMessage(), PHP_EOL;
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

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
