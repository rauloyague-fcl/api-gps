# UserRoleResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique UUID of this entity | 
**owner** | [**\Swagger\Client\Model\IdNameType**](IdNameType.md) | The company entity that owns this entity | 
**name** | **string** | The name of the user role | [optional] 
**description** | **string** | An optional description for the role | [optional] 
**legacy_rights** | [**\Swagger\Client\Model\LegacyRights**](LegacyRights.md) | The api rights of the policy. Legacy only | [optional] 
**inline_policies** | [**\Swagger\Client\Model\Policy[]**](Policy.md) | This applies to v2 API only | [optional] 
**entity** | [**\Swagger\Client\Model\EntityInfo**](EntityInfo.md) | entity specific metadata | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


