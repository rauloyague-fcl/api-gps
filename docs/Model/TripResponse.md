# TripResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique id for this trip | 
**asset** | [**\Swagger\Client\Model\IdName**](IdName.md) | The asset that generated this trip | 
**asset_type** | [**\Swagger\Client\Model\IdName**](IdName.md) | The type of this asset | 
**trip_type** | **string** | The type of this trip | 
**date_start** | **string** | The ISO8601 UTC date that the trip was started | 
**date_end** | **string** | The ISO8601 UTC date that the trip was ended | 
**start** | [**\Swagger\Client\Model\TripLocation**](TripLocation.md) | The location where the trip started | [optional] 
**end** | [**\Swagger\Client\Model\TripLocation**](TripLocation.md) | The location where the trip ended | [optional] 
**stats** | [**\Swagger\Client\Model\TripStats**](TripStats.md) | Statistics about the trip | [optional] 
**rating** | [**\Swagger\Client\Model\TripRating**](TripRating.md) | Trip rating information | [optional] 
**records** | **double** | The number of telemetry records that comprised this trip | [optional] 
**linked_assets** | [**\Swagger\Client\Model\IdNameType[]**](IdNameType.md) | Any other assets that were linked to this trip | 
**maxes** | [**\Swagger\Client\Model\NumberDictionary**](NumberDictionary.md) | Max values for the trip | [optional] 
**labels** | [**\Swagger\Client\Model\LabelValuePayload[]**](LabelValuePayload.md) | An optional list of labels assigned to this trip | [optional] 
**private** | **bool** | Indication of whether this trip is private or not | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


