# DeviceConfigProfileResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**device_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The device type that this profile applies to | [optional] 
**parameters** | [**\Swagger\Client\Model\DeviceParameters**](DeviceParameters.md) | A number of device specific parameters | [optional] 
**settings** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | Values for the DeviceType&#39;s setting definition form | [optional] 
**accessories** | [**\Swagger\Client\Model\DeviceAccessories**](DeviceAccessories.md) | Accessory settings for this device | [optional] 
**name** | **string** | A unique name for this entity | [optional] 
**state** | **string** | The current state of this entity | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 
**features** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A number of features that have been enabled on this device | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


