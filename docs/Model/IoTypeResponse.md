# IoTypeResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A unique name for this entity | [optional] 
**state** | **string** | The current state of this entity | [optional] 
**type** | **string** | The type of the IO type | [optional] 
**unit** | **string** | Optional units that this I/O type is measured in | [optional] 
**smoothing_type** | **string** | The type of smoothing to apply to this input | [optional] 
**text** | [**\Swagger\Client\Model\IoTypeTextConfig**](IoTypeTextConfig.md) | Digital types can have their value substituted with the following text | [optional] 
**rate** | [**\Swagger\Client\Model\IoTypeRateConfig**](IoTypeRateConfig.md) | An optional rate conversion to do on this value | [optional] 
**lookups** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | A dictionary of lookup values. Only relevant for \&quot;value_input\&quot; types. | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


