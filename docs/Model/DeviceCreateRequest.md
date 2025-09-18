# DeviceCreateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**device_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of device | 
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
**owner_id** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


