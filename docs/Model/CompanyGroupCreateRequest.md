# CompanyGroupCreateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | A unique name for this entity | 
**parent** | [**\Swagger\Client\Model\IdName**](IdName.md) | The parent of this entity | [optional] 
**flags** | [**\Swagger\Client\Model\FlagsBucket**](FlagsBucket.md) | A set of user defined flags | [optional] 
**email** | [**\Swagger\Client\Model\EmailConfig**](EmailConfig.md) | Email configuration | [optional] 
**limits** | [**\Swagger\Client\Model\SoftLimits**](SoftLimits.md) | Soft limits that apply to companies in this group. | [optional] 
**retention** | [**\Swagger\Client\Model\CompanyDataRetentionSettings**](CompanyDataRetentionSettings.md) | Data retention settings. If this is null, settings from the parent company will be used instead. | [optional] 
**password_policy** | [**\Swagger\Client\Model\UserPasswordPolicy**](UserPasswordPolicy.md) | Password policy to apply to users of companies that belong to this group. | [optional] 
**owner_id** | **string** | The client that owns this entity | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


