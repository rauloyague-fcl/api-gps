# AlertResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A unique name for this alert | [optional] 
**state** | **string** | The current state of this alert | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre that this alert applies to | [optional] 
**priority** | **string** | The priority of this alert | [optional] 
**filter** | [**\Swagger\Client\Model\EventFilter**](EventFilter.md) | The filter that this alert matches on | [optional] 
**notify** | [**\Swagger\Client\Model\AlertNotify[]**](AlertNotify.md) | A list of users and roles that will be notified if this alert triggers. | [optional] 
**actions** | [**\Swagger\Client\Model\AlertAction[]**](AlertAction.md) | A list of actions to be performed once this alert triggers. | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


