# Swagger\Client\GeoLockProfilesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createGeoLockProfile**](GeoLockProfilesApi.md#createGeoLockProfile) | **POST** /entities/geolockprofiles | 
[**getGeoLockProfile**](GeoLockProfilesApi.md#getGeoLockProfile) | **GET** /entities/geolockprofiles/{id} | 
[**listGeoLockProfiles**](GeoLockProfilesApi.md#listGeoLockProfiles) | **GET** /entities/geolockprofiles | 
[**updateGeoLockProfile**](GeoLockProfilesApi.md#updateGeoLockProfile) | **PUT** /entities/geolockprofiles/{id} | 


# **createGeoLockProfile**
> \Swagger\Client\Model\GeoLockProfileResponse createGeoLockProfile($request)



Creates a new GeoLock Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GeoLockProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\GeoLockProfileCreateRequest(); // \Swagger\Client\Model\GeoLockProfileCreateRequest | 

try {
    $result = $apiInstance->createGeoLockProfile($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeoLockProfilesApi->createGeoLockProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\GeoLockProfileCreateRequest**](../Model/GeoLockProfileCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\GeoLockProfileResponse**](../Model/GeoLockProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getGeoLockProfile**
> \Swagger\Client\Model\GeoLockProfileResponse getGeoLockProfile($id)



Returns GeoLock profile details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GeoLockProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the GeoLock profile

try {
    $result = $apiInstance->getGeoLockProfile($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeoLockProfilesApi->getGeoLockProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the GeoLock profile |

### Return type

[**\Swagger\Client\Model\GeoLockProfileResponse**](../Model/GeoLockProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listGeoLockProfiles**
> \Swagger\Client\Model\GeoLockProfileListResponse listGeoLockProfiles($owner, $recurse, $offset, $limit, $sort, $filter)



Retrieve a list of GeoLock profiles for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GeoLockProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id you are requesting data for
$recurse = true; // bool | Load items from the parent as well
$offset = 1.2; // double | An offset into the result set, useful for pagination
$limit = 1.2; // double | Limit the number of results to this value.
$sort = "sort_example"; // string | Sorting column or attribute name with an optional direction, e.g. `sort=name:desc`
$filter = "filter_example"; // string | A filter to apply to the data in RQL format.

try {
    $result = $apiInstance->listGeoLockProfiles($owner, $recurse, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeoLockProfilesApi->listGeoLockProfiles: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id you are requesting data for |
 **recurse** | **bool**| Load items from the parent as well | [optional]
 **offset** | **double**| An offset into the result set, useful for pagination | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **sort** | **string**| Sorting column or attribute name with an optional direction, e.g. &#x60;sort&#x3D;name:desc&#x60; | [optional]
 **filter** | **string**| A filter to apply to the data in RQL format. | [optional]

### Return type

[**\Swagger\Client\Model\GeoLockProfileListResponse**](../Model/GeoLockProfileListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateGeoLockProfile**
> \Swagger\Client\Model\GeoLockProfileResponse updateGeoLockProfile($id, $request)



Updates an existing GeoLock Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GeoLockProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the GeoLock Profile
$request = new \Swagger\Client\Model\GeoLockProfileUpdateRequest(); // \Swagger\Client\Model\GeoLockProfileUpdateRequest | 

try {
    $result = $apiInstance->updateGeoLockProfile($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeoLockProfilesApi->updateGeoLockProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the GeoLock Profile |
 **request** | [**\Swagger\Client\Model\GeoLockProfileUpdateRequest**](../Model/GeoLockProfileUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\GeoLockProfileResponse**](../Model/GeoLockProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

