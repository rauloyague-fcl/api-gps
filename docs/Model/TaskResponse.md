# TaskResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | A unique GUID for the task | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company that owns this task | 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user that created this task (optional) | [optional] 
**linked** | [**\Swagger\Client\Model\IdNameType[]**](IdNameType.md) | A number of entities that are linked to this task | 
**options** | [**\Swagger\Client\Model\TaskOptions**](TaskOptions.md) | A number of task execution options | 
**state** | **string** | The state of the task | 
**date** | [**\Swagger\Client\Model\TaskDates**](TaskDates.md) | Date information | 
**type** | **string** | The type of the task | 
**data** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A number of task specific options | 
**results** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A number of task specific results | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


