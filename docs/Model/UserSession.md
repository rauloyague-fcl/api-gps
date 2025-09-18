# UserSession

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique ID of this session | 
**user_id** | **string** | The user UUID | 
**start** | **string** | The ISO date when the session was started | 
**expiry** | **string** | The expiry date of the session (can be extended with token refreshes) | 
**ip** | **string** | The IP address of the user that initiated or last refreshed the session | 
**hostname** | **string** | The hostname of the front-end from which the session was created | 
**agent** | **string** | The browser user agent string of the user | 
**invalidated** | **bool** | A flag indicating if the session has been invalidated | [optional] 
**current** | **bool** | True if this session is the same session from which this request was made | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


