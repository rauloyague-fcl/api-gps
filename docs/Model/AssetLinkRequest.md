# AssetLinkRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **string** | The destination UUID of an existing asset. This asset must not be already linked, nor have any devices linked to it. | [optional] 
**asset** | [**\Swagger\Client\Model\AssetCreateRequest**](AssetCreateRequest.md) | Details of a new asset to create and link. Cannot be used with &#39;destinationAddressId&#39;. | [optional] 
**start** | **string** | The ISO date/time when the linkage should start | 
**end** | **string** | The ISO date/time when the linkage should end | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


