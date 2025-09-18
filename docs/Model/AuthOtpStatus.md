# AuthOtpStatus

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**methods** | [**\Swagger\Client\Model\UserOTPMethod[]**](UserOTPMethod.md) | The type of OTP that is required for this user. | 
**required_from** | **string** | Date by which the user is required to use OTP authentication. | 
**authenticated** | **bool** | If true, the cached OTP token for the user has been accepted, and OTP can be skipped. | 
**token_validity_days** | **double** | The number of days for which any OTP tokens returned by the API will be valid for | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


