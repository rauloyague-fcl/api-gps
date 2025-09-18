# CompletedReportResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique ID of this report definition | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The entity that owns this report | 
**user** | [**\Swagger\Client\Model\IdName**](IdName.md) | The user that queued this report definition | 
**client** | [**\Swagger\Client\Model\IdName**](IdName.md) | The client for which the report was run | 
**name** | **string** | The base report name | 
**title** | **string** | The report title as set by the user | 
**source** | **string** | The reporting subsystem that generates this report | 
**status** | **string** | The status of this report | 
**queue_date** | **string** | The ISO date/time that this report was queued | 
**update_date** | **string** | The ISO date/time that this report&#39;s state last changed | 
**output_format** | **string** | The output format for this report | 
**progress** | **double** | The progress percentage of this report | 
**order** | **double** | report queue order, will change sometimes while queued | 
**priority** | **double** | The report priority: 0 &#x3D; urgent, 1 &#x3D; high, 2 &#x3D; normal, 3 &#x3D; low, 4+ &#x3D; none (sorted as an integer) | 
**config** | [**\Swagger\Client\Model\ReportConfig**](ReportConfig.md) | The report configuration | 
**triggered_by** | **string** | What triggered the report | 
**base_report_id** | **string** | The UUID of a base report in analytics (if any) this report is linked to | [optional] 
**output_options** | [**\Swagger\Client\Model\ReportOutputOptions**](ReportOutputOptions.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


