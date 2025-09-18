# Swagger\Client\DataApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**acknowledgeAlert**](DataApi.md#acknowledgeAlert) | **POST** /data/feeds/alerts/{client}/acknowledge/{alert} | 
[**addTripLabels**](DataApi.md#addTripLabels) | **POST** /data/history/trips/{asset}/{date}/labels | 
[**clearTripPrivate**](DataApi.md#clearTripPrivate) | **DELETE** /data/history/trips/{asset}/{date}/private | 
[**commentAlert**](DataApi.md#commentAlert) | **POST** /data/feeds/alerts/{client}/comment/{alert} | 
[**getAlertFeed**](DataApi.md#getAlertFeed) | **GET** /data/feeds/alerts/{client} | 
[**getAlertHistory**](DataApi.md#getAlertHistory) | **GET** /data/history/alerts/{id} | 
[**getAuditFeedForEntity**](DataApi.md#getAuditFeedForEntity) | **GET** /data/feeds/audit/{company}/entity/{entity} | 
[**getEventFeed**](DataApi.md#getEventFeed) | **GET** /data/feeds/events/{client} | 
[**getEventHistory**](DataApi.md#getEventHistory) | **GET** /data/history/events/{id} | 
[**getLocationFeed**](DataApi.md#getLocationFeed) | **GET** /data/feeds/location/{client} | 
[**getLogHistoryForEntity**](DataApi.md#getLogHistoryForEntity) | **GET** /data/history/logs/{entityType}/{id} | 
[**getNotificationFeed**](DataApi.md#getNotificationFeed) | **GET** /data/feeds/notifications | 
[**getTelemetryHistory**](DataApi.md#getTelemetryHistory) | **GET** /data/history/telemetry/{id} | 
[**getTripFeed**](DataApi.md#getTripFeed) | **GET** /data/feeds/trips/{client} | 
[**getTripHistory**](DataApi.md#getTripHistory) | **GET** /data/history/trips/{id} | 
[**removeTripLabels**](DataApi.md#removeTripLabels) | **DELETE** /data/history/trips/{asset}/{date}/labels | 
[**setTripPrivate**](DataApi.md#setTripPrivate) | **POST** /data/history/trips/{asset}/{date}/private | 


# **acknowledgeAlert**
> \Swagger\Client\Model\EventResponse acknowledgeAlert($client, $alert, $request)



Acknowlege an alert.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client id you are requesting data for
$alert = "alert_example"; // string | The alert id you wish to acknowledge.
$request = new \Swagger\Client\Model\EventCommentRequest(); // \Swagger\Client\Model\EventCommentRequest | 

try {
    $result = $apiInstance->acknowledgeAlert($client, $alert, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->acknowledgeAlert: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client id you are requesting data for |
 **alert** | **string**| The alert id you wish to acknowledge. |
 **request** | [**\Swagger\Client\Model\EventCommentRequest**](../Model/EventCommentRequest.md)|  |

### Return type

[**\Swagger\Client\Model\EventResponse**](../Model/EventResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->addTripLabels: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->clearTripPrivate: ', $e->getMessage(), PHP_EOL;
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

# **commentAlert**
> \Swagger\Client\Model\EventResponse commentAlert($client, $alert, $request)



Add a comment to an alert.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client id you are requesting data for
$alert = "alert_example"; // string | The alert id you wish to comment on.
$request = new \Swagger\Client\Model\EventCommentRequest(); // \Swagger\Client\Model\EventCommentRequest | 

try {
    $result = $apiInstance->commentAlert($client, $alert, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->commentAlert: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client id you are requesting data for |
 **alert** | **string**| The alert id you wish to comment on. |
 **request** | [**\Swagger\Client\Model\EventCommentRequest**](../Model/EventCommentRequest.md)|  |

### Return type

[**\Swagger\Client\Model\EventResponse**](../Model/EventResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAlertFeed**
> \Swagger\Client\Model\EventFeedResponse getAlertFeed($client, $sequence, $direction, $limit, $asset, $alert)



Retrieve an alert feed for the specified asset.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client id you are requesting data for
$sequence = 1.2; // double | The sequence to continue from.
$direction = "direction_example"; // string | The direction to run the feed in.
$limit = 1.2; // double | Limit the number of results to this value. This function may return slightly more results than requested.
$asset = "asset_example"; // string | Filter alerts for this asset only.
$alert = "alert_example"; // string | Filter alerts for this alert only.

try {
    $result = $apiInstance->getAlertFeed($client, $sequence, $direction, $limit, $asset, $alert);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->getAlertFeed: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client id you are requesting data for |
 **sequence** | **double**| The sequence to continue from. |
 **direction** | **string**| The direction to run the feed in. |
 **limit** | **double**| Limit the number of results to this value. This function may return slightly more results than requested. | [optional]
 **asset** | **string**| Filter alerts for this asset only. | [optional]
 **alert** | **string**| Filter alerts for this alert only. | [optional]

### Return type

[**\Swagger\Client\Model\EventFeedResponse**](../Model/EventFeedResponse.md)

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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->getAlertHistory: ', $e->getMessage(), PHP_EOL;
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

# **getAuditFeedForEntity**
> \Swagger\Client\Model\AuditEventFeedResponse getAuditFeedForEntity($company, $entity, $sequence, $direction, $limit)



Retrieve an audit log feed for the specified client and entity.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$company = "company_example"; // string | The client, vendor or distributor id you are requesting data for
$entity = "entity_example"; // string | 
$sequence = 1.2; // double | The sequence to continue from.
$direction = "direction_example"; // string | The direction to run the feed in.
$limit = 1.2; // double | Limit the number of results to this value.

try {
    $result = $apiInstance->getAuditFeedForEntity($company, $entity, $sequence, $direction, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->getAuditFeedForEntity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company** | **string**| The client, vendor or distributor id you are requesting data for |
 **entity** | **string**|  |
 **sequence** | **double**| The sequence to continue from. |
 **direction** | **string**| The direction to run the feed in. |
 **limit** | **double**| Limit the number of results to this value. |

### Return type

[**\Swagger\Client\Model\AuditEventFeedResponse**](../Model/AuditEventFeedResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getEventFeed**
> \Swagger\Client\Model\EventFeedResponse getEventFeed($client, $sequence, $direction, $limit, $asset)



Retrieve an event feed for the specified asset.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client id you are requesting data for
$sequence = 1.2; // double | The sequence to continue from.
$direction = "direction_example"; // string | The direction to run the feed in.
$limit = 1.2; // double | Limit the number of results to this value.
$asset = "asset_example"; // string | Filter events for this asset only.

try {
    $result = $apiInstance->getEventFeed($client, $sequence, $direction, $limit, $asset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->getEventFeed: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client id you are requesting data for |
 **sequence** | **double**| The sequence to continue from. |
 **direction** | **string**| The direction to run the feed in. |
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **asset** | **string**| Filter events for this asset only. | [optional]

### Return type

[**\Swagger\Client\Model\EventFeedResponse**](../Model/EventFeedResponse.md)

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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->getEventHistory: ', $e->getMessage(), PHP_EOL;
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

# **getLocationFeed**
> \Swagger\Client\Model\TelemetryFeedResponse getLocationFeed($client, $sequence, $offset, $limit, $sort, $filter)



Retrieve the current state for all assets for the specified client.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client id you're requesting data for.
$sequence = 1.2; // double | The sequence to continue from.
$offset = 1.2; // double | 
$limit = 1.2; // double | Limit the number of results to this value.
$sort = "sort_example"; // string | 
$filter = "filter_example"; // string | 

try {
    $result = $apiInstance->getLocationFeed($client, $sequence, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->getLocationFeed: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client id you&#39;re requesting data for. |
 **sequence** | **double**| The sequence to continue from. |
 **offset** | **double**|  | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **sort** | **string**|  | [optional]
 **filter** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\TelemetryFeedResponse**](../Model/TelemetryFeedResponse.md)

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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->getLogHistoryForEntity: ', $e->getMessage(), PHP_EOL;
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

# **getNotificationFeed**
> \Swagger\Client\Model\NotificationFeedResponse getNotificationFeed($sequence, $direction, $limit)



Retrieve the notification feed for the current user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sequence = 1.2; // double | The sequence to continue from.
$direction = "direction_example"; // string | The direction to run the feed in.
$limit = 1.2; // double | Limit the number of results to this value.

try {
    $result = $apiInstance->getNotificationFeed($sequence, $direction, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->getNotificationFeed: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sequence** | **double**| The sequence to continue from. |
 **direction** | **string**| The direction to run the feed in. |
 **limit** | **double**| Limit the number of results to this value. | [optional]

### Return type

[**\Swagger\Client\Model\NotificationFeedResponse**](../Model/NotificationFeedResponse.md)

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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->getTelemetryHistory: ', $e->getMessage(), PHP_EOL;
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

# **getTripFeed**
> \Swagger\Client\Model\TripFeedResponse getTripFeed($client, $sequence, $direction, $limit, $asset)



Retrieve a trip feed for the specified asset.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client id you are requesting data for
$sequence = 1.2; // double | The sequence to continue from.
$direction = "direction_example"; // string | The direction to run the feed in.
$limit = 1.2; // double | Limit the number of results to this value.
$asset = "asset_example"; // string | 

try {
    $result = $apiInstance->getTripFeed($client, $sequence, $direction, $limit, $asset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->getTripFeed: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client id you are requesting data for |
 **sequence** | **double**| The sequence to continue from. |
 **direction** | **string**| The direction to run the feed in. |
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **asset** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\TripFeedResponse**](../Model/TripFeedResponse.md)

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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->getTripHistory: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->removeTripLabels: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\DataApi(
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
    echo 'Exception when calling DataApi->setTripPrivate: ', $e->getMessage(), PHP_EOL;
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

