# EventResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique ID for the event | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The owner company of the event | 
**origin** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The originator of the event | [optional] 
**linked** | [**\Swagger\Client\Model\IdNameType[]**](IdNameType.md) | Assets and devices that are linked to this event | 
**alerts** | [**\Swagger\Client\Model\IdNameType[]**](IdNameType.md) | Any alerts this event may have triggered | 
**labels** | [**\Swagger\Client\Model\LabelValuePayload[]**](LabelValuePayload.md) | Any labels applied to this event | 
**notify** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | Users that were notified of this event | 
**media** | [**\Swagger\Client\Model\EventMedia[]**](EventMedia.md) | Media that&#39;s linked to this event | 
**event_date** | **string** | The UTC date of the event as recorded by the device that triggered it | 
**creation_date** | **string** | The UTC date when the evetn was created in the system | 
**modified_date** | **string** | The UTC date when this event was last modified | 
**event_class** | **string** | The class of the event | 
**event_type** | **string** | The type of event in the given class | 
**handled_by** | [**\Swagger\Client\Model\EventHandled**](EventHandled.md) | Populated if the event/alert has been handled by a user | [optional] 
**comments** | [**\Swagger\Client\Model\EventComment[]**](EventComment.md) | List of comments that users have left on this event | 
**details** | [**\Swagger\Client\Model\Dictionary**](Dictionary.md) | An event class specific bag of details relating to this event | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


