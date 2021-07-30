# Ebay\Sell\Listing\ItemDraftApi

All URIs are relative to https://api.ebay.com/sell/listing/v1_beta.

Method | HTTP request | Description
------------- | ------------- | -------------
[**createItemDraft()**](ItemDraftApi.md#createItemDraft) | **POST** /item_draft/ | 


## `createItemDraft()`

```php
createItemDraft($x_ebay_c_marketplace_id, $content_language, $body): \Ebay\Sell\Listing\Model\ItemDraftResponse
```



This call gives Partners the ability to create an eBay draft of a item for their seller using information from their site. This lets the Partner increase the exposure of items on their site and leverage the eBay user listing experience seamlessly. This experience provides guidance on pricing, aspects, etc. and recommendations that help create a listing that is complete and improves the exposure of the listing in search results. After the listing draft is created, the seller logs into their eBay account and uses the listing experience to finish the listing and publish the item on eBay.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Authorization Code
$config = Ebay\Sell\Listing\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Ebay\Sell\Listing\Api\ItemDraftApi(
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

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_ebay_c_marketplace_id** | **string**| Use this header to specify an eBay marketplace ID. For a list of supported sites, see API Restrictions in the Listing API overview. |
 **content_language** | **string**| Use this header to specify the natural language of the seller. For details, see Content-Language in HTTP request headers. Required: For EBAY_CA in French. (Content-Language &#x3D; fr-CA) | [optional]
 **body** | [**\Ebay\Sell\Listing\Model\ItemDraft**](../Model/ItemDraft.md)|  | [optional]

### Return type

[**\Ebay\Sell\Listing\Model\ItemDraftResponse**](../Model/ItemDraftResponse.md)

### Authorization

[Authorization Code](../../README.md#Authorization Code)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
