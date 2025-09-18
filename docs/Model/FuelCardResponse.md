# FuelCardResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | The serial number of the fuel card that is used to uniquely identify it. | [optional] 
**brand_name** | **string** | The brand of fuel card | [optional] 
**embossed_name** | **string** | The name embossed on the fuel card | [optional] 
**expiry_date** | **string** | The expiry date of the fuel card in the format YYYY/MM/DD | [optional] 
**description** | **string** | A short description of the fuel card. | [optional] 
**state** | **string** | The current state of the object | [optional] 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this fuelcard. | [optional] 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset to which this fuel card has been assigned. | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


