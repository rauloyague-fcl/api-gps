# Swagger\Client\OverspeedProfilesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createOverspeedProfile**](OverspeedProfilesApi.md#createOverspeedProfile) | **POST** /entities/overspeedprofiles | 
[**getOverspeedProfile**](OverspeedProfilesApi.md#getOverspeedProfile) | **GET** /entities/overspeedprofiles/{id} | 
[**listOverspeedProfiles**](OverspeedProfilesApi.md#listOverspeedProfiles) | **GET** /entities/overspeedprofiles | 
[**updateOverspeedProfile**](OverspeedProfilesApi.md#updateOverspeedProfile) | **PUT** /entities/overspeedprofiles/{id} | 


# **createOverspeedProfile**
> \Swagger\Client\Model\OverspeedProfileResponse createOverspeedProfile($request)



Creates a new Overspeed Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\OverspeedProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\OverspeedProfileCreateRequest(); // \Swagger\Client\Model\OverspeedProfileCreateRequest | 

try {
    $result = $apiInstance->createOverspeedProfile($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OverspeedProfilesApi->createOverspeedProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\OverspeedProfileCreateRequest**](../Model/OverspeedProfileCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\OverspeedProfileResponse**](../Model/OverspeedProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getOverspeedProfile**
> \Swagger\Client\Model\OverspeedProfileResponse getOverspeedProfile($id)



Returns overspeed profile details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\OverspeedProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the overspeed profile

try {
    $result = $apiInstance->getOverspeedProfile($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OverspeedProfilesApi->getOverspeedProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the overspeed profile |

### Return type

[**\Swagger\Client\Model\OverspeedProfileResponse**](../Model/OverspeedProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listOverspeedProfiles**
> \Swagger\Client\Model\OverspeedProfileListResponse listOverspeedProfiles($owner, $recurse, $offset, $limit, $sort, $filter)



Retrieve a list of overspeed profiles for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\OverspeedProfilesApi(
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
    $result = $apiInstance->listOverspeedProfiles($owner, $recurse, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OverspeedProfilesApi->listOverspeedProfiles: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\OverspeedProfileListResponse**](../Model/OverspeedProfileListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateOverspeedProfile**
> \Swagger\Client\Model\OverspeedProfileResponse updateOverspeedProfile($id, $request)



Updates an existing Overspeed Profile entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\OverspeedProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the Overspeed Profile
$request = new \Swagger\Client\Model\OverspeedProfileUpdateRequest(); // \Swagger\Client\Model\OverspeedProfileUpdateRequest | 

try {
    $result = $apiInstance->updateOverspeedProfile($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OverspeedProfilesApi->updateOverspeedProfile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the Overspeed Profile |
 **request** | [**\Swagger\Client\Model\OverspeedProfileUpdateRequest**](../Model/OverspeedProfileUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\OverspeedProfileResponse**](../Model/OverspeedProfileResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

