# OpenAPI\Client\Oauth2Api

All URIs are relative to https://api.builtbybit.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getOauth2Token()**](Oauth2Api.md#getOauth2Token) | **POST** /oauth2/token | Request an access token using an existing grant |
| [**getOauth2TokenRevoke()**](Oauth2Api.md#getOauth2TokenRevoke) | **POST** /oauth2/token/revoke | Revoke an existing access or refresh token |


## `getOauth2Token()`

```php
getOauth2Token($authorization, $grant_type, $code, $refresh_token): \OpenAPI\Client\Model\GetOauth2Token200Response
```

Request an access token using an existing grant

Supported grant types: authorization_code, refresh_token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\Oauth2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$authorization = 'authorization_example'; // string | OAuth2 client credentials in the Basic authorization format.
$grant_type = 'grant_type_example'; // string
$code = 'code_example'; // string | Required if grant_type = `authorization_code`.
$refresh_token = 'refresh_token_example'; // string | Required if grant_type = `refresh_token`.

try {
    $result = $apiInstance->getOauth2Token($authorization, $grant_type, $code, $refresh_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling Oauth2Api->getOauth2Token: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **authorization** | **string**| OAuth2 client credentials in the Basic authorization format. | |
| **grant_type** | **string**|  | |
| **code** | **string**| Required if grant_type &#x3D; &#x60;authorization_code&#x60;. | [optional] |
| **refresh_token** | **string**| Required if grant_type &#x3D; &#x60;refresh_token&#x60;. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetOauth2Token200Response**](../Model/GetOauth2Token200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOauth2TokenRevoke()`

```php
getOauth2TokenRevoke($authorization, $token, $token_hint): \OpenAPI\Client\Model\GetOauth2TokenRevoke200Response
```

Revoke an existing access or refresh token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\Oauth2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$authorization = 'authorization_example'; // string | OAuth2 client credentials in the Basic authorization format.
$token = 'token_example'; // string
$token_hint = 'token_hint_example'; // string

try {
    $result = $apiInstance->getOauth2TokenRevoke($authorization, $token, $token_hint);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling Oauth2Api->getOauth2TokenRevoke: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **authorization** | **string**| OAuth2 client credentials in the Basic authorization format. | |
| **token** | **string**|  | |
| **token_hint** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetOauth2TokenRevoke200Response**](../Model/GetOauth2TokenRevoke200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
