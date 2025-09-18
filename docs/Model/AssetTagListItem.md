# AssetTagListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID for this Asset Tag | 
**owner** | [**\Swagger\Client\Model\IdName**](IdName.md) | The client that owns this Asset Tag | 
**name** | **string** | The serial number of the Asset Tag that is used to uniquely identify it. | 
**serial_number** | **string** | The serial number of the Asset Tag that is used to uniquely identify it. | 
**asset_tag_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of asset tag | 
**mode** | **string** | The asset tag operation mode. Options are &#39;movable&#39; for movable assets, &#39;fixed&#39; for fixed assets and &#39;stock&#39; for temporary stock control uses. | 
**state** | **string** | The current state of the object | 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset to which this tag is currently assigned | 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this assettag. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


