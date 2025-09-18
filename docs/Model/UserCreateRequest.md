# UserCreateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [optional] 
**email_address** | **string** | The user&#39;s email address, used to log into the system | [optional] 
**mobile** | **string** | An optional mobile number used for SMS notifications | [optional] 
**time_zone_id** | **string** | The time zone identifier for the user (uses the tz database for timezones, see https://en.wikipedia.org/wiki/Tz_database) | [optional] 
**language** | **string** | The language code for this user | [optional] 
**state** | **string** | The state of the user object | [optional] 
**notify_settings** | [**\Swagger\Client\Model\NotificationSettings**](NotificationSettings.md) | notification settings | [optional] 
**default_client** | [**\Swagger\Client\Model\IdName**](IdName.md) | The default client to load for this user | [optional] 
**roles** | [**\Swagger\Client\Model\IdName[]**](IdName.md) | A list of user roles that apply to this user | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre that this user belongs to | [optional] 
**oidc_tags** | [**\Swagger\Client\Model\OidcTags**](OidcTags.md) | When OpenId Connect is enabled for a client, you need to tie the user to the issuer&#39;s internal user ID. Specificy them  in the oidcTags bucket | [optional] 
**permissions** | [**\Swagger\Client\Model\UserPermissions**](UserPermissions.md) |  | [optional] 
**owner_id** | **string** | The company that owns this user | 
**password** | **string** | The users password | [optional] 
**invite_url** | **string** | Populate only if you wish to send an invitation email on account creation.  The full URL where the user will be redirected for completing their profile. Include a {token} template variable so the API can insert the reset token, and optionally a {domain} template variable into which the configured domain for this user will be inserted. i.e. https://{domain}/reset?token&#x3D;{token} | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


