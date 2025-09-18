# DashboardUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user to whom this dashboard belongs | [optional] 
**name** | **string** | The name of the dashboard. | [optional] 
**description** | **string** | A short description of the dashboard. | [optional] 
**public** | **bool** | Whether or not other users can see the dashboard | [optional] 
**options** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A number of custom field values for this dashboard. | [optional] 
**widgets** | [**\Swagger\Client\Model\DashboardWidgetDictionary**](DashboardWidgetDictionary.md) | A dictionary of the widgets in this dashboard | [optional] 
**parent** | [**\Swagger\Client\Model\IdName**](IdName.md) | The template dashboard from which this dashboard was constructed. This dashboard will track  all of the widgets on the parent dashboard. | [optional] 
**source** | [**\Swagger\Client\Model\IdName**](IdName.md) | The source dashboard if this dashboard was cloned from another. | [optional] 
**level** | **string** | The company level of the dashboard target audience | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


