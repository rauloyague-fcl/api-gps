# DashboardListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID for this Dashboard | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The client that owns this Dashboard | 
**parent** | [**\Swagger\Client\Model\IdName**](IdName.md) | The template dashboard from which this dashboard was constructed. This dashboard will track  all of the widgets on the parent dashboard. | [optional] 
**source** | [**\Swagger\Client\Model\IdName**](IdName.md) | The source dashboard if this dashboard was cloned from another. | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre the dashboard belongs to | [optional] 
**level** | **string** | The company level the dashboard is intended for | [optional] 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user to whom this dashboard belongs | 
**name** | **string** | The name of the dashboard. | 
**options** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A number of custom field values for this dashboard. | [optional] 
**public** | **bool** | Whethere or not other users can see the dashboard | 
**description** | **string** | A short description of the dashboard. | 
**modified_date** | **string** | The date the entity was last modified | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


