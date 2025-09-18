# DeviceTypeListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A unique name for this entity | [optional] 
**short_name** | **string** | A short name for this device type (usually just a model number) | [optional] 
**parent** | [**\Swagger\Client\Model\IdName**](IdName.md) | The parent of this entity | [optional] 
**tag** | **string** | A unique tag for this entity | [optional] 
**state** | **string** | The current state of the device type object | [optional] 
**device_provider_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | An optional link to a device provider that supplies the data for this device type. If this is set, the user will be  required to select the device provider on device configuration. | [optional] 
**modified_date** | **string** | The date the entity was last modified | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


