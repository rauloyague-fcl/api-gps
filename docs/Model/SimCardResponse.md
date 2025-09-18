# SimCardResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | The serial number of the SIM card that is used to uniquely identify it. | [optional] 
**network_name** | **string** | The name of the telecommunications network. | [optional] 
**number** | **string** | The direct mobile number for this SIM card. Must be in international format starting with +. | [optional] 
**description** | **string** | A short description of the sim card. | [optional] 
**state** | **string** | The current state of the object | [optional] 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this simcard. | [optional] 
**device** | [**\Swagger\Client\Model\IdName**](IdName.md) | The device to which this SIM card has been assigned.  Can only be modified using the &#x60;updateDevice&#x60; operation. | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


