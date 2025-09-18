# UserListItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** |  | [optional] 
**email_address** | **string** | The user&#39;s email address, used to log into the system | [optional] 
**mobile** | **string** | An optional mobile number used for SMS notifications | [optional] 
**time_zone_id** | **string** | The time zone identifier for the user (uses the tz datbase for timezones, see https://en.wikipedia.org/wiki/Tz_database) | [optional] 
**language** | **string** | The language code for this user | [optional] 
**state** | **string** | The state of the user object | [optional] 
**default_client** | [**\Swagger\Client\Model\IdName**](IdName.md) | The default client to load for this user | [optional] 
**cost_centre** | [**\Swagger\Client\Model\IdName**](IdName.md) | The cost centre that this user belongs to | [optional] 
**modified_date** | **string** | The date the user was last modified | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


