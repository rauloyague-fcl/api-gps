# AuditEventResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique ID for the event | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The owner company of the event | 
**entity** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The user that triggered the event | 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user that triggered the event | 
**date** | **string** | The UTC date when the event was recorded in the system | 
**event_class** | **string** | The class of the event | 
**event_type** | **string** | The type of event in the given class | 
**changes** | [**\Swagger\Client\Model\AuditEventChange[]**](AuditEventChange.md) | A list of changes that were applied | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


