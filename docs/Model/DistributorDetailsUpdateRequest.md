# DistributorDetailsUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
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

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


