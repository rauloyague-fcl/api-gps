# OTPSettings

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**methods** | [**map[string,\Swagger\Client\Model\OTPMethodSettings]**](OTPMethodSettings.md) | The one time password methods that are allowed | 
**mandatory_for** | **string** | Define who is forced to enable OTP. If set to \&quot;optional\&quot;, users can opt themselves into OTP but do not need to do so. | 
**grace_period_days** | **double** | The number of days grace that will be given to new users when their account is created before they are forced to enable OTP on their account. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


