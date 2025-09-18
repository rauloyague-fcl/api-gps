# Swagger\Client\MediaApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelMedia**](MediaApi.md#cancelMedia) | **POST** /media/{id}/cancel | 
[**createVideoEvent**](MediaApi.md#createVideoEvent) | **POST** /media/video/event | 
[**deleteMediaFile**](MediaApi.md#deleteMediaFile) | **DELETE** /media/{id}/file | 
[**getMedia**](MediaApi.md#getMedia) | **GET** /media/{id} | 
[**getMediaFile**](MediaApi.md#getMediaFile) | **GET** /media/{asset}/file | 
[**getMediaInfo**](MediaApi.md#getMediaInfo) | **GET** /media/{asset}/info | 
[**getMediaInfoDeprecated**](MediaApi.md#getMediaInfoDeprecated) | **GET** /media/info/{owner}/{asset}/{filename} | 
[**listMedia**](MediaApi.md#listMedia) | **GET** /media | 
[**saveMedia**](MediaApi.md#saveMedia) | **POST** /media/{id}/save | 
[**startVideoLiveStream**](MediaApi.md#startVideoLiveStream) | **POST** /media/{asset}/livestream | 
[**updateVideoEvent**](MediaApi.md#updateVideoEvent) | **PUT** /media/video/event/{owner}/{event} | 


# **cancelMedia**
> \Swagger\Client\Model\MediaInfoResponse cancelMedia($id)



Cancel a pending or queued media item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The media ID you are canceling

try {
    $result = $apiInstance->cancelMedia($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->cancelMedia: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The media ID you are canceling |

### Return type

[**\Swagger\Client\Model\MediaInfoResponse**](../Model/MediaInfoResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createVideoEvent**
> \Swagger\Client\Model\EventResponse createVideoEvent($request)



Creates a new video event for a specified date time.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\MediaVideoEventCreateRequest(); // \Swagger\Client\Model\MediaVideoEventCreateRequest | 

try {
    $result = $apiInstance->createVideoEvent($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->createVideoEvent: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\MediaVideoEventCreateRequest**](../Model/MediaVideoEventCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\EventResponse**](../Model/EventResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteMediaFile**
> \Swagger\Client\Model\MediaInfoResponse deleteMediaFile($id)



Delete a media item media file

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The media ID you are deleting

try {
    $result = $apiInstance->deleteMediaFile($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->deleteMediaFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The media ID you are deleting |

### Return type

[**\Swagger\Client\Model\MediaInfoResponse**](../Model/MediaInfoResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMedia**
> \Swagger\Client\Model\MediaInfoResponse getMedia($id)



Retrieve a media information item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The media ID you are requesting data for

try {
    $result = $apiInstance->getMedia($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->getMedia: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The media ID you are requesting data for |

### Return type

[**\Swagger\Client\Model\MediaInfoResponse**](../Model/MediaInfoResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMediaFile**
> getMediaFile($asset, $filename)



Retrieve a media item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asset = "asset_example"; // string | The UUID of the asset you are requesting media for.
$filename = "filename_example"; // string | The filename of the media item.

try {
    $apiInstance->getMediaFile($asset, $filename);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->getMediaFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset** | **string**| The UUID of the asset you are requesting media for. |
 **filename** | **string**| The filename of the media item. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMediaInfo**
> \Swagger\Client\Model\MediaInfoResponse getMediaInfo($asset, $filename)



Returns information for a media item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asset = "asset_example"; // string | The UUID of the asset you are requesting media for.
$filename = "filename_example"; // string | The filename of the media item.

try {
    $result = $apiInstance->getMediaInfo($asset, $filename);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->getMediaInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset** | **string**| The UUID of the asset you are requesting media for. |
 **filename** | **string**| The filename of the media item. |

### Return type

[**\Swagger\Client\Model\MediaInfoResponse**](../Model/MediaInfoResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMediaInfoDeprecated**
> \Swagger\Client\Model\MediaInfoResponse getMediaInfoDeprecated($owner, $asset, $filename)



[DEPRECATED] Use getMediaInfo instead

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | 
$asset = "asset_example"; // string | 
$filename = "filename_example"; // string | 

try {
    $result = $apiInstance->getMediaInfoDeprecated($owner, $asset, $filename);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->getMediaInfoDeprecated: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**|  |
 **asset** | **string**|  |
 **filename** | **string**|  |

### Return type

[**\Swagger\Client\Model\MediaInfoResponse**](../Model/MediaInfoResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listMedia**
> \Swagger\Client\Model\MediaInfoListResponse listMedia($owner, $offset, $limit, $filter)



Retrieve a list of media information items for the specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id you are requesting data for
$offset = 1.2; // double | An offset into the result set, useful for pagination
$limit = 1.2; // double | Limit the number of results to this value.
$filter = "filter_example"; // string | A filter to apply to the data in RQL format.

try {
    $result = $apiInstance->listMedia($owner, $offset, $limit, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->listMedia: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id you are requesting data for |
 **offset** | **double**| An offset into the result set, useful for pagination | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **filter** | **string**| A filter to apply to the data in RQL format. | [optional]

### Return type

[**\Swagger\Client\Model\MediaInfoListResponse**](../Model/MediaInfoListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **saveMedia**
> \Swagger\Client\Model\MediaInfoResponse saveMedia($id)



Save a video in the user's saved list.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The media ID you are saving

try {
    $result = $apiInstance->saveMedia($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->saveMedia: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The media ID you are saving |

### Return type

[**\Swagger\Client\Model\MediaInfoResponse**](../Model/MediaInfoResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **startVideoLiveStream**
> \Swagger\Client\Model\VideoLiveStreamResponse startVideoLiveStream($asset, $request)



Requests a live stream endpoint for a video.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asset = "asset_example"; // string | The UUID of the asset you are requesting media for.
$request = new \Swagger\Client\Model\VideoLiveStreamRequest(); // \Swagger\Client\Model\VideoLiveStreamRequest | 

try {
    $result = $apiInstance->startVideoLiveStream($asset, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->startVideoLiveStream: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset** | **string**| The UUID of the asset you are requesting media for. |
 **request** | [**\Swagger\Client\Model\VideoLiveStreamRequest**](../Model/VideoLiveStreamRequest.md)|  |

### Return type

[**\Swagger\Client\Model\VideoLiveStreamResponse**](../Model/VideoLiveStreamResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateVideoEvent**
> \Swagger\Client\Model\EventResponse updateVideoEvent($owner, $event, $request)



Request a video from a camera enabled device for a particular event.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id of the company that owns the event
$event = "event_example"; // string | The GUID of the event for which you wish to retrieve the video
$request = new \Swagger\Client\Model\MediaVideoEventUpdateRequest(); // \Swagger\Client\Model\MediaVideoEventUpdateRequest | 

try {
    $result = $apiInstance->updateVideoEvent($owner, $event, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->updateVideoEvent: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id of the company that owns the event |
 **event** | **string**| The GUID of the event for which you wish to retrieve the video |
 **request** | [**\Swagger\Client\Model\MediaVideoEventUpdateRequest**](../Model/MediaVideoEventUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\EventResponse**](../Model/EventResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

