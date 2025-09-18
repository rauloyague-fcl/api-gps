# Swagger\Client\SmsGatewayProvidersApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSmsGatewayProvider**](SmsGatewayProvidersApi.md#createSmsGatewayProvider) | **POST** /entities/smsgatewayproviders | 
[**getSmsGatewayProvider**](SmsGatewayProvidersApi.md#getSmsGatewayProvider) | **GET** /entities/smsgatewayproviders/{id} | 
[**listSmsGatewayProviders**](SmsGatewayProvidersApi.md#listSmsGatewayProviders) | **GET** /entities/smsgatewayproviders | 
[**updateSmsGatewayProvider**](SmsGatewayProvidersApi.md#updateSmsGatewayProvider) | **PUT** /entities/smsgatewayproviders/{id} | 


# **createSmsGatewayProvider**
> \Swagger\Client\Model\SmsGatewayProviderResponse createSmsGatewayProvider($request)



Creates a new sms gateway provider entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SmsGatewayProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\SmsGatewayProviderCreateRequest(); // \Swagger\Client\Model\SmsGatewayProviderCreateRequest | 

try {
    $result = $apiInstance->createSmsGatewayProvider($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsGatewayProvidersApi->createSmsGatewayProvider: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\SmsGatewayProviderCreateRequest**](../Model/SmsGatewayProviderCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SmsGatewayProviderResponse**](../Model/SmsGatewayProviderResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSmsGatewayProvider**
> \Swagger\Client\Model\SmsGatewayProviderResponse getSmsGatewayProvider($id)



Returns sms gateway provider details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SmsGatewayProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the entity

try {
    $result = $apiInstance->getSmsGatewayProvider($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsGatewayProvidersApi->getSmsGatewayProvider: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the entity |

### Return type

[**\Swagger\Client\Model\SmsGatewayProviderResponse**](../Model/SmsGatewayProviderResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listSmsGatewayProviders**
> \Swagger\Client\Model\SmsGatewayProviderListResponse listSmsGatewayProviders($owner, $offset, $limit, $sort, $filter)



Retrieve a list of sms gateway providers.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SmsGatewayProvidersApi(
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
    $result = $apiInstance->listSmsGatewayProviders($owner, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsGatewayProvidersApi->listSmsGatewayProviders: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\SmsGatewayProviderListResponse**](../Model/SmsGatewayProviderListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateSmsGatewayProvider**
> \Swagger\Client\Model\SmsGatewayProviderResponse updateSmsGatewayProvider($id, $request)



Updates an existing sms gateway provider entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SmsGatewayProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the sms gateway provider
$request = new \Swagger\Client\Model\SmsGatewayProviderUpdateRequest(); // \Swagger\Client\Model\SmsGatewayProviderUpdateRequest | 

try {
    $result = $apiInstance->updateSmsGatewayProvider($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsGatewayProvidersApi->updateSmsGatewayProvider: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the sms gateway provider |
 **request** | [**\Swagger\Client\Model\SmsGatewayProviderUpdateRequest**](../Model/SmsGatewayProviderUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SmsGatewayProviderResponse**](../Model/SmsGatewayProviderResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

