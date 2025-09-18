# DashboardTemplateResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user to whom this dashboard belongs | [optional] 
**name** | **string** | The name of the dashboard. | [optional] 
**description** | **string** | A short description of the dashboard. | [optional] 
**public** | **bool** | Determines if the template can be added by downstream users | [optional] 
**options** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A number of custom field values for this dashboard. | [optional] 
**widgets** | [**\Swagger\Client\Model\DashboardWidgetDictionary**](DashboardWidgetDictionary.md) | A dictionary of the widgets in this dashboard | [optional] 
**state** | **string** | The state of dashboard template | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


