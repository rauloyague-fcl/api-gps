# LabelResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**label** | **string** | A lowercase alphanumeric label value | [optional] 
**name** | **string** | A friendly descriptive name for label | [optional] 
**color** | **string** | An optional color for this label | [optional] 
**state** | **string** | The current state of this entity | [optional] 
**values** | [**\Swagger\Client\Model\LabelValuePayload[]**](LabelValuePayload.md) | A list of sub labels that are mutually exclusive | [optional] 
**entities** | **string[]** | The entities to which this label applies | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


