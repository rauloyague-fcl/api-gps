# Swagger\Client\ThemesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTheme**](ThemesApi.md#createTheme) | **POST** /entities/themes | 
[**deleteThemeLogo**](ThemesApi.md#deleteThemeLogo) | **DELETE** /entities/themes/{id}/logo | 
[**getTheme**](ThemesApi.md#getTheme) | **GET** /entities/themes/{id} | 
[**getThemeForDomain**](ThemesApi.md#getThemeForDomain) | **GET** /entities/themes/domain/{domain} | 
[**getThemeLogo**](ThemesApi.md#getThemeLogo) | **GET** /entities/themes/{id}/logo | 
[**listThemes**](ThemesApi.md#listThemes) | **GET** /entities/themes | 
[**updateTheme**](ThemesApi.md#updateTheme) | **PUT** /entities/themes/{id} | 
[**updateThemeLogo**](ThemesApi.md#updateThemeLogo) | **POST** /entities/themes/{id}/logo | 


# **createTheme**
> \Swagger\Client\Model\ThemeResponse createTheme($request)



Creates a new Theme entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\ThemeCreateRequest(); // \Swagger\Client\Model\ThemeCreateRequest | 

try {
    $result = $apiInstance->createTheme($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->createTheme: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\ThemeCreateRequest**](../Model/ThemeCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\ThemeResponse**](../Model/ThemeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteThemeLogo**
> deleteThemeLogo($id, $size)



Permanently deletes a theme logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The theme UUID.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->deleteThemeLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->deleteThemeLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The theme UUID. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTheme**
> \Swagger\Client\Model\ThemeResponse getTheme($id)



Returns Theme details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the Theme

try {
    $result = $apiInstance->getTheme($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->getTheme: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the Theme |

### Return type

[**\Swagger\Client\Model\ThemeResponse**](../Model/ThemeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getThemeForDomain**
> \Swagger\Client\Model\DomainThemeResponse getThemeForDomain($domain)



Returns client details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$domain = "domain_example"; // string | The domain name to look up

try {
    $result = $apiInstance->getThemeForDomain($domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->getThemeForDomain: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **string**| The domain name to look up |

### Return type

[**\Swagger\Client\Model\DomainThemeResponse**](../Model/DomainThemeResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getThemeLogo**
> string getThemeLogo($id, $size, $recurse)



Return the specified vendor's logo in binary format. Should the vendor not have a custom logo, the logo of the distributor will be supplied.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The vendor UUID you are requesting data for.
$size = "size_example"; // string | The size of the returned image. Can be either \"small\" or \"large\".
$recurse = true; // bool | If the theme doesn't have a logo, should we go up the client tree and try find one?

try {
    $result = $apiInstance->getThemeLogo($id, $size, $recurse);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->getThemeLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The vendor UUID you are requesting data for. |
 **size** | **string**| The size of the returned image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. | [optional]
 **recurse** | **bool**| If the theme doesn&#39;t have a logo, should we go up the client tree and try find one? | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listThemes**
> \Swagger\Client\Model\ThemeListResponse listThemes($owner, $recurse, $offset, $limit, $sort, $filter)



Retrieve a list of themes for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id you are requesting data for
$recurse = true; // bool | 
$offset = 1.2; // double | 
$limit = 1.2; // double | 
$sort = "sort_example"; // string | 
$filter = "filter_example"; // string | 

try {
    $result = $apiInstance->listThemes($owner, $recurse, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->listThemes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id you are requesting data for |
 **recurse** | **bool**|  | [optional]
 **offset** | **double**|  | [optional]
 **limit** | **double**|  | [optional]
 **sort** | **string**|  | [optional]
 **filter** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\ThemeListResponse**](../Model/ThemeListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateTheme**
> \Swagger\Client\Model\ThemeResponse updateTheme($id, $request)



Updates an existing Theme entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the Theme
$request = new \Swagger\Client\Model\ThemeUpdateRequest(); // \Swagger\Client\Model\ThemeUpdateRequest | 

try {
    $result = $apiInstance->updateTheme($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->updateTheme: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the Theme |
 **request** | [**\Swagger\Client\Model\ThemeUpdateRequest**](../Model/ThemeUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\ThemeResponse**](../Model/ThemeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateThemeLogo**
> updateThemeLogo($id, $size)



Updates the theme logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ThemesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The theme UUID you are requesting data for.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->updateThemeLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling ThemesApi->updateThemeLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The theme UUID you are requesting data for. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

