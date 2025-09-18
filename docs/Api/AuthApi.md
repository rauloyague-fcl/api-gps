# Swagger\Client\AuthApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**changePassword**](AuthApi.md#changePassword) | **PUT** /auth/user/password | 
[**enrolOTP**](AuthApi.md#enrolOTP) | **POST** /auth/otp/{method}/enrol | 
[**getCurrentUserAvatar**](AuthApi.md#getCurrentUserAvatar) | **GET** /auth/user/avatar | 
[**getUserProfile**](AuthApi.md#getUserProfile) | **GET** /auth/user/profile | 
[**refreshTokens**](AuthApi.md#refreshTokens) | **POST** /auth/refresh | 
[**resetPassword**](AuthApi.md#resetPassword) | **POST** /auth/password/reset | 
[**selectUser**](AuthApi.md#selectUser) | **GET** /auth/select/user/{id} | 
[**sendOTP**](AuthApi.md#sendOTP) | **POST** /auth/otp/{method}/send | 
[**setPassword**](AuthApi.md#setPassword) | **POST** /auth/password/set | 
[**signIn**](AuthApi.md#signIn) | **POST** /auth/signin | 
[**signOut**](AuthApi.md#signOut) | **POST** /auth/signout | 
[**validateOTP**](AuthApi.md#validateOTP) | **POST** /auth/otp/{method}/validate | 
[**verifyOTP**](AuthApi.md#verifyOTP) | **POST** /auth/otp/{method}/verify | 


# **changePassword**
> \Swagger\Client\Model\SuccessResponse changePassword($request)



Changes the currently authenticated user's password.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\UpdateUserPasswordRequest(); // \Swagger\Client\Model\UpdateUserPasswordRequest | 

try {
    $result = $apiInstance->changePassword($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->changePassword: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\UpdateUserPasswordRequest**](../Model/UpdateUserPasswordRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SuccessResponse**](../Model/SuccessResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **enrolOTP**
> \Swagger\Client\Model\AuthOTPGenerateResponse enrolOTP($method)



Generate a new TOTP secret for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$method = "method_example"; // string | 

try {
    $result = $apiInstance->enrolOTP($method);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->enrolOTP: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **method** | **string**|  |

### Return type

[**\Swagger\Client\Model\AuthOTPGenerateResponse**](../Model/AuthOTPGenerateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCurrentUserAvatar**
> string getCurrentUserAvatar()



Return the current user's avatar in binary format

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getCurrentUserAvatar();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->getCurrentUserAvatar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserProfile**
> \Swagger\Client\Model\UserProfileResponse getUserProfile()



Retrieves the currently authenticated user's profile

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getUserProfile();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->getUserProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\UserProfileResponse**](../Model/UserProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **refreshTokens**
> \Swagger\Client\Model\TokenResponse refreshTokens($request)



Refreshes a user's tokens by providing a valid refresh token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\AuthRefreshTokenRequest(); // \Swagger\Client\Model\AuthRefreshTokenRequest | 

try {
    $result = $apiInstance->refreshTokens($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->refreshTokens: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\AuthRefreshTokenRequest**](../Model/AuthRefreshTokenRequest.md)|  |

### Return type

[**\Swagger\Client\Model\TokenResponse**](../Model/TokenResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **resetPassword**
> \Swagger\Client\Model\SuccessResponse resetPassword($request)



Sends a password reset email to the user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\AuthResetPasswordRequest(); // \Swagger\Client\Model\AuthResetPasswordRequest | 

try {
    $result = $apiInstance->resetPassword($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->resetPassword: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\AuthResetPasswordRequest**](../Model/AuthResetPasswordRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SuccessResponse**](../Model/SuccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **selectUser**
> \Swagger\Client\Model\SelectedUserTokenResponse selectUser($id)



Selects a user from a list that has already been authenticated.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The user id you are requesting an access token for (previously retrieved using the /auth/signin route).

try {
    $result = $apiInstance->selectUser($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->selectUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The user id you are requesting an access token for (previously retrieved using the /auth/signin route). |

### Return type

[**\Swagger\Client\Model\SelectedUserTokenResponse**](../Model/SelectedUserTokenResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendOTP**
> \Swagger\Client\Model\AuthOTPSendResponse sendOTP($method)



Generate a new TOTP secret for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$method = "method_example"; // string | 

try {
    $result = $apiInstance->sendOTP($method);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->sendOTP: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **method** | **string**|  |

### Return type

[**\Swagger\Client\Model\AuthOTPSendResponse**](../Model/AuthOTPSendResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setPassword**
> \Swagger\Client\Model\SuccessResponse setPassword($request)



Sends a password reset email to the user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\AuthSetPasswordRequest(); // \Swagger\Client\Model\AuthSetPasswordRequest | 

try {
    $result = $apiInstance->setPassword($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->setPassword: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\AuthSetPasswordRequest**](../Model/AuthSetPasswordRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SuccessResponse**](../Model/SuccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **signIn**
> \Swagger\Client\Model\UserSessionResponse signIn($request)



Authenticate using a username and password

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\AuthRequest(); // \Swagger\Client\Model\AuthRequest | 

try {
    $result = $apiInstance->signIn($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->signIn: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\AuthRequest**](../Model/AuthRequest.md)|  |

### Return type

[**\Swagger\Client\Model\UserSessionResponse**](../Model/UserSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **signOut**
> map[string,null] signOut($request)



Invalidate an active access token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\SignOutRequest(); // \Swagger\Client\Model\SignOutRequest | 

try {
    $result = $apiInstance->signOut($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->signOut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\SignOutRequest**](../Model/SignOutRequest.md)|  |

### Return type

**map[string,null]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **validateOTP**
> \Swagger\Client\Model\AuthOTPValidateResponse validateOTP($method, $request)



Validate a user TOTP token against the user secret

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$method = "method_example"; // string | 
$request = new \Swagger\Client\Model\AuthOTPValidateRequest(); // \Swagger\Client\Model\AuthOTPValidateRequest | 

try {
    $result = $apiInstance->validateOTP($method, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->validateOTP: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **method** | **string**|  |
 **request** | [**\Swagger\Client\Model\AuthOTPValidateRequest**](../Model/AuthOTPValidateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AuthOTPValidateResponse**](../Model/AuthOTPValidateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **verifyOTP**
> \Swagger\Client\Model\AuthOTPValidateResponse verifyOTP($method, $request)



Verify a new TOTP token against the freshly generated user secret. Once successful, this route cannot be called again until TOTP is reset for the user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$method = "method_example"; // string | 
$request = new \Swagger\Client\Model\AuthOTPValidateRequest(); // \Swagger\Client\Model\AuthOTPValidateRequest | 

try {
    $result = $apiInstance->verifyOTP($method, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->verifyOTP: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **method** | **string**|  |
 **request** | [**\Swagger\Client\Model\AuthOTPValidateRequest**](../Model/AuthOTPValidateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AuthOTPValidateResponse**](../Model/AuthOTPValidateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

