# HealthIssueResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | A unique GUID for the issue | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company that owns this issue | 
**target** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The target entity to which the issue relates | 
**topic** | **string** | A name given to the issue | 
**source** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The source entity from which the issue originates | 
**date** | [**\Swagger\Client\Model\HealthIssueDates**](HealthIssueDates.md) | Date information | 
**count** | **double** | A number of times the issue has been experienced since it was first experienced | 
**resolved** | [**\Swagger\Client\Model\HealthIssueResolutionDetail**](HealthIssueResolutionDetail.md) | The flag indicating the issue has been corrected or not | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


