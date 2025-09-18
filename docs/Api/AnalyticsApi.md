# Swagger\Client\AnalyticsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAnalyticsBaseReport**](AnalyticsApi.md#getAnalyticsBaseReport) | **GET** /reports/analytics/{id} | 
[**listAnalyticsBaseReports**](AnalyticsApi.md#listAnalyticsBaseReports) | **GET** /reports/analytics | 
[**rebuildAnalyticsBaseReport**](AnalyticsApi.md#rebuildAnalyticsBaseReport) | **POST** /reports/analytics/{id}/rebuild | 


# **getAnalyticsBaseReport**
> \Swagger\Client\Model\AnalyticsBaseReportResponse getAnalyticsBaseReport($id)



Retrieve an analytics base report by its ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AnalyticsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID to retrieve.

try {
    $result = $apiInstance->getAnalyticsBaseReport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsApi->getAnalyticsBaseReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID to retrieve. |

### Return type

[**\Swagger\Client\Model\AnalyticsBaseReportResponse**](../Model/AnalyticsBaseReportResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listAnalyticsBaseReports**
> \Swagger\Client\Model\AnalyticsBaseReportsListResponse listAnalyticsBaseReports($owner, $client, $user, $offset, $limit)



Retrieve a list of base reports for a specified owner, client or user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AnalyticsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | 
$client = "client_example"; // string | 
$user = "user_example"; // string | 
$offset = 1.2; // double | 
$limit = 1.2; // double | 

try {
    $result = $apiInstance->listAnalyticsBaseReports($owner, $client, $user, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsApi->listAnalyticsBaseReports: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**|  | [optional]
 **client** | **string**|  | [optional]
 **user** | **string**|  | [optional]
 **offset** | **double**|  | [optional]
 **limit** | **double**|  | [optional]

### Return type

[**\Swagger\Client\Model\AnalyticsBaseReportsListResponse**](../Model/AnalyticsBaseReportsListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **rebuildAnalyticsBaseReport**
> rebuildAnalyticsBaseReport($id)



Rebuilds a base report

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AnalyticsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->rebuildAnalyticsBaseReport($id);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsApi->rebuildAnalyticsBaseReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

