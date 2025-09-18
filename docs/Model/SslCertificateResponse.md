# SslCertificateResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**company** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company for which the ssl certificate was created | [optional] 
**domain** | **string** | The domain of the ssl certificate | [optional] 
**theme** | [**\Swagger\Client\Model\IdName**](IdName.md) | An optional theme for user of this domain | [optional] 
**notes** | **string** | A field for capturing notes about the ssl certificate | [optional] 
**state** | **string** | The state of the ssl certificate | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


