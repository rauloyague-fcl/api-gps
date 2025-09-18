# Swagger\Client\ReportsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelReport**](ReportsApi.md#cancelReport) | **DELETE** /reports/queues/{id} | 
[**getAnalyticsBaseReport**](ReportsApi.md#getAnalyticsBaseReport) | **GET** /reports/analytics/{id} | 
[**getCompletedReport**](ReportsApi.md#getCompletedReport) | **GET** /reports/history/{id} | 
[**getCompletedReportData**](ReportsApi.md#getCompletedReportData) | **GET** /reports/history/{id}/{filename} | 
[**getCompletedReportDataStream**](ReportsApi.md#getCompletedReportDataStream) | **GET** /reports/history/{id}/stream/{filename} | 
[**getCompletedReportDataWithOptions**](ReportsApi.md#getCompletedReportDataWithOptions) | **POST** /reports/history/{id}/{filename} | 
[**getCompletedReportWithOptions**](ReportsApi.md#getCompletedReportWithOptions) | **POST** /reports/history/{id} | 
[**getQueuedReport**](ReportsApi.md#getQueuedReport) | **GET** /reports/queues/{id} | 
[**listAnalyticsBaseReports**](ReportsApi.md#listAnalyticsBaseReports) | **GET** /reports/analytics | 
[**listCompletedReports**](ReportsApi.md#listCompletedReports) | **GET** /reports/history | 
[**listQueuedReports**](ReportsApi.md#listQueuedReports) | **GET** /reports/queues | 
[**queueReport**](ReportsApi.md#queueReport) | **POST** /reports/queues | 
[**rebuildAnalyticsBaseReport**](ReportsApi.md#rebuildAnalyticsBaseReport) | **POST** /reports/analytics/{id}/rebuild | 
[**updateCompletedReport**](ReportsApi.md#updateCompletedReport) | **PUT** /reports/history/{id} | 


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

$apiInstance = new Swagger\Client\Api\ReportsApi(
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
    echo 'Exception when calling ReportsApi->cancelReport: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\ReportsApi(
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
    echo 'Exception when calling ReportsApi->getAnalyticsBaseReport: ', $e->getMessage(), PHP_EOL;
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

# **getCompletedReport**
> \Swagger\Client\Model\CompletedReportResponse getCompletedReport($id)



Retrieve a queued report by it's ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID to retrieve.

try {
    $result = $apiInstance->getCompletedReport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->getCompletedReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID to retrieve. |

### Return type

[**\Swagger\Client\Model\CompletedReportResponse**](../Model/CompletedReportResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCompletedReportData**
> string getCompletedReportData($id, $filename)



Retrieve the binary data for a queued report by it's ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The UUID to retrieve.
$filename = "filename_example"; // string | The filename and type your want the to be returned as, can be '.pdf', '.csv' or '.json'

try {
    $result = $apiInstance->getCompletedReportData($id, $filename);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->getCompletedReportData: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID to retrieve. |
 **filename** | **string**| The filename and type your want the to be returned as, can be &#39;.pdf&#39;, &#39;.csv&#39; or &#39;.json&#39; |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCompletedReportDataStream**
> getCompletedReportDataStream($id, $filename, $output_format)



Retrieve the binary data for a queued report by it's ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The UUID to retrieve.
$filename = "filename_example"; // string | The filename and type your want the to be returned as, can be '.pdf', '.csv' or '.json'
$output_format = "output_format_example"; // string | 

try {
    $apiInstance->getCompletedReportDataStream($id, $filename, $output_format);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->getCompletedReportDataStream: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID to retrieve. |
 **filename** | **string**| The filename and type your want the to be returned as, can be &#39;.pdf&#39;, &#39;.csv&#39; or &#39;.json&#39; |
 **output_format** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCompletedReportDataWithOptions**
> map[string,null] getCompletedReportDataWithOptions($id, $filename, $options)



Retrieve the binary data for a queued report by it's ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID to retrieve.
$filename = "filename_example"; // string | The filename and type your want the data to be returned as, can be '.pdf', '.csv' or '.json'
$options = new \Swagger\Client\Model\CompletedReportDataRequest(); // \Swagger\Client\Model\CompletedReportDataRequest | 

try {
    $result = $apiInstance->getCompletedReportDataWithOptions($id, $filename, $options);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->getCompletedReportDataWithOptions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID to retrieve. |
 **filename** | **string**| The filename and type your want the data to be returned as, can be &#39;.pdf&#39;, &#39;.csv&#39; or &#39;.json&#39; |
 **options** | [**\Swagger\Client\Model\CompletedReportDataRequest**](../Model/CompletedReportDataRequest.md)|  |

### Return type

**map[string,null]**

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCompletedReportWithOptions**
> \Swagger\Client\Model\CompletedReportResponse getCompletedReportWithOptions($id, $options)



Retrieve a queued report by it's ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID to retrieve.
$options = new \Swagger\Client\Model\CompletedReportRequest(); // \Swagger\Client\Model\CompletedReportRequest | 

try {
    $result = $apiInstance->getCompletedReportWithOptions($id, $options);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->getCompletedReportWithOptions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID to retrieve. |
 **options** | [**\Swagger\Client\Model\CompletedReportRequest**](../Model/CompletedReportRequest.md)|  |

### Return type

[**\Swagger\Client\Model\CompletedReportResponse**](../Model/CompletedReportResponse.md)

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

$apiInstance = new Swagger\Client\Api\ReportsApi(
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
    echo 'Exception when calling ReportsApi->getQueuedReport: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\ReportsApi(
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
    echo 'Exception when calling ReportsApi->listAnalyticsBaseReports: ', $e->getMessage(), PHP_EOL;
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

# **listCompletedReports**
> \Swagger\Client\Model\CompletedReportListResponse listCompletedReports($start, $end, $client, $user)



Retrieve a list of queued reports for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start = "start_example"; // string | 
$end = "end_example"; // string | 
$client = "client_example"; // string | The client id you are requesting reports for
$user = "user_example"; // string | 

try {
    $result = $apiInstance->listCompletedReports($start, $end, $client, $user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->listCompletedReports: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start** | **string**|  |
 **end** | **string**|  |
 **client** | **string**| The client id you are requesting reports for | [optional]
 **user** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\CompletedReportListResponse**](../Model/CompletedReportListResponse.md)

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

$apiInstance = new Swagger\Client\Api\ReportsApi(
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
    echo 'Exception when calling ReportsApi->listQueuedReports: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\ReportsApi(
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
    echo 'Exception when calling ReportsApi->queueReport: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->rebuildAnalyticsBaseReport($id);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->rebuildAnalyticsBaseReport: ', $e->getMessage(), PHP_EOL;
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

# **updateCompletedReport**
> \Swagger\Client\Model\CompletedReportResponse updateCompletedReport($id, $report)



Update a report by it's ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the report to update
$report = new \Swagger\Client\Model\CompletedReportUpdateRequest(); // \Swagger\Client\Model\CompletedReportUpdateRequest | The data with which to update an existing report.

try {
    $result = $apiInstance->updateCompletedReport($id, $report);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->updateCompletedReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the report to update |
 **report** | [**\Swagger\Client\Model\CompletedReportUpdateRequest**](../Model/CompletedReportUpdateRequest.md)| The data with which to update an existing report. |

### Return type

[**\Swagger\Client\Model\CompletedReportResponse**](../Model/CompletedReportResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

