# OpenAPIClient-php

Note: This is a (Limited Release) API available only to select developers approved by business units. Enables a seller adding an ad or item on a Partner's site to automatically create an eBay listing draft using the item details from the Partner's site.


## Installation & Usage

### Requirements

PHP 7.2 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github/zvps/ebay-sell-listing-php-client.git"
    }
  ],
  "require": {
    "zvps/ebay-sell-listing-php-client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure OAuth2 access token for authorization: Authorization Code
$config = Ebay\Sell\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Ebay\Sell\Api\ItemDraftApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_ebay_c_marketplace_id = 'x_ebay_c_marketplace_id_example'; // string | Use this header to specify an eBay marketplace ID. For a list of supported sites, see API Restrictions in the Listing API overview.
$content_language = 'content_language_example'; // string | Use this header to specify the natural language of the seller. For details, see Content-Language in HTTP request headers. Required: For EBAY_CA in French. (Content-Language = fr-CA)
$body = new \Ebay\Sell\Listing\Model\ItemDraft(); // \Ebay\Sell\Listing\Model\ItemDraft

try {
    $result = $apiInstance->createItemDraft($x_ebay_c_marketplace_id, $content_language, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemDraftApi->createItemDraft: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.ebay.com/sell/listing/v1_beta*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ItemDraftApi* | [**createItemDraft**](docs/Api/ItemDraftApi.md#createitemdraft) | **POST** /item_draft/ | 

## Models

- [Amount](docs/Model/Amount.md)
- [Aspect](docs/Model/Aspect.md)
- [Charity](docs/Model/Charity.md)
- [ItemDraft](docs/Model/ItemDraft.md)
- [ItemDraftResponse](docs/Model/ItemDraftResponse.md)
- [PricingSummary](docs/Model/PricingSummary.md)
- [Product](docs/Model/Product.md)

## Authorization

### Authorization Code

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://auth.ebay.com/oauth2/authorize`
- **Scopes**: 
    - **https://api.ebay.com/oauth/api_scope/sell.item.draft**: View and manage your item drafts.

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v1_beta.3.0`
    - Package version: `5.0.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
