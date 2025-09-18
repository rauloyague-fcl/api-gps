# ReminderListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | A unique name for this reminder | [optional] 
**target** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The target entity to which this reminder applies. Usually an asset. | [optional] 
**type** | **string** | Specify the trigger type of the reminder, which can be either time, odometer or engine hours. | [optional] 
**mode** | **string** | The reminder mode. If set to once, the reminder will be disabled as soon as it has triggered at least once. | [optional] 
**time_zone_id** | **string** | The timezone to use for time based triggers. | [optional] 
**trigger** | [**\Swagger\Client\Model\ReminderTriggerValue**](ReminderTriggerValue.md) | The value to trigger at. This could be a date/time or and odometer or engine hours value. | [optional] 
**reset** | [**\Swagger\Client\Model\ReminderReset**](ReminderReset.md) |  | [optional] 
**enabled** | **bool** | Whether the reminder is still enabled (will be false for reminders with mode set to &#x60;once&#x60; that have already triggered. | [optional] 
**modified_date** | **string** | The date the entity was last modified | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


