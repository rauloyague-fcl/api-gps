# DeviceResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**device_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The device type that this profile applies to | [optional] 
**parameters** | [**\Swagger\Client\Model\DeviceParameters**](DeviceParameters.md) | A number of device specific parameters | [optional] 
**settings** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | Values for the DeviceType&#39;s setting definition form | [optional] 
**accessories** | [**\Swagger\Client\Model\DeviceAccessories**](DeviceAccessories.md) | Accessory settings for this device | [optional] 
**name** | **string** | The serial or IMEI of the device that is used to uniquely identify it. The value used will depend on the device type. | [optional] 
**state** | **string** | The current state of the device object | [optional] 
**provider** | [**\Swagger\Client\Model\IdName**](IdName.md) | The device provider, if the device requires one to function. | [optional] 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset to which this device has been assigned. | [optional] 
**simcard** | [**\Swagger\Client\Model\IdName**](IdName.md) | The sim card which has been assigned to this device. | [optional] 
**config_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | An optional configuration profile | [optional] 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this device. | [optional] 
**features** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A number of features that have been enabled on this device (only available if configProfile is null) | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


