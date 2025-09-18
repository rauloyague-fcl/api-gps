# ZoneUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | A unique name for this zone | [optional] 
**group** | [**\Swagger\Client\Model\IdName**](IdName.md) | The zone group to which this zone belongs | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre to which this zone belongs | [optional] 
**state** | **string** | The state of this zone | [optional] 
**zone_type** | **string** | The type of zone | [optional] 
**speed** | **double** | A speed limit (in km/h) to apply to this zone. Any asset that enters this zone will have the road speed limit overriden by the zone speed limit. | [optional] 
**radius** | **double** | For zone proximity alerts, specifiy a distance in km from the center of the zone. | [optional] 
**points** | [**\Swagger\Client\Model\ZonePoint[]**](ZonePoint.md) | The points for the zone polygon/polyline. Only populated on &#x60;get*&#x60; routes. | [optional] 
**tag** | **string** | The tag entity | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


