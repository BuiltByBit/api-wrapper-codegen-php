# YourApiClient

All operations not tagged 'free' require an active [Ultimate](https://builtbybit.com/account/ultimate) subscription or invite-only permissions.

For more information, please visit [https://builtbybit.com/ticket](https://builtbybit.com/ticket).

## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/BuiltByBit/api-wrapper-codegen-php.git"
    }
  ],
  "require": {
    "BuiltByBit/api-wrapper-codegen-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/YourApiClient/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://api.builtbybit.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**getV2Analytics**](docs/Api/DefaultApi.md#getv2analytics) | **GET** /v2/analytics | Fetch a list of analytics definitions
*DefaultApi* | [**getV2AnalyticsGraph**](docs/Api/DefaultApi.md#getv2analyticsgraph) | **GET** /v2/analytics/graph | Fetch analytics graph data
*DefaultApi* | [**getV2Events**](docs/Api/DefaultApi.md#getv2events) | **GET** /v2/events | Fetch a list of pending events
*DefaultApi* | [**postV2EventsComplete**](docs/Api/DefaultApi.md#postv2eventscomplete) | **POST** /v2/events/complete | Mark events as complete
*DefaultApi* | [**postV2ResourcesCreatorUpdate**](docs/Api/DefaultApi.md#postv2resourcescreatorupdate) | **POST** /v2/resources/creator/update | Post a resource update
*DiscoveryApi* | [**getResourcesDiscoverCategories**](docs/Api/DiscoveryApi.md#getresourcesdiscovercategories) | **GET** /v2/resources/discover/categories | Fetch a list of categories
*DiscoveryApi* | [**getResourcesDiscoverResources**](docs/Api/DiscoveryApi.md#getresourcesdiscoverresources) | **GET** /v2/resources/discover/resources | Fetch a list of resources
*DiscoveryApi* | [**getV2ResourcesDiscoverCartView**](docs/Api/DiscoveryApi.md#getv2resourcesdiscovercartview) | **GET** /v2/resources/discover/cart/view | View the user&#39;s cart items
*DiscoveryApi* | [**getV2ResourcesDiscoverLicenses**](docs/Api/DiscoveryApi.md#getv2resourcesdiscoverlicenses) | **GET** /v2/resources/discover/licenses | Fetch a list of the user&#39;s licenses
*DiscoveryApi* | [**postV2ResourcesDiscoverCartAdd**](docs/Api/DiscoveryApi.md#postv2resourcesdiscovercartadd) | **POST** /v2/resources/discover/cart/add | Add items to a user&#39;s cart
*DiscoveryApi* | [**postV2ResourcesDiscoverCartCheckout**](docs/Api/DiscoveryApi.md#postv2resourcesdiscovercartcheckout) | **POST** /v2/resources/discover/cart/checkout | Initiate a checkout of a user&#39;s cart
*DiscoveryApi* | [**postV2ResourcesDiscoverCartCouponAdd**](docs/Api/DiscoveryApi.md#postv2resourcesdiscovercartcouponadd) | **POST** /v2/resources/discover/cart/coupon/add | Add a coupon to the user&#39;s cart
*DiscoveryApi* | [**postV2ResourcesDiscoverCartCouponRemove**](docs/Api/DiscoveryApi.md#postv2resourcesdiscovercartcouponremove) | **POST** /v2/resources/discover/cart/coupon/remove | Remove a coupon from the user&#39;s cart
*DiscoveryApi* | [**postV2ResourcesDiscoverCartRemove**](docs/Api/DiscoveryApi.md#postv2resourcesdiscovercartremove) | **POST** /v2/resources/discover/cart/remove | Remove an item from the user&#39;s cart
*Oauth2Api* | [**getOauth2Token**](docs/Api/Oauth2Api.md#getoauth2token) | **POST** /oauth2/token | Request an access token using an existing grant
*Oauth2Api* | [**getOauth2TokenRevoke**](docs/Api/Oauth2Api.md#getoauth2tokenrevoke) | **POST** /oauth2/token/revoke | Revoke an existing access or refresh token

## Models

- [Addon](docs/Model/Addon.md)
- [Analytic](docs/Model/Analytic.md)
- [AnalyticGraphData](docs/Model/AnalyticGraphData.md)
- [AnalyticGraphDataPeriod](docs/Model/AnalyticGraphDataPeriod.md)
- [AnalyticGraphDataPoint](docs/Model/AnalyticGraphDataPoint.md)
- [CartItem](docs/Model/CartItem.md)
- [CartItemDiscountsInner](docs/Model/CartItemDiscountsInner.md)
- [CartSummary](docs/Model/CartSummary.md)
- [Category](docs/Model/Category.md)
- [Description](docs/Model/Description.md)
- [Event](docs/Model/Event.md)
- [Filter](docs/Model/Filter.md)
- [FilterChoice](docs/Model/FilterChoice.md)
- [FilterValue](docs/Model/FilterValue.md)
- [GetOauth2Token200Response](docs/Model/GetOauth2Token200Response.md)
- [GetOauth2TokenRevoke200Response](docs/Model/GetOauth2TokenRevoke200Response.md)
- [GetResourcesDiscoverCategories200Response](docs/Model/GetResourcesDiscoverCategories200Response.md)
- [GetResourcesDiscoverCategories200ResponseData](docs/Model/GetResourcesDiscoverCategories200ResponseData.md)
- [GetResourcesDiscoverResources200Response](docs/Model/GetResourcesDiscoverResources200Response.md)
- [GetResourcesDiscoverResources200ResponseData](docs/Model/GetResourcesDiscoverResources200ResponseData.md)
- [GetResourcesDiscoverResources4XXResponse](docs/Model/GetResourcesDiscoverResources4XXResponse.md)
- [GetResourcesDiscoverResources4XXResponseError](docs/Model/GetResourcesDiscoverResources4XXResponseError.md)
- [GetV2Analytics200Response](docs/Model/GetV2Analytics200Response.md)
- [GetV2Analytics200ResponseData](docs/Model/GetV2Analytics200ResponseData.md)
- [GetV2AnalyticsGraph200Response](docs/Model/GetV2AnalyticsGraph200Response.md)
- [GetV2Events200Response](docs/Model/GetV2Events200Response.md)
- [GetV2Events200ResponseData](docs/Model/GetV2Events200ResponseData.md)
- [GetV2ResourcesDiscoverCartView200Response](docs/Model/GetV2ResourcesDiscoverCartView200Response.md)
- [GetV2ResourcesDiscoverCartView200ResponseData](docs/Model/GetV2ResourcesDiscoverCartView200ResponseData.md)
- [GetV2ResourcesDiscoverLicenses200Response](docs/Model/GetV2ResourcesDiscoverLicenses200Response.md)
- [GetV2ResourcesDiscoverLicenses200ResponseData](docs/Model/GetV2ResourcesDiscoverLicenses200ResponseData.md)
- [License](docs/Model/License.md)
- [ListStats](docs/Model/ListStats.md)
- [Member](docs/Model/Member.md)
- [PostV2EventsComplete200Response](docs/Model/PostV2EventsComplete200Response.md)
- [PostV2EventsCompleteRequest](docs/Model/PostV2EventsCompleteRequest.md)
- [PostV2ResourcesCreatorUpdate200Response](docs/Model/PostV2ResourcesCreatorUpdate200Response.md)
- [PostV2ResourcesCreatorUpdate200ResponseData](docs/Model/PostV2ResourcesCreatorUpdate200ResponseData.md)
- [PostV2ResourcesCreatorUpdateRequest](docs/Model/PostV2ResourcesCreatorUpdateRequest.md)
- [PostV2ResourcesCreatorUpdateRequestFile](docs/Model/PostV2ResourcesCreatorUpdateRequestFile.md)
- [PostV2ResourcesCreatorUpdateRequestUpdate](docs/Model/PostV2ResourcesCreatorUpdateRequestUpdate.md)
- [PostV2ResourcesDiscoverCartAdd2XXResponse](docs/Model/PostV2ResourcesDiscoverCartAdd2XXResponse.md)
- [PostV2ResourcesDiscoverCartAddRequest](docs/Model/PostV2ResourcesDiscoverCartAddRequest.md)
- [PostV2ResourcesDiscoverCartCheckout200Response](docs/Model/PostV2ResourcesDiscoverCartCheckout200Response.md)
- [PostV2ResourcesDiscoverCartCheckout200ResponseData](docs/Model/PostV2ResourcesDiscoverCartCheckout200ResponseData.md)
- [PostV2ResourcesDiscoverCartCouponAdd200Response](docs/Model/PostV2ResourcesDiscoverCartCouponAdd200Response.md)
- [PostV2ResourcesDiscoverCartCouponAddRequest](docs/Model/PostV2ResourcesDiscoverCartCouponAddRequest.md)
- [PostV2ResourcesDiscoverCartCouponRemove200Response](docs/Model/PostV2ResourcesDiscoverCartCouponRemove200Response.md)
- [PostV2ResourcesDiscoverCartCouponRemoveRequest](docs/Model/PostV2ResourcesDiscoverCartCouponRemoveRequest.md)
- [PostV2ResourcesDiscoverCartRemove200Response](docs/Model/PostV2ResourcesDiscoverCartRemove200Response.md)
- [PostV2ResourcesDiscoverCartRemoveRequest](docs/Model/PostV2ResourcesDiscoverCartRemoveRequest.md)
- [Resource](docs/Model/Resource.md)
- [Review](docs/Model/Review.md)
- [SaleEvent](docs/Model/SaleEvent.md)
- [SaleEventEntry](docs/Model/SaleEventEntry.md)
- [Update](docs/Model/Update.md)
- [Version](docs/Model/Version.md)

## Authorization

Authentication schemes defined for the API:
### token

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v2`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
