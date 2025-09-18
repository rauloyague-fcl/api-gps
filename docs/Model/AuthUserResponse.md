# AuthUserResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique user identifier | 
**username** | **string** | The user&#39;s username (usually his email address) | 
**name** | **string** | The user&#39;s full name | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The entity that owns this user | 
**default_client** | [**\Swagger\Client\Model\IdName**](IdName.md) | The client that has been configured as the default for this user | 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre to which this user belongs | 
**time_zone_id** | **string** | The user&#39;s timezone, either as a region/city value (i.e. America/New_York) or a specific timezone (i.e. GMT+2) | 
**language** | **string** | The user&#39;s chosen language | 
**otp** | [**\Swagger\Client\Model\AuthOtpStatus**](AuthOtpStatus.md) | Information about one time password requirements | 
**password_expires_on** | **string** | The ISO date on which the users current password expires | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


