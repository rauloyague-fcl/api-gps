# DashboardWidget

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**inherited** | **bool** | Inherited widgets are tied to a parent dashboard and cannot have their &#x60;widgetType&#x60; or &#x60;options&#x60; modified, as  they are tracked with the parent dashboard widget. | [optional] 
**source_id** | **string** | If a widget was cloned from another widget, the ID of the source widget will be stored here. | [optional] 
**name** | **string** | The name of the widget. | [optional] 
**description** | **string** | A short description of the widget. | [optional] 
**widget_type** | **string** | The type of widget | [optional] 
**options** | [**\Swagger\Client\Model\WidgetOptions**](WidgetOptions.md) | A number of custom field values for this widget. | [optional] 
**hidden** | **bool** | Should the widget be displayed on the dashboard or not. | [optional] 
**placement** | [**\Swagger\Client\Model\DashboardWidgetPlacement**](DashboardWidgetPlacement.md) | Information about the placement of the widget | [optional] 
**data_source** | [**\Swagger\Client\Model\DashboardWidgetDataSource**](DashboardWidgetDataSource.md) | Data source information | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


