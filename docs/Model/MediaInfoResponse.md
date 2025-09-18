# MediaInfoResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The internal ID of the media item | 
**owner** | [**\Swagger\Client\Model\IdName**](IdName.md) | The company that owns this media item | 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset that generated this media item | 
**requester** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The entity that requested this media item | 
**mime_type** | **string** | The MIME type of this media | 
**filename** | **string** | The filename of the media item | 
**input** | **string** | The camera input from which this media was recorded | 
**date** | **string** | The ISO date at which this media was started | 
**duration** | **double** | The duration of the media item | 
**status** | **string** | The status of the media item | 
**event_id** | **string** | The UUID of an event that is linked to this media item | 
**event_class** | **string** | The class of the event that is linked to this media item | 
**event_type** | **string** | The type of the event that is linked to this media item | 
**lat** | **double** | The latitude where this event was triggered | 
**lon** | **double** | The longitude where this event was triggered | 
**address** | **string** | The geocoded address of where this event was triggered | 
**fields** | [**map[string,null]**](.md) | a list of custom field values attached to this event | 
**labels** | [**\Swagger\Client\Model\LabelValuePayload[]**](LabelValuePayload.md) | Any labels applied to this media item | 
**provider** | **string** | The name of the device provider that handled this media item | 
**progress** | **double** | The progress of media retrieval (not all devices support this property) | 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | Information about when this media item was created and last updated | 
**data** | [**map[string,null]**](.md) | Device specific information about this media item | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


