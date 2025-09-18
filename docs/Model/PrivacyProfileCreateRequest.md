# PrivacyProfileCreateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | A unique name for this entity | [optional] 
**state** | **string** | The current state of this entity | [optional] 
**schedule_triggers** | [**\Swagger\Client\Model\PrivacyScheduleItem[]**](PrivacyScheduleItem.md) | The scheduled trigger times for this profile | [optional] 
**state_triggers** | [**\Swagger\Client\Model\PrivacyStateItem[]**](PrivacyStateItem.md) | The state profiles to trigger on | [optional] 
**enable_manual_trigger** | **bool** | Set to true to allow manual privacy mode triggers via the API | [optional] 
**owner_id** | **string** | The company that owns this privacy profile | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


