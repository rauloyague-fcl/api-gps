# UserPasswordPolicy

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | [READ-ONLY] The entity from which the active password polict settings are being calculated | [optional] 
**password_length** | **double** | The minimum length allowed for passwords | 
**password_complexity** | [**\Swagger\Client\Model\PasswordComplexity**](PasswordComplexity.md) | Defines the password complexity rules | 
**password_expiration_days** | **double** | Determines when users are prompted to change their password. Set to zero to disable password expiration. | 
**otp_settings** | [**\Swagger\Client\Model\OTPSettings**](OTPSettings.md) | Settings for One Time Password authentication. Set to null to disable OTP requirements | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


