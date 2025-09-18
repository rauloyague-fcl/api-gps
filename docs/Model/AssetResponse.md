# AssetResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A client unique name for this asset. This can be any value that is relevant for the client. | [optional] 
**asset_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of asset | [optional] 
**color** | **string** | The color of the icon for this asset | [optional] 
**tags** | **string[]** |  | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre to which this asset belongs | [optional] 
**rating_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The trip rating profile to use for this assets trip rating | [optional] 
**asset_state_profiles** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | One or more asset state profiles to use for this asset | [optional] 
**overspeed_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The overspeed profile to use for this asset | [optional] 
**geo_lock_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The geo lock profile to use for this asset | [optional] 
**road_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The road profile to use for this asset | [optional] 
**privacy_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The privacy profile to use for this asset | [optional] 
**groups** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | One of more asset groups that this asset belongs to | [optional] 
**categories** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | Up to 5 different categories that this asset belongs to | [optional] 
**shared_with** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | One or more clients to which this asset has been shared. | [optional] 
**asset_tag** | [**\Swagger\Client\Model\IdName**](IdName.md) |  | [optional] 
**state** | **string** | The current state of the asset object | [optional] 
**fields** | [**\Swagger\Client\Model\CustomFieldValues**](CustomFieldValues.md) | A number of custom field values for this asset. | [optional] 
**parameters** | [**\Swagger\Client\Model\AssetParameters**](AssetParameters.md) |  | [optional] 
**geo_lock** | [**\Swagger\Client\Model\AssetGeoLock**](AssetGeoLock.md) | Details about an active geo-lock on this asset (if any) | [optional] 
**contacts** | [**\Swagger\Client\Model\Contact[]**](Contact.md) | One or more contacts that are relevant to this asset | [optional] 
**location** | [**\Swagger\Client\Model\AssetLocation**](AssetLocation.md) | For static assets this field can be set with the known location of the asset | [optional] 
**zones** | [**\Swagger\Client\Model\AssetZoneTarget[]**](AssetZoneTarget.md) | A list of zones and routes that are relevant to this asset | [optional] 
**default_trip_labels** | **string[]** | A list of labels that will be applied to trips from this asset by default. | [optional] 
**devices** | [**\Swagger\Client\Model\AssetDevice[]**](AssetDevice.md) | One or more devices that provide telemetry data for this asset.  Can only be modified using the &#x60;updateDevice&#x60; operation. | [optional] 
**linked_from** | [**\Swagger\Client\Model\AssetLinkage**](AssetLinkage.md) | Information about asset linkage, can only be modified with the &#x60;linkAssets&#x60; operation. | [optional] 
**linked_to** | [**\Swagger\Client\Model\AssetLinkage[]**](AssetLinkage.md) | A list of assets this asset it linked to, can only be modified with the &#x60;linkAssets&#x60; operation. | [optional] 
**privacy** | [**\Swagger\Client\Model\AssetPrivacyResponse**](AssetPrivacyResponse.md) | If this is set (and the conditions are valid), the asset will run in privacy mode. | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


