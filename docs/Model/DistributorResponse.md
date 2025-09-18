# DistributorResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | The display name of the company | [optional] 
**tags** | **string[]** | A list of custom ID&#39;s for this company. Can be queried using the getClientByTag, getVendorByTag and getDistributorByTag methods. | [optional] 
**website** | **string** | The company website (if available) | [optional] 
**state** | **string** | The state of this company | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 
**limits** | [**\Swagger\Client\Model\SoftLimits**](SoftLimits.md) | Soft limits that apply to this company. This includes overrides only, see &#x60;getLookups&#x60; for defaults. | [optional] 
**flags** | [**\Swagger\Client\Model\FlagsBucket**](FlagsBucket.md) | A set of user defined flags | [optional] 
**retention** | [**\Swagger\Client\Model\CompanyDataRetentionSettings**](CompanyDataRetentionSettings.md) | Data retention settings. If this is null, settings from the parent or group will be used instead. | [optional] 
**password_policy** | [**\Swagger\Client\Model\UserPasswordPolicy**](UserPasswordPolicy.md) | Password policy to apply to users. If this is null, settings from the group will be used instead. | [optional] 
**theme** | [**\Swagger\Client\Model\ThemeInfo**](ThemeInfo.md) | The theme that this company uses | [optional] 
**address** | [**\Swagger\Client\Model\CompanyAddress**](CompanyAddress.md) | Address information for this company | [optional] 
**time_zone_id** | **string** | The default timezone for this company | [optional] 
**custom_fields** | [**\Swagger\Client\Model\CustomFields**](CustomFields.md) | A set of custom fields for this company | [optional] 
**domains** | **string[]** | A list of custom domains to use for this company | [optional] 
**language** | **string** | The default language to user for this client. | [optional] 
**support** | [**\Swagger\Client\Model\CompanySupportDetails**](CompanySupportDetails.md) | Support contact information that will be displayed to user of this company | [optional] 
**messages** | [**\Swagger\Client\Model\CompanyMessages**](CompanyMessages.md) | Customized messages that are displayed to users of this company. | [optional] 
**oidc** | [**\Swagger\Client\Model\OpenIdConnectIssuers**](OpenIdConnectIssuers.md) | A set of OpenId Connect issuers that are able to authenticate users on our behalf. | [optional] 
**email_provider** | [**\Swagger\Client\Model\IdNameState**](IdNameState.md) | The email provider to be used when sending emails | [optional] 
**ssl_certificates** | [**\Swagger\Client\Model\CompanySSLCertificate[]**](CompanySSLCertificate.md) | A list of ssl certificates provisioned for this company | [optional] 
**vendor_groups** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | [DEPRECATED] Use the listCompanyGroups operation instead | [optional] 
**features** | [**\Swagger\Client\Model\Features**](Features.md) | A set of features that are enabled for this distributor. | [optional] 
**available_map_sets** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | A list of maps sets that are available to this distributor | [optional] 
**available_email_providers** | [**\Swagger\Client\Model\IdNameState[]**](IdNameState.md) | A list of email providers that are available to this distributor | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


