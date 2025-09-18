# ScheduledReportResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user who&#39;s security credentials to use when running this schedule. | [optional] 
**name** | **string** | A unique name for this entity | [optional] 
**state** | **string** | The current state of this entity | [optional] 
**schedule_type** | **string** | The type of scheduled report. | [optional] 
**schedule** | [**\Swagger\Client\Model\Schedule**](Schedule.md) | The time schedule on which to run | [optional] 
**reports** | [**\Swagger\Client\Model\ScheduledReportReports**](ScheduledReportReports.md) | The reports that should be run when the schedule fires. | [optional] 
**recipients** | [**\Swagger\Client\Model\IdNameType[]**](IdNameType.md) | The recipients that will receive an email with the completed reports | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


