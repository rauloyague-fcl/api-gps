# Swagger\Client\QueuesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelReport**](QueuesApi.md#cancelReport) | **DELETE** /reports/queues/{id} | 
[**getQueuedReport**](QueuesApi.md#getQueuedReport) | **GET** /reports/queues/{id} | 
[**listQueuedReports**](QueuesApi.md#listQueuedReports) | **GET** /reports/queues | 
[**queueReport**](QueuesApi.md#queueReport) | **POST** /reports/queues | 


# **cancelReport**
> \Swagger\Client\Model\QueuedReportResponse cancelReport($id)



Cancel a queued or running report

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\QueuesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->cancelReport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QueuesApi->cancelReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\QueuedReportResponse**](../Model/QueuedReportResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getQueuedReport**
> \Swagger\Client\Model\QueuedReportResponse getQueuedReport($id)



Retrieve a queued report by it's ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\QueuesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID to retrieve.

try {
    $result = $apiInstance->getQueuedReport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QueuesApi->getQueuedReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID to retrieve. |

### Return type

[**\Swagger\Client\Model\QueuedReportResponse**](../Model/QueuedReportResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listQueuedReports**
> \Swagger\Client\Model\QueuedReportListResponse listQueuedReports($client, $user, $server)



Retrieve a list of queued reports for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\QueuesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client id you are requesting reports for
$user = "user_example"; // string | 
$server = "server_example"; // string | An optional server identifier (will be inferred from client settings if possible)

try {
    $result = $apiInstance->listQueuedReports($client, $user, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QueuesApi->listQueuedReports: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client id you are requesting reports for | [optional]
 **user** | **string**|  | [optional]
 **server** | **string**| An optional server identifier (will be inferred from client settings if possible) | [optional]

### Return type

[**\Swagger\Client\Model\QueuedReportListResponse**](../Model/QueuedReportListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queueReport**
> \Swagger\Client\Model\QueuedReportResponse queueReport($request)



Queue a new report

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\QueuesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\QueueReportRequest(); // \Swagger\Client\Model\QueueReportRequest | 

try {
    $result = $apiInstance->queueReport($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QueuesApi->queueReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\QueueReportRequest**](../Model/QueueReportRequest.md)|  |

### Return type

[**\Swagger\Client\Model\QueuedReportResponse**](../Model/QueuedReportResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

