# # ItemDraftResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**item_draft_id** | **string** | The eBay generated ID of the listing draft. | [optional]
**sell_flow_native_uri** | **string** | The URI the Partner uses to send the seller to their listing draft that was created on the eBay site. From there the seller can change, update, and publish the item on eBay. This is returned when the seller is using a mobile app. | [optional]
**sell_flow_url** | **string** | The web URL the Partner uses to send the seller to the listing draft that was created on the eBay site. From there the seller can change, update, and publish the item on eBay. This is returned when the seller is using mobile web (mweb) or the desktop web. Note: You must construct the URL using the URL returned in this field and a session token. For example: sellFlowUrl?id_token&#x3D;session_token | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
