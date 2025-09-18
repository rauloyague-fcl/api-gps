# ExportTaskUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client** | [**\Swagger\Client\Model\IdName**](IdName.md) | The client to export data from. In the case of a Firehose export task, this will be the Vendor and not a client. | [optional] 
**name** | **string** | The name of the export task | [optional] 
**state** | **string** | The state of the export task | [optional] 
**delivery_method** | **string** | The delivery method of the export tasks | [optional] 
**assets** | [**\Swagger\Client\Model\EventActorFilter[]**](EventActorFilter.md) | The filters used to get the assets to be included in the export task | [optional] 
**document_types** | **string[]** | The document types to include in the export task | [optional] 
**document_version** | **string** | The document layout version | [optional] 
**settings** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | A set of delivery method specific options | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


