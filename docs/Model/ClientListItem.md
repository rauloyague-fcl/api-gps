# ClientListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The client&#39;s unique UUID | 
**name** | **string** | The client&#39;s display name | 
**website** | **string** | The client website (if available) | 
**owner** | [**\Swagger\Client\Model\IdName**](IdName.md) | The vendor that owns this client. | 
**group** | **string** | The group to which this client belongs. | 
**state** | **string** | The state of this client. | 
**counts** | [**\Swagger\Client\Model\NumberDictionary**](NumberDictionary.md) | A dictionary of child entity names and their counts, present if the &#x60;counts&#x60; parameter is supplied. | [optional] 
**creation_date** | **string** | The date this client was created. | 
**modified_date** | **string** | The date that this client was last modified. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


