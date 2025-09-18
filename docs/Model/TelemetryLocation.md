# TelemetryLocation

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**lon** | **double** | The WGS84 longitude in decimal degrees | 
**lat** | **double** | The WGS84 latitude in decimal degrees | 
**speed** | **double** | The speed in km/h | 
**altitude** | **double** | The altitude above sea level in meters | 
**heading** | **double** | The heading in degrees | 
**accuracy** | **double** | The accuracy of the location (usually the number of satellites visible, but varies by device) | 
**address** | **string** | The reverse geocoded address of this location. May also be the name of a zone that is currently been entered. | [optional] 
**age** | **double** | The age of the gps position. Not sent by all devices. | [optional] 
**gc** | [**\Swagger\Client\Model\ReverseGeocode**](ReverseGeocode.md) | Detailed reverse geoding information | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


