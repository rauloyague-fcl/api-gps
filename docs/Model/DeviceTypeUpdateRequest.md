# DeviceTypeUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | A unique name for this entity | [optional] 
**short_name** | **string** | A short name for this device type (usually just a model number) | [optional] 
**parent** | [**\Swagger\Client\Model\IdName**](IdName.md) | The parent of this entity | [optional] 
**tag** | **string** | A unique tag for this entity | [optional] 
**state** | **string** | The current state of the device type object | [optional] 
**device_provider_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | An optional link to a device provider that supplies the data for this device type. If this is set, the user will be  required to select the device provider on device configuration. | [optional] 
**io_capabilities** | [**\Swagger\Client\Model\DeviceTypeIOCapabilities**](DeviceTypeIOCapabilities.md) | Defines the types of IOs that are available on this device type | [optional] 
**settings_definition** | **string** | A form definition for custom settings in this device type | [optional] 
**accessories** | [**\Swagger\Client\Model\DeviceTypeAccessories**](DeviceTypeAccessories.md) | A list of available accessories for this device type | [optional] 
**features** | [**\Swagger\Client\Model\DeviceTypeFeatures**](DeviceTypeFeatures.md) | A map of features for this device type | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


