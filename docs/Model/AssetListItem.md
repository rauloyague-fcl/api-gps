# AssetListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique ID for this asset | 
**name** | **string** | A client unique name for this asset. This can be any value that is relevant for the client. | 
**owner** | [**\Swagger\Client\Model\IdName**](IdName.md) | The client that owns this asset | 
**shared_with** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | One or more clients to which this asset has been shared. | 
**asset_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of asset | 
**groups** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | One of more asset groups that this asset belongs to | 
**categories** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | Up to 5 different categories that this asset belongs to | 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre to which this asset belongs | 
**devices** | [**\Swagger\Client\Model\AssetDevice[]**](AssetDevice.md) | One or more devices that provide telemetry data for this asset. | 
**asset_tag** | **string** |  | 
**tags** | **string[]** |  | 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this asset. | 
**color** | **string** | The color of the icon for this asset | 
**state** | **string** | The current state of the asset object | 
**geo_lock** | [**\Swagger\Client\Model\AssetGeoLock**](AssetGeoLock.md) | Details about an active geo-lock on this asset (if any) | [optional] 
**cameras** | **double** | The number of cameras connected to this asset | 
**linked_to** | [**\Swagger\Client\Model\AssetLinkage[]**](AssetLinkage.md) | A list of clients into which this asset has been linked/cloned | 
**linked_from** | [**\Swagger\Client\Model\AssetLinkage[]**](AssetLinkage.md) | The source client that this asset has been linked/cloned from | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


