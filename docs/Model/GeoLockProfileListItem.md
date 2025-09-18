# GeoLockProfileListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A unique name for this entity | [optional] 
**state** | **string** | The current state of this entity | [optional] 
**radius_km** | **double** | The radius of the geo lock (in kilometers) | [optional] 
**times** | [**\Swagger\Client\Model\GeoLockTimeItem[]**](GeoLockTimeItem.md) | The geo lock times for this profile | [optional] 
**modified_date** | **string** | The date the entity was last modified | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


