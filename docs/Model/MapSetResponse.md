# MapSetResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A unique name for this map set | [optional] 
**layers** | [**\Swagger\Client\Model\MapSetLayer[]**](MapSetLayer.md) | One or more layers available in this map set | [optional] 
**state** | **string** | The state of this map set | [optional] 
**overlays** | [**\Swagger\Client\Model\MapSetLayer[]**](MapSetLayer.md) | One or more overlays for this map set | [optional] 
**static_map_url** | **string** | The url to use for static maps when this map set is selected | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


