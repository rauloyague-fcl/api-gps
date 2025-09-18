# Swagger\Client\FeedsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**acknowledgeAlert**](FeedsApi.md#acknowledgeAlert) | **POST** /data/feeds/alerts/{client}/acknowledge/{alert} | 
[**commentAlert**](FeedsApi.md#commentAlert) | **POST** /data/feeds/alerts/{client}/comment/{alert} | 
[**getAlertFeed**](FeedsApi.md#getAlertFeed) | **GET** /data/feeds/alerts/{client} | 
[**getAuditFeedForEntity**](FeedsApi.md#getAuditFeedForEntity) | **GET** /data/feeds/audit/{company}/entity/{entity} | 
[**getEventFeed**](FeedsApi.md#getEventFeed) | **GET** /data/feeds/events/{client} | 
[**getLocationFeed**](FeedsApi.md#getLocationFeed) | **GET** /data/feeds/location/{client} | 
[**getNotificationFeed**](FeedsApi.md#getNotificationFeed) | **GET** /data/feeds/notifications | 
[**getTripFeed**](FeedsApi.md#getTripFeed) | **GET** /data/feeds/trips/{client} | 


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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->acknowledgeAlert: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->commentAlert: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->getAlertFeed: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->getAuditFeedForEntity: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->getEventFeed: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->getLocationFeed: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->getNotificationFeed: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\FeedsApi(
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
    echo 'Exception when calling FeedsApi->getTripFeed: ', $e->getMessage(), PHP_EOL;
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

