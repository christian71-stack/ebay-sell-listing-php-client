# # Product

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**aspects** | [**\Ebay\Sell\Listing\Model\Aspect[]**](Aspect.md) | The list of item aspects that describe the item (such as size, color, capacity, model, brand, etc.) | [optional]
**brand** | **string** | The name brand of the item, such as Nike, Apple, etc. | [optional]
**description** | **string** | The description of the item that was created by the seller. This field supports plain text or rich content within HTML tags. Note: Active content is not supported. Active content includes animation or video via JavaScript, Flash, plug-ins, or form actions. Max Length: 500,000 | [optional]
**epid** | **string** | An EPID is the eBay product identifier of a product from the eBay product catalog. Note: If you submit both a category ID and an EPID, eBay determines the best category based on the EPID and uses that. The category ID will be ignored. | [optional]
**image_urls** | **string[]** | The image URLs of the item. The first URL will be the primary image, which appears on the View Item page in the eBay listing. The URL can be from the following: The eBay Picture Services (images previously uploaded). A server outside of eBay (self-hosted). For more details, see PictureURL and Introduction to Pictures in Listings. Maximum: 12 URLs (for most categories and marketplaces) Restrictions: You cannot mix self-hosted and EPS-hosted URLs in the same listing. All image URLs must be &#39;https&#39;. | [optional]
**title** | **string** | The seller-created title of the item. This should include unique characteristics of the item, such as brand, model, color, size, capacity, etc. For example: Levi&#39;s 501 size 10 black jeans | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
