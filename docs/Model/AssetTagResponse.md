# AssetTagResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A friendly name to identify this tag | [optional] 
**serial_number** | **string** | The serial number of the Asset Tag that is used to uniquely identify it. | [optional] 
**asset_tag_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of asset tag | [optional] 
**mode** | **string** | The asset tag operation mode. Options are &#39;movable&#39; for movable assets, &#39;fixed&#39; for fixed assets and &#39;stock&#39; for temporary stock control uses. | [optional] 
**state** | **string** | The current state of the object | [optional] 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset to which this tag is currently assigned | [optional] 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this assettag. | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


