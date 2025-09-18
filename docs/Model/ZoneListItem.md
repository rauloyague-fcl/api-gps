# ZoneListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A unique name for this zone | [optional] 
**group** | [**\Swagger\Client\Model\IdName**](IdName.md) | The zone group to which this zone belongs | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre to which this zone belongs | [optional] 
**state** | **string** | The state of this zone | [optional] 
**zone_type** | **string** | The type of zone | [optional] 
**speed** | **double** | A speed limit (in km/h) to apply to this zone. Any asset that enters this zone will have the road speed limit overriden by the zone speed limit. | [optional] 
**radius** | **double** | For zone proximity alerts, specifiy a distance in km from the center of the zone. | [optional] 
**points** | [**\Swagger\Client\Model\ZonePoint[]**](ZonePoint.md) | The points for the zone polygon/polyline. Only populated on &#x60;get*&#x60; routes. | [optional] 
**tag** | **string** | The tag entity | [optional] 
**center** | [**\Swagger\Client\Model\ZoneCenter**](ZoneCenter.md) | The center of the zone (this is automatically calculated from the zone polygon. | [optional] 
**bounds** | [**\Swagger\Client\Model\ZoneBounds**](ZoneBounds.md) | The rectangular bounds that contains the zone polygon. | [optional] 
**modified_date** | **string** | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


