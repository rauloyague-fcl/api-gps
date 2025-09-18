# Swagger\Client\AssetRatingProfilesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAssetRatingProfile**](AssetRatingProfilesApi.md#createAssetRatingProfile) | **POST** /entities/assetratingprofiles | 
[**getAssetRatingProfile**](AssetRatingProfilesApi.md#getAssetRatingProfile) | **GET** /entities/assetratingprofiles/{id} | 
[**listAssetRatingProfiles**](AssetRatingProfilesApi.md#listAssetRatingProfiles) | **GET** /entities/assetratingprofiles | 
[**updateAssetRatingProfile**](AssetRatingProfilesApi.md#updateAssetRatingProfile) | **PUT** /entities/assetratingprofiles/{id} | 


# **createAssetRatingProfile**
> \Swagger\Client\Model\AssetRatingProfileResponse createAssetRatingProfile($request)



Creates a new Asset Rating Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetRatingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\AssetRatingProfileCreateRequest(); // \Swagger\Client\Model\AssetRatingProfileCreateRequest | 

try {
    $result = $apiInstance->createAssetRatingProfile($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetRatingProfilesApi->createAssetRatingProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\AssetRatingProfileCreateRequest**](../Model/AssetRatingProfileCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetRatingProfileResponse**](../Model/AssetRatingProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAssetRatingProfile**
> \Swagger\Client\Model\AssetRatingProfileResponse getAssetRatingProfile($id)



Returns asset rating profile details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetRatingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset rating profile

try {
    $result = $apiInstance->getAssetRatingProfile($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetRatingProfilesApi->getAssetRatingProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset rating profile |

### Return type

[**\Swagger\Client\Model\AssetRatingProfileResponse**](../Model/AssetRatingProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listAssetRatingProfiles**
> \Swagger\Client\Model\AssetRatingProfileListResponse listAssetRatingProfiles($owner, $offset, $limit, $sort, $filter)



Retrieve a list of asset rating profiles for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetRatingProfilesApi(
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
    $result = $apiInstance->listAssetRatingProfiles($owner, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetRatingProfilesApi->listAssetRatingProfiles: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\AssetRatingProfileListResponse**](../Model/AssetRatingProfileListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateAssetRatingProfile**
> \Swagger\Client\Model\AssetRatingProfileResponse updateAssetRatingProfile($id, $request)



Updates an existing Asset Rating Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetRatingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the Asset State Profile
$request = new \Swagger\Client\Model\AssetRatingProfileUpdateRequest(); // \Swagger\Client\Model\AssetRatingProfileUpdateRequest | 

try {
    $result = $apiInstance->updateAssetRatingProfile($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetRatingProfilesApi->updateAssetRatingProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the Asset State Profile |
 **request** | [**\Swagger\Client\Model\AssetRatingProfileUpdateRequest**](../Model/AssetRatingProfileUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetRatingProfileResponse**](../Model/AssetRatingProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

