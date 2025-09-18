# Swagger\Client\AssetStateProfilesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAssetStateProfile**](AssetStateProfilesApi.md#createAssetStateProfile) | **POST** /entities/assetstateprofiles | 
[**getAssetStateProfile**](AssetStateProfilesApi.md#getAssetStateProfile) | **GET** /entities/assetstateprofiles/{id} | 
[**listAssetStateProfiles**](AssetStateProfilesApi.md#listAssetStateProfiles) | **GET** /entities/assetstateprofiles | 
[**updateAssetStateProfile**](AssetStateProfilesApi.md#updateAssetStateProfile) | **PUT** /entities/assetstateprofiles/{id} | 


# **createAssetStateProfile**
> \Swagger\Client\Model\AssetStateProfileResponse createAssetStateProfile($request)



Creates a new Asset State Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetStateProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\AssetStateProfileCreateRequest(); // \Swagger\Client\Model\AssetStateProfileCreateRequest | 

try {
    $result = $apiInstance->createAssetStateProfile($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetStateProfilesApi->createAssetStateProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\AssetStateProfileCreateRequest**](../Model/AssetStateProfileCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetStateProfileResponse**](../Model/AssetStateProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAssetStateProfile**
> \Swagger\Client\Model\AssetStateProfileResponse getAssetStateProfile($id)



Returns asset state profile details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetStateProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset state profile

try {
    $result = $apiInstance->getAssetStateProfile($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetStateProfilesApi->getAssetStateProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset state profile |

### Return type

[**\Swagger\Client\Model\AssetStateProfileResponse**](../Model/AssetStateProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listAssetStateProfiles**
> \Swagger\Client\Model\AssetStateProfileListResponse listAssetStateProfiles($owner, $offset, $limit, $sort, $filter)



Retrieve a list of asset state profiles for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetStateProfilesApi(
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
    $result = $apiInstance->listAssetStateProfiles($owner, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetStateProfilesApi->listAssetStateProfiles: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\AssetStateProfileListResponse**](../Model/AssetStateProfileListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateAssetStateProfile**
> \Swagger\Client\Model\AssetStateProfileResponse updateAssetStateProfile($id, $request)



Updates an existing Asset State Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetStateProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the Asset State Profile
$request = new \Swagger\Client\Model\AssetStateProfileUpdateRequest(); // \Swagger\Client\Model\AssetStateProfileUpdateRequest | 

try {
    $result = $apiInstance->updateAssetStateProfile($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetStateProfilesApi->updateAssetStateProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the Asset State Profile |
 **request** | [**\Swagger\Client\Model\AssetStateProfileUpdateRequest**](../Model/AssetStateProfileUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetStateProfileResponse**](../Model/AssetStateProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

