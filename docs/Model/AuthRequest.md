# AuthRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Optionally pass the domain for which this login is restricted to. Required for OpenId Connect &#x60;id_token&#x60; based authentication. | [optional] 
**username** | **string** | The username to authenticate against, usually an email address. Required for password validation. | [optional] 
**password** | **string** | The password for the specified username. Required if you passed a username. | [optional] 
**user_id** | **string** | Optional - if multiple matching users are expected, you can pre-select the user you want by passing in the user id | [optional] 
**token** | **string** | Optional token based authentication. This could be a password reset token or an OpenId Connect &#x60;id_token&#x60;. Username and password are ignored if a token is passed. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


