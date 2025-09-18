# DeviceListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID for this device | 
**name** | **string** | The serial or IMEI of the device that is used to uniquely identify it. The value used will depend on the device type. | 
**owner** | [**\Swagger\Client\Model\IdName**](IdName.md) | The client that owns this device | 
**device_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of device | [optional] 
**provider** | [**\Swagger\Client\Model\IdName**](IdName.md) | The device provider, if the device requires one to function. | [optional] 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset to which this device has been assigned. | [optional] 
**simcard** | [**\Swagger\Client\Model\IdName**](IdName.md) | The sim card which has been assigned to this device. | [optional] 
**config_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The config profile which has been assigned to this device. | [optional] 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this device. | 
**state** | **string** | The current state of the device object | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


