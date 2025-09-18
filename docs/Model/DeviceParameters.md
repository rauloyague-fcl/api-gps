# DeviceParameters

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active_input** | **string** | The input that is used to determine when the device becomes active (ignition on for vehicles). Determines when trips are started and ended. | [optional] 
**hours_input** | **string** | The input that is used to start counting engine hours. This is usually the same as &#39;active_input&#39;. | [optional] 
**idling_input** | **string** | The input that is used to determine when the device is idling. Defaults to \&quot;speed\&quot; where idling is calulated based on device speed. | [optional] 
**idling_input_invert** | **bool** | Set to true to invert the input value that is being used for the idling input | [optional] 
**io** | [**\Swagger\Client\Model\DeviceIOParameters**](DeviceIOParameters.md) | Mappings between IoTypes and the device&#39;s telemetry inputs and outputs | [optional] 
**io_whitelist** | **string[]** | If this array is populated, only the IOs listed in this array will be persisted in the system, and everything else will be discarded | [optional] 
**bitmaps** | [**\Swagger\Client\Model\DeviceBitmapConfiguration[]**](DeviceBitmapConfiguration.md) | A list of inputs derived using a bitmap operation | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


