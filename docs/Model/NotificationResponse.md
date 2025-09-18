# NotificationResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique ID for the notification event | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The owner company of the notification event | 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user that triggered the notification event | 
**date** | **string** | The UTC date when the notification event was recorded in the system | 
**sequence** | **double** | A sequence number that can be used to traverse the notification feed | 
**event_type** | **string** | The type of event in the given class | 
**text** | **string** | The text description of the event | 
**data** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | Event specific information | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


