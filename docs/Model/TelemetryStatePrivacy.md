# TelemetryStatePrivacy

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | **string** | The source of the current privacy mode (scheduled, assetstate or user) | 
**schedule_trigger** | [**\Swagger\Client\Model\PrivacyScheduleItem**](PrivacyScheduleItem.md) | The scheduled trigger (if source is scheduled) | [optional] 
**asset_state_trigger** | [**\Swagger\Client\Model\PrivacyStateItem**](PrivacyStateItem.md) | The asset state trigger responsible (if source is assetstate) | [optional] 
**user_trigger** | [**\Swagger\Client\Model\AssetPrivacyResponse**](AssetPrivacyResponse.md) | Information about the user initiated privacy mode (if source is user) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


