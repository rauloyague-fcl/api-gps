# Swagger\Client\HistoryApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addTripLabels**](HistoryApi.md#addTripLabels) | **POST** /data/history/trips/{asset}/{date}/labels | 
[**clearTripPrivate**](HistoryApi.md#clearTripPrivate) | **DELETE** /data/history/trips/{asset}/{date}/private | 
[**getAlertHistory**](HistoryApi.md#getAlertHistory) | **GET** /data/history/alerts/{id} | 
[**getCompletedReport**](HistoryApi.md#getCompletedReport) | **GET** /reports/history/{id} | 
[**getCompletedReportData**](HistoryApi.md#getCompletedReportData) | **GET** /reports/history/{id}/{filename} | 
[**getCompletedReportDataStream**](HistoryApi.md#getCompletedReportDataStream) | **GET** /reports/history/{id}/stream/{filename} | 
[**getCompletedReportDataWithOptions**](HistoryApi.md#getCompletedReportDataWithOptions) | **POST** /reports/history/{id}/{filename} | 
[**getCompletedReportWithOptions**](HistoryApi.md#getCompletedReportWithOptions) | **POST** /reports/history/{id} | 
[**getEventHistory**](HistoryApi.md#getEventHistory) | **GET** /data/history/events/{id} | 
[**getLogHistoryForEntity**](HistoryApi.md#getLogHistoryForEntity) | **GET** /data/history/logs/{entityType}/{id} | 
[**getTelemetryHistory**](HistoryApi.md#getTelemetryHistory) | **GET** /data/history/telemetry/{id} | 
[**getTripHistory**](HistoryApi.md#getTripHistory) | **GET** /data/history/trips/{id} | 
[**listCompletedReports**](HistoryApi.md#listCompletedReports) | **GET** /reports/history | 
[**removeTripLabels**](HistoryApi.md#removeTripLabels) | **DELETE** /data/history/trips/{asset}/{date}/labels | 
[**setTripPrivate**](HistoryApi.md#setTripPrivate) | **POST** /data/history/trips/{asset}/{date}/private | 
[**updateCompletedReport**](HistoryApi.md#updateCompletedReport) | **PUT** /reports/history/{id} | 


# **addTripLabels**
> \Swagger\Client\Model\TripResponse addTripLabels($asset, $date, $request)



Adds one or more labels to a trip.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asset = "asset_example"; // string | The asset id for the trip
$date = "date_example"; // string | The trip start date (in ISO format)
$request = new \Swagger\Client\Model\TripLabelRequest(); // \Swagger\Client\Model\TripLabelRequest | 

try {
    $result = $apiInstance->addTripLabels($asset, $date, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->addTripLabels: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset** | **string**| The asset id for the trip |
 **date** | **string**| The trip start date (in ISO format) |
 **request** | [**\Swagger\Client\Model\TripLabelRequest**](../Model/TripLabelRequest.md)|  |

### Return type

[**\Swagger\Client\Model\TripResponse**](../Model/TripResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **clearTripPrivate**
> \Swagger\Client\Model\TripResponse clearTripPrivate($asset, $date)



Clears the private flag on a trip.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asset = "asset_example"; // string | The asset id for the trip
$date = "date_example"; // string | The trip start date (in ISO format)

try {
    $result = $apiInstance->clearTripPrivate($asset, $date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->clearTripPrivate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset** | **string**| The asset id for the trip |
 **date** | **string**| The trip start date (in ISO format) |

### Return type

[**\Swagger\Client\Model\TripResponse**](../Model/TripResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAlertHistory**
> \Swagger\Client\Model\EventListResponse getAlertHistory($id, $start, $end, $limit)



Retrieve alert records between two dates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The client, alert or asset id you are requesting data for
$start = "start_example"; // string | The start date (in ISO format)
$end = "end_example"; // string | The end date (in ISO format)
$limit = 1.2; // double | Limit the number of results to this value.

try {
    $result = $apiInstance->getAlertHistory($id, $start, $end, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->getAlertHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The client, alert or asset id you are requesting data for |
 **start** | **string**| The start date (in ISO format) |
 **end** | **string**| The end date (in ISO format) |
 **limit** | **double**| Limit the number of results to this value. | [optional]

### Return type

[**\Swagger\Client\Model\EventListResponse**](../Model/EventListResponse.md)

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

$apiInstance = new Swagger\Client\Api\HistoryApi(
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
    echo 'Exception when calling HistoryApi->getCompletedReport: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\HistoryApi(
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
    echo 'Exception when calling HistoryApi->getCompletedReportData: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\HistoryApi(
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
    echo 'Exception when calling HistoryApi->getCompletedReportDataStream: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\HistoryApi(
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
    echo 'Exception when calling HistoryApi->getCompletedReportDataWithOptions: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\HistoryApi(
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
    echo 'Exception when calling HistoryApi->getCompletedReportWithOptions: ', $e->getMessage(), PHP_EOL;
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

# **getEventHistory**
> \Swagger\Client\Model\EventListResponse getEventHistory($id, $start, $end, $limit)



Retrieve event records between two dates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The asset id you are requesting data for
$start = "start_example"; // string | The start date (in ISO format)
$end = "end_example"; // string | The end date (in ISO format)
$limit = 1.2; // double | Limit the number of results to this value.

try {
    $result = $apiInstance->getEventHistory($id, $start, $end, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->getEventHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The asset id you are requesting data for |
 **start** | **string**| The start date (in ISO format) |
 **end** | **string**| The end date (in ISO format) |
 **limit** | **double**| Limit the number of results to this value. | [optional]

### Return type

[**\Swagger\Client\Model\EventListResponse**](../Model/EventListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLogHistoryForEntity**
> \Swagger\Client\Model\LogResponse getLogHistoryForEntity($entity_type, $id, $start, $end, $limit, $levels)



Restricted route, not available for general usage.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$entity_type = "entity_type_example"; // string | 
$id = "id_example"; // string | 
$start = "start_example"; // string | 
$end = "end_example"; // string | 
$limit = 1.2; // double | 
$levels = "levels_example"; // string | 

try {
    $result = $apiInstance->getLogHistoryForEntity($entity_type, $id, $start, $end, $limit, $levels);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->getLogHistoryForEntity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **string**|  |
 **id** | **string**|  |
 **start** | **string**|  | [optional]
 **end** | **string**|  | [optional]
 **limit** | **double**|  | [optional]
 **levels** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\LogResponse**](../Model/LogResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTelemetryHistory**
> \Swagger\Client\Model\TelemetryListResponse getTelemetryHistory($id, $start, $end, $limit)



Retrieve telemetry records between two dates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The asset id you are requesting data for
$start = "start_example"; // string | The start date (in ISO format)
$end = "end_example"; // string | The end date (in ISO format)
$limit = 1.2; // double | Limit the number of results to this value.

try {
    $result = $apiInstance->getTelemetryHistory($id, $start, $end, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->getTelemetryHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The asset id you are requesting data for |
 **start** | **string**| The start date (in ISO format) |
 **end** | **string**| The end date (in ISO format) |
 **limit** | **double**| Limit the number of results to this value. | [optional]

### Return type

[**\Swagger\Client\Model\TelemetryListResponse**](../Model/TelemetryListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTripHistory**
> \Swagger\Client\Model\TripListResponse getTripHistory($id, $start, $end, $date, $limit)



Retrieve trip records between two dates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The asset id you are requesting data for
$start = "start_example"; // string | The start date (in ISO format)
$end = "end_example"; // string | The end date (in ISO format)
$date = "date_example"; // string | Use the date parameter to find the specific trip that contains this date (start and end are ignored)
$limit = 1.2; // double | Limit the number of results to this value.

try {
    $result = $apiInstance->getTripHistory($id, $start, $end, $date, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->getTripHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The asset id you are requesting data for |
 **start** | **string**| The start date (in ISO format) | [optional]
 **end** | **string**| The end date (in ISO format) | [optional]
 **date** | **string**| Use the date parameter to find the specific trip that contains this date (start and end are ignored) | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]

### Return type

[**\Swagger\Client\Model\TripListResponse**](../Model/TripListResponse.md)

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

$apiInstance = new Swagger\Client\Api\HistoryApi(
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
    echo 'Exception when calling HistoryApi->listCompletedReports: ', $e->getMessage(), PHP_EOL;
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

# **removeTripLabels**
> \Swagger\Client\Model\TripResponse removeTripLabels($asset, $date, $request)



Adds one or more labels to a trip.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asset = "asset_example"; // string | The asset id for the trip
$date = "date_example"; // string | The trip start date (in ISO format)
$request = new \Swagger\Client\Model\TripLabelRequest(); // \Swagger\Client\Model\TripLabelRequest | 

try {
    $result = $apiInstance->removeTripLabels($asset, $date, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->removeTripLabels: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset** | **string**| The asset id for the trip |
 **date** | **string**| The trip start date (in ISO format) |
 **request** | [**\Swagger\Client\Model\TripLabelRequest**](../Model/TripLabelRequest.md)|  |

### Return type

[**\Swagger\Client\Model\TripResponse**](../Model/TripResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setTripPrivate**
> \Swagger\Client\Model\TripResponse setTripPrivate($asset, $date)



Sets a trip to private.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HistoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asset = "asset_example"; // string | The asset id for the trip
$date = "date_example"; // string | The trip start date (in ISO format)

try {
    $result = $apiInstance->setTripPrivate($asset, $date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HistoryApi->setTripPrivate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset** | **string**| The asset id for the trip |
 **date** | **string**| The trip start date (in ISO format) |

### Return type

[**\Swagger\Client\Model\TripResponse**](../Model/TripResponse.md)

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

$apiInstance = new Swagger\Client\Api\HistoryApi(
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
    echo 'Exception when calling HistoryApi->updateCompletedReport: ', $e->getMessage(), PHP_EOL;
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

