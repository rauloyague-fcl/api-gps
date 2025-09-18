# Schedule

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schedule_type** | **string** | The type of schedule | [optional] 
**start_time** | **string** | The time of schedule initation. Also sets the time at which reports run. | [optional] 
**every** | **double** | For daily and hourly scheduled, every {{every}} x hours/days | [optional] 
**days** | **double[]** | For weekly schedules, the days of the week in which to run (0-6 where 0 &#x3D; sunday). For monthly schedule, a single value with the day of the month to run on. | [optional] 
**months** | **double[]** | For monthly schedules, the month number (1-12) in which to run. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


