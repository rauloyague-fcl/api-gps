# SelectedUserTokenResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id_token** | **string** | The JWT token is represented as a JSON Web Token (JWT). The token contains claims about the identity of the authenticated user. Additional information is also included in this token such as the default client id and user&#39;s full name and surname. The id token expires one hour after the user authenticates. You should not process the access token in your client or web API after it has expired. | 
**access_token** | **string** | The JWT token is represented as a JSON Web Token (JWT). The token contains claims about the identity of the authenticated user. The access token expires one hour after the user authenticates. You should not process the access token in your client or web API after it has expired. | 
**refresh_token** | **string** | The JWT token is represented as a JSON Web Token (JWT). The token can be used to refresh a user&#39;s access and id tokens. The access token expires one hour after the user authenticates and the refresh token is valid for 30 days. You should not process the access token in your client or web API after it has expired. | 
**user** | [**\Swagger\Client\Model\AuthUserResponse**](AuthUserResponse.md) | The user that was selected | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


