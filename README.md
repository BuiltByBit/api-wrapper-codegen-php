# builtbybit/api-wrapper-codegen-php

All operations not tagged 'free' require an active [Ultimate](https://builtbybit.com/account/ultimate) subscription or invite-only permissions.

V2 documentation: https://builtbybit.com/wiki/api-v2/ \\
OAuth2 documentation: https://builtbybit.com/wiki/oauth2/

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
require_once('/path/to/builtbybit/api-wrapper-codegen-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AnalyticsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getV2Analytics();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsApi->getV2Analytics: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.builtbybit.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AnalyticsApi* | [**getV2Analytics**](docs/Api/AnalyticsApi.md#getv2analytics) | **GET** /v2/analytics | Fetch a list of analytics definitions
*AnalyticsApi* | [**getV2AnalyticsGraph**](docs/Api/AnalyticsApi.md#getv2analyticsgraph) | **GET** /v2/analytics/graph | Fetch analytics graph data
*AnalyticsApi* | [**getV2AnalyticsSingle**](docs/Api/AnalyticsApi.md#getv2analyticssingle) | **GET** /v2/analytics/single | Fetch a single analytics value
*EventsApi* | [**getV2Events**](docs/Api/EventsApi.md#getv2events) | **GET** /v2/events | Fetch a list of pending events
*EventsApi* | [**postV2EventsComplete**](docs/Api/EventsApi.md#postv2eventscomplete) | **POST** /v2/events/complete | Mark events as complete
*HealthApi* | [**getV2Health**](docs/Api/HealthApi.md#getv2health) | **GET** /v2/health | Retrieve a health status
*Oauth2Api* | [**getOauth2Token**](docs/Api/Oauth2Api.md#getoauth2token) | **POST** /oauth2/token | Request an access token using an existing grant
*Oauth2Api* | [**getOauth2TokenRevoke**](docs/Api/Oauth2Api.md#getoauth2tokenrevoke) | **POST** /oauth2/token/revoke | Revoke an existing access or refresh token
*ResourcesBuyerApi* | [**getV2ResourcesBuyerLatest**](docs/Api/ResourcesBuyerApi.md#getv2resourcesbuyerlatest) | **GET** /v2/resources/buyer/latest | Fetches the latest versions &amp; license information
*ResourcesCreatorApi* | [**getV2ResourcesCreatorAddons**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatoraddons) | **GET** /v2/resources/creator/addons | Fetch a list of your resources&#39; addons
*ResourcesCreatorApi* | [**getV2ResourcesCreatorBatch**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorbatch) | **GET** /v2/resources/creator/batch | Fetch a list of your batches edits
*ResourcesCreatorApi* | [**getV2ResourcesCreatorBundles**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorbundles) | **GET** /v2/resources/creator/bundles | Fetch a list of your bundles
*ResourcesCreatorApi* | [**getV2ResourcesCreatorBundlesEntries**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorbundlesentries) | **GET** /v2/resources/creator/bundles/entries | Fetch a list of your bundle entries
*ResourcesCreatorApi* | [**getV2ResourcesCreatorCoupons**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorcoupons) | **GET** /v2/resources/creator/coupons | Fetch a list of your coupons
*ResourcesCreatorApi* | [**getV2ResourcesCreatorCouponsEntries**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorcouponsentries) | **GET** /v2/resources/creator/coupons/entries | Fetch a list of your coupon entries
*ResourcesCreatorApi* | [**getV2ResourcesCreatorLicenses**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorlicenses) | **GET** /v2/resources/creator/licenses | Fetch a list of your resources&#39; licenses
*ResourcesCreatorApi* | [**getV2ResourcesCreatorPurchases**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorpurchases) | **GET** /v2/resources/creator/purchases | Fetch a list of your resources&#39; purchases
*ResourcesCreatorApi* | [**getV2ResourcesCreatorResources**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorresources) | **GET** /v2/resources/creator/resources | Fetch a list of your resources
*ResourcesCreatorApi* | [**getV2ResourcesCreatorReviews**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorreviews) | **GET** /v2/resources/creator/reviews | Fetch a list of your resources&#39; reviews
*ResourcesCreatorApi* | [**getV2ResourcesCreatorSaleEvents**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorsaleevents) | **GET** /v2/resources/creator/sale-events | Fetch a list of your sale events
*ResourcesCreatorApi* | [**getV2ResourcesCreatorSaleEventsEntries**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorsaleeventsentries) | **GET** /v2/resources/creator/sale-events/entries | Fetch a list of your sale event entries
*ResourcesCreatorApi* | [**getV2ResourcesCreatorStores**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorstores) | **GET** /v2/resources/creator/stores | Fetch a list of your stores
*ResourcesCreatorApi* | [**getV2ResourcesCreatorUpdates**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorupdates) | **GET** /v2/resources/creator/updates | Fetch a list of your resource&#39;s updates
*ResourcesCreatorApi* | [**getV2ResourcesCreatorVersions**](docs/Api/ResourcesCreatorApi.md#getv2resourcescreatorversions) | **GET** /v2/resources/creator/versions | Fetch a list of your resources&#39; versions
*ResourcesCreatorApi* | [**postV2ResourcesCreatorBatch**](docs/Api/ResourcesCreatorApi.md#postv2resourcescreatorbatch) | **POST** /v2/resources/creator/batch | Submit a new batch edit
*ResourcesCreatorApi* | [**postV2ResourcesCreatorCoupons**](docs/Api/ResourcesCreatorApi.md#postv2resourcescreatorcoupons) | **POST** /v2/resources/creator/coupons | Create a new coupon
*ResourcesCreatorApi* | [**postV2ResourcesCreatorUpdate**](docs/Api/ResourcesCreatorApi.md#postv2resourcescreatorupdate) | **POST** /v2/resources/creator/update | Post a resource update
*ResourcesDiscoveryApi* | [**getResourcesDiscoverCategories**](docs/Api/ResourcesDiscoveryApi.md#getresourcesdiscovercategories) | **GET** /v2/resources/discover/categories | Fetch a list of categories
*ResourcesDiscoveryApi* | [**getResourcesDiscoverResources**](docs/Api/ResourcesDiscoveryApi.md#getresourcesdiscoverresources) | **GET** /v2/resources/discover/resources | Fetch a list of resources
*ResourcesDiscoveryApi* | [**getV2ResourcesDiscoverCartView**](docs/Api/ResourcesDiscoveryApi.md#getv2resourcesdiscovercartview) | **GET** /v2/resources/discover/cart/view | View the user&#39;s cart items
*ResourcesDiscoveryApi* | [**getV2ResourcesDiscoverLicenses**](docs/Api/ResourcesDiscoveryApi.md#getv2resourcesdiscoverlicenses) | **GET** /v2/resources/discover/licenses | Fetch a list of the user&#39;s licenses
*ResourcesDiscoveryApi* | [**postV2ResourcesDiscoverCartAdd**](docs/Api/ResourcesDiscoveryApi.md#postv2resourcesdiscovercartadd) | **POST** /v2/resources/discover/cart/add | Add items to a user&#39;s cart
*ResourcesDiscoveryApi* | [**postV2ResourcesDiscoverCartCheckout**](docs/Api/ResourcesDiscoveryApi.md#postv2resourcesdiscovercartcheckout) | **POST** /v2/resources/discover/cart/checkout | Initiate a checkout of a user&#39;s cart
*ResourcesDiscoveryApi* | [**postV2ResourcesDiscoverCartCouponAdd**](docs/Api/ResourcesDiscoveryApi.md#postv2resourcesdiscovercartcouponadd) | **POST** /v2/resources/discover/cart/coupon/add | Add a coupon to the user&#39;s cart
*ResourcesDiscoveryApi* | [**postV2ResourcesDiscoverCartCouponRemove**](docs/Api/ResourcesDiscoveryApi.md#postv2resourcesdiscovercartcouponremove) | **POST** /v2/resources/discover/cart/coupon/remove | Remove a coupon from the user&#39;s cart
*ResourcesDiscoveryApi* | [**postV2ResourcesDiscoverCartRemove**](docs/Api/ResourcesDiscoveryApi.md#postv2resourcesdiscovercartremove) | **POST** /v2/resources/discover/cart/remove | Remove an item from the user&#39;s cart

## Models

- [Addon](docs/Model/Addon.md)
- [Analytic](docs/Model/Analytic.md)
- [AnalyticFiltersValue](docs/Model/AnalyticFiltersValue.md)
- [AnalyticGraphData](docs/Model/AnalyticGraphData.md)
- [AnalyticGraphDataPeriod](docs/Model/AnalyticGraphDataPeriod.md)
- [AnalyticGraphDataPoint](docs/Model/AnalyticGraphDataPoint.md)
- [Batch](docs/Model/Batch.md)
- [Bundle](docs/Model/Bundle.md)
- [BundleEntry](docs/Model/BundleEntry.md)
- [CartItem](docs/Model/CartItem.md)
- [CartItemDiscountsInner](docs/Model/CartItemDiscountsInner.md)
- [CartSummary](docs/Model/CartSummary.md)
- [Category](docs/Model/Category.md)
- [Coupon](docs/Model/Coupon.md)
- [CouponEntry](docs/Model/CouponEntry.md)
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
- [GetV2AnalyticsSingle200Response](docs/Model/GetV2AnalyticsSingle200Response.md)
- [GetV2AnalyticsSingle200ResponseData](docs/Model/GetV2AnalyticsSingle200ResponseData.md)
- [GetV2AnalyticsSingle200ResponseDataPeriod](docs/Model/GetV2AnalyticsSingle200ResponseDataPeriod.md)
- [GetV2Events200Response](docs/Model/GetV2Events200Response.md)
- [GetV2Events200ResponseData](docs/Model/GetV2Events200ResponseData.md)
- [GetV2Health200Response](docs/Model/GetV2Health200Response.md)
- [GetV2ResourcesBuyerLatest200Response](docs/Model/GetV2ResourcesBuyerLatest200Response.md)
- [GetV2ResourcesBuyerLatest200ResponseData](docs/Model/GetV2ResourcesBuyerLatest200ResponseData.md)
- [GetV2ResourcesCreatorAddons200Response](docs/Model/GetV2ResourcesCreatorAddons200Response.md)
- [GetV2ResourcesCreatorAddons200ResponseData](docs/Model/GetV2ResourcesCreatorAddons200ResponseData.md)
- [GetV2ResourcesCreatorBatch200Response](docs/Model/GetV2ResourcesCreatorBatch200Response.md)
- [GetV2ResourcesCreatorBatch200ResponseData](docs/Model/GetV2ResourcesCreatorBatch200ResponseData.md)
- [GetV2ResourcesCreatorBundles200Response](docs/Model/GetV2ResourcesCreatorBundles200Response.md)
- [GetV2ResourcesCreatorBundles200ResponseData](docs/Model/GetV2ResourcesCreatorBundles200ResponseData.md)
- [GetV2ResourcesCreatorBundlesEntries200Response](docs/Model/GetV2ResourcesCreatorBundlesEntries200Response.md)
- [GetV2ResourcesCreatorBundlesEntries200ResponseData](docs/Model/GetV2ResourcesCreatorBundlesEntries200ResponseData.md)
- [GetV2ResourcesCreatorCoupons200Response](docs/Model/GetV2ResourcesCreatorCoupons200Response.md)
- [GetV2ResourcesCreatorCoupons200ResponseData](docs/Model/GetV2ResourcesCreatorCoupons200ResponseData.md)
- [GetV2ResourcesCreatorCouponsEntries200Response](docs/Model/GetV2ResourcesCreatorCouponsEntries200Response.md)
- [GetV2ResourcesCreatorCouponsEntries200ResponseData](docs/Model/GetV2ResourcesCreatorCouponsEntries200ResponseData.md)
- [GetV2ResourcesCreatorLicenses200Response](docs/Model/GetV2ResourcesCreatorLicenses200Response.md)
- [GetV2ResourcesCreatorLicenses200ResponseData](docs/Model/GetV2ResourcesCreatorLicenses200ResponseData.md)
- [GetV2ResourcesCreatorPurchases200Response](docs/Model/GetV2ResourcesCreatorPurchases200Response.md)
- [GetV2ResourcesCreatorPurchases200ResponseData](docs/Model/GetV2ResourcesCreatorPurchases200ResponseData.md)
- [GetV2ResourcesCreatorResources200Response](docs/Model/GetV2ResourcesCreatorResources200Response.md)
- [GetV2ResourcesCreatorResources200ResponseData](docs/Model/GetV2ResourcesCreatorResources200ResponseData.md)
- [GetV2ResourcesCreatorReviews200Response](docs/Model/GetV2ResourcesCreatorReviews200Response.md)
- [GetV2ResourcesCreatorReviews200ResponseData](docs/Model/GetV2ResourcesCreatorReviews200ResponseData.md)
- [GetV2ResourcesCreatorSaleEvents200Response](docs/Model/GetV2ResourcesCreatorSaleEvents200Response.md)
- [GetV2ResourcesCreatorSaleEvents200ResponseData](docs/Model/GetV2ResourcesCreatorSaleEvents200ResponseData.md)
- [GetV2ResourcesCreatorSaleEventsEntries200Response](docs/Model/GetV2ResourcesCreatorSaleEventsEntries200Response.md)
- [GetV2ResourcesCreatorSaleEventsEntries200ResponseData](docs/Model/GetV2ResourcesCreatorSaleEventsEntries200ResponseData.md)
- [GetV2ResourcesCreatorStores200Response](docs/Model/GetV2ResourcesCreatorStores200Response.md)
- [GetV2ResourcesCreatorStores200ResponseData](docs/Model/GetV2ResourcesCreatorStores200ResponseData.md)
- [GetV2ResourcesCreatorUpdates200Response](docs/Model/GetV2ResourcesCreatorUpdates200Response.md)
- [GetV2ResourcesCreatorUpdates200ResponseData](docs/Model/GetV2ResourcesCreatorUpdates200ResponseData.md)
- [GetV2ResourcesCreatorVersions200Response](docs/Model/GetV2ResourcesCreatorVersions200Response.md)
- [GetV2ResourcesCreatorVersions200ResponseData](docs/Model/GetV2ResourcesCreatorVersions200ResponseData.md)
- [GetV2ResourcesDiscoverCartView200Response](docs/Model/GetV2ResourcesDiscoverCartView200Response.md)
- [GetV2ResourcesDiscoverCartView200ResponseData](docs/Model/GetV2ResourcesDiscoverCartView200ResponseData.md)
- [GetV2ResourcesDiscoverLicenses200Response](docs/Model/GetV2ResourcesDiscoverLicenses200Response.md)
- [GetV2ResourcesDiscoverLicenses200ResponseData](docs/Model/GetV2ResourcesDiscoverLicenses200ResponseData.md)
- [License](docs/Model/License.md)
- [ListStats](docs/Model/ListStats.md)
- [Member](docs/Model/Member.md)
- [PostV2EventsComplete200Response](docs/Model/PostV2EventsComplete200Response.md)
- [PostV2EventsCompleteRequest](docs/Model/PostV2EventsCompleteRequest.md)
- [PostV2ResourcesCreatorBatch200Response](docs/Model/PostV2ResourcesCreatorBatch200Response.md)
- [PostV2ResourcesCreatorBatch200ResponseData](docs/Model/PostV2ResourcesCreatorBatch200ResponseData.md)
- [PostV2ResourcesCreatorBatchRequest](docs/Model/PostV2ResourcesCreatorBatchRequest.md)
- [PostV2ResourcesCreatorBatchRequestChangesInner](docs/Model/PostV2ResourcesCreatorBatchRequestChangesInner.md)
- [PostV2ResourcesCreatorCoupons200Response](docs/Model/PostV2ResourcesCreatorCoupons200Response.md)
- [PostV2ResourcesCreatorCoupons200ResponseData](docs/Model/PostV2ResourcesCreatorCoupons200ResponseData.md)
- [PostV2ResourcesCreatorCouponsRequest](docs/Model/PostV2ResourcesCreatorCouponsRequest.md)
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
- [Price](docs/Model/Price.md)
- [Purchase](docs/Model/Purchase.md)
- [Resource](docs/Model/Resource.md)
- [Review](docs/Model/Review.md)
- [RichText](docs/Model/RichText.md)
- [SaleEvent](docs/Model/SaleEvent.md)
- [SaleEventEntry](docs/Model/SaleEventEntry.md)
- [Store](docs/Model/Store.md)
- [Update](docs/Model/Update.md)
- [Version](docs/Model/Version.md)

## Authorization

Authentication schemes defined for the API:
### token

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


### oauth2

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://builtbybit.com/account/external/authorize`
- **Scopes**: N/A

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
