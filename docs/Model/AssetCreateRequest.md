# AssetCreateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | A client unique name for this asset. This can be any value that is relevant for the client. | 
**asset_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of asset | 
**color** | **string** | The color of the icon for this asset | [optional] 
**tags** | **string[]** |  | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre to which this asset belongs | 
**rating_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The trip rating profile to use for this assets trip rating | [optional] 
**asset_state_profiles** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | One or more asset state profiles to use for this asset | [optional] 
**overspeed_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The overspeed profile to use for this asset | [optional] 
**geo_lock_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The geo lock profile to use for this asset | [optional] 
**road_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The road profile to use for this asset | [optional] 
**privacy_profile** | [**\Swagger\Client\Model\IdName**](IdName.md) | The privacy profile to use for this asset | [optional] 
**groups** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | One of more asset groups that this asset belongs to | 
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
**owner_id** | **string** |  | 
**counter_values** | [**\Swagger\Client\Model\AssetCounterValues**](AssetCounterValues.md) | Populate this field to supply new odometer and/or engine hours values for the asset. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


