# AssetSharedLocationTokenResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | A name for the asset to be returned instead of the asset&#39;s default name. | [optional] 
**expiry** | **string** | an ISO date/time at which to stop sharing the asset&#39;s location | 
**destination** | [**\Swagger\Client\Model\DestinationAddress**](DestinationAddress.md) | An optional destination address | [optional] 
**owner** | [**\Swagger\Client\Model\IdName**](IdName.md) | The client that owns the asset | 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset to be shared | 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user that created this share | 
**date** | [**\Swagger\Client\Model\IdName**](IdName.md) | The date on which the token was created | 
**token** | **string** | A unique token that can be used to retreive the shared asset&#39;s location | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


