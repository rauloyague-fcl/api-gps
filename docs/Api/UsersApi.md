# Swagger\Client\UsersApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createApiKey**](UsersApi.md#createApiKey) | **POST** /accounts/users/{id}/apikeys | 
[**createUser**](UsersApi.md#createUser) | **POST** /accounts/users | 
[**deleteApiKey**](UsersApi.md#deleteApiKey) | **DELETE** /accounts/users/{id}/apikeys/{keyid} | 
[**deleteOTPMethod**](UsersApi.md#deleteOTPMethod) | **DELETE** /accounts/users/{id}/otp/{method} | 
[**deleteUserAvatar**](UsersApi.md#deleteUserAvatar) | **DELETE** /accounts/users/{id}/avatar | 
[**getUser**](UsersApi.md#getUser) | **GET** /accounts/users/{id} | 
[**getUserAvatar**](UsersApi.md#getUserAvatar) | **GET** /accounts/users/{id}/avatar | 
[**getUserPolicies**](UsersApi.md#getUserPolicies) | **GET** /accounts/users/{id}/policies | 
[**listUsers**](UsersApi.md#listUsers) | **GET** /accounts/users | 
[**resetUser**](UsersApi.md#resetUser) | **PUT** /accounts/users/{id}/reset | 
[**updateUser**](UsersApi.md#updateUser) | **PUT** /accounts/users/{id} | 
[**updateUserAvatar**](UsersApi.md#updateUserAvatar) | **POST** /accounts/users/{id}/avatar | 


# **createApiKey**
> \Swagger\Client\Model\UserApiKeyCreateResponse createApiKey($id, $request)



Creates a new API key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$request = new \Swagger\Client\Model\UserApiKeyCreateRequest(); // \Swagger\Client\Model\UserApiKeyCreateRequest | 

try {
    $result = $apiInstance->createApiKey($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->createApiKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **request** | [**\Swagger\Client\Model\UserApiKeyCreateRequest**](../Model/UserApiKeyCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\UserApiKeyCreateResponse**](../Model/UserApiKeyCreateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createUser**
> \Swagger\Client\Model\UserCreateResponse createUser($request)



Creates a new user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\UserCreateRequest(); // \Swagger\Client\Model\UserCreateRequest | 

try {
    $result = $apiInstance->createUser($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->createUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\UserCreateRequest**](../Model/UserCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\UserCreateResponse**](../Model/UserCreateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteApiKey**
> \Swagger\Client\Model\SuccessResponse deleteApiKey($id, $keyid)



Deletes an API key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$keyid = "keyid_example"; // string | 

try {
    $result = $apiInstance->deleteApiKey($id, $keyid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->deleteApiKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **keyid** | **string**|  |

### Return type

[**\Swagger\Client\Model\SuccessResponse**](../Model/SuccessResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteOTPMethod**
> \Swagger\Client\Model\SuccessResponse deleteOTPMethod($id, $method)



Deletes a previously configured OTP method for a user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$method = "method_example"; // string | 

try {
    $result = $apiInstance->deleteOTPMethod($id, $method);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->deleteOTPMethod: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **method** | **string**|  |

### Return type

[**\Swagger\Client\Model\SuccessResponse**](../Model/SuccessResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteUserAvatar**
> deleteUserAvatar($id)



Permanently deletes a user avatar.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The user UUID.

try {
    $apiInstance->deleteUserAvatar($id);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->deleteUserAvatar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The user UUID. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUser**
> \Swagger\Client\Model\UserResponse getUser($id)



Returns user details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the user

try {
    $result = $apiInstance->getUser($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the user |

### Return type

[**\Swagger\Client\Model\UserResponse**](../Model/UserResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserAvatar**
> string getUserAvatar($id)



Return the user avatar in binary format

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The UUID of the user

try {
    $result = $apiInstance->getUserAvatar($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getUserAvatar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the user |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserPolicies**
> \Swagger\Client\Model\UserPoliciesResponse getUserPolicies($id)



Returns active security policies for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getUserPolicies($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getUserPolicies: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\UserPoliciesResponse**](../Model/UserPoliciesResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listUsers**
> \Swagger\Client\Model\UserListResponse listUsers($owner, $offset, $limit, $sort, $filter)



Retrieve a list of users for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id you are requesting data for
$offset = 1.2; // double | An offset into the result set, useful for pagination
$limit = 1.2; // double | Limit the number of results to this value.
$sort = "sort_example"; // string | Sorting column or attribute name with an optional direction, e.g. `sort=name:desc`
$filter = "filter_example"; // string | A filter to apply to the data in RQL format.

try {
    $result = $apiInstance->listUsers($owner, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->listUsers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id you are requesting data for |
 **offset** | **double**| An offset into the result set, useful for pagination | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **sort** | **string**| Sorting column or attribute name with an optional direction, e.g. &#x60;sort&#x3D;name:desc&#x60; | [optional]
 **filter** | **string**| A filter to apply to the data in RQL format. | [optional]

### Return type

[**\Swagger\Client\Model\UserListResponse**](../Model/UserListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **resetUser**
> \Swagger\Client\Model\UserResetResponse resetUser($id, $request)



Optionally suspends the user and sends them a password reset email.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the user
$request = new \Swagger\Client\Model\UserResetRequest(); // \Swagger\Client\Model\UserResetRequest | 

try {
    $result = $apiInstance->resetUser($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->resetUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the user |
 **request** | [**\Swagger\Client\Model\UserResetRequest**](../Model/UserResetRequest.md)|  |

### Return type

[**\Swagger\Client\Model\UserResetResponse**](../Model/UserResetResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateUser**
> \Swagger\Client\Model\UserResponse updateUser($id, $request)



Updates an existing user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the user
$request = new \Swagger\Client\Model\UserUpdateRequest(); // \Swagger\Client\Model\UserUpdateRequest | 

try {
    $result = $apiInstance->updateUser($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->updateUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the user |
 **request** | [**\Swagger\Client\Model\UserUpdateRequest**](../Model/UserUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\UserResponse**](../Model/UserResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateUserAvatar**
> updateUserAvatar($id)



Updates the specified user's avatar.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The user UUID you are requesting data for.

try {
    $apiInstance->updateUserAvatar($id);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->updateUserAvatar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The user UUID you are requesting data for. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

