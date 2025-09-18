# Swagger\Client\DeviceTypesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDeviceType**](DeviceTypesApi.md#createDeviceType) | **POST** /entities/devicetypes | 
[**getDeviceType**](DeviceTypesApi.md#getDeviceType) | **GET** /entities/devicetypes/{id} | 
[**listDeviceTypes**](DeviceTypesApi.md#listDeviceTypes) | **GET** /entities/devicetypes | 
[**updateDeviceType**](DeviceTypesApi.md#updateDeviceType) | **PUT** /entities/devicetypes/{id} | 


# **createDeviceType**
> \Swagger\Client\Model\DeviceTypeResponse createDeviceType($request)



Creates a new device type entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DeviceTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\DeviceTypeCreateRequest(); // \Swagger\Client\Model\DeviceTypeCreateRequest | 

try {
    $result = $apiInstance->createDeviceType($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceTypesApi->createDeviceType: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\DeviceTypeCreateRequest**](../Model/DeviceTypeCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\DeviceTypeResponse**](../Model/DeviceTypeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDeviceType**
> \Swagger\Client\Model\DeviceTypeResponse getDeviceType($id, $owner)



Returns device type details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DeviceTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the device
$owner = "owner_example"; // string | The optional UUID of a Client. The device type may be customized based on settings and features in the client.

try {
    $result = $apiInstance->getDeviceType($id, $owner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceTypesApi->getDeviceType: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the device |
 **owner** | **string**| The optional UUID of a Client. The device type may be customized based on settings and features in the client. | [optional]

### Return type

[**\Swagger\Client\Model\DeviceTypeResponse**](../Model/DeviceTypeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listDeviceTypes**
> \Swagger\Client\Model\DeviceTypeListResponse listDeviceTypes($owner, $recurse, $offset, $limit, $sort, $filter)



Retrieve a list of device types for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DeviceTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id you are requesting data for
$recurse = true; // bool | Load items from the parent company tree as well (defaults to \"true\")
$offset = 1.2; // double | An offset into the result set, useful for pagination
$limit = 1.2; // double | Limit the number of results to this value.
$sort = "sort_example"; // string | Sorting column or attribute name with an optional direction, e.g. `sort=name:desc`
$filter = "filter_example"; // string | A filter to apply to the data in RQL format.

try {
    $result = $apiInstance->listDeviceTypes($owner, $recurse, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceTypesApi->listDeviceTypes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id you are requesting data for |
 **recurse** | **bool**| Load items from the parent company tree as well (defaults to \&quot;true\&quot;) | [optional]
 **offset** | **double**| An offset into the result set, useful for pagination | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **sort** | **string**| Sorting column or attribute name with an optional direction, e.g. &#x60;sort&#x3D;name:desc&#x60; | [optional]
 **filter** | **string**| A filter to apply to the data in RQL format. | [optional]

### Return type

[**\Swagger\Client\Model\DeviceTypeListResponse**](../Model/DeviceTypeListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateDeviceType**
> \Swagger\Client\Model\DeviceTypeResponse updateDeviceType($id, $request)



Updates an existing device type

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DeviceTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$request = new \Swagger\Client\Model\DeviceTypeUpdateRequest(); // \Swagger\Client\Model\DeviceTypeUpdateRequest | 

try {
    $result = $apiInstance->updateDeviceType($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceTypesApi->updateDeviceType: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **request** | [**\Swagger\Client\Model\DeviceTypeUpdateRequest**](../Model/DeviceTypeUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\DeviceTypeResponse**](../Model/DeviceTypeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

