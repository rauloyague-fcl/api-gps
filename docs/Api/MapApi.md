# Swagger\Client\MapApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**geocodeForward**](MapApi.md#geocodeForward) | **GET** /map/geocode/{client}/forward | 
[**geocodeReverse**](MapApi.md#geocodeReverse) | **GET** /map/geocode/{client}/reverse | 
[**getRoute**](MapApi.md#getRoute) | **GET** /map/routing/{client}/route | 


# **geocodeForward**
> \Swagger\Client\Model\ForwardGeocodeResponse geocodeForward($client, $query)



Perform a free text search against map addresses and zones.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MapApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client UUID for whom geocoding is being done
$query = "query_example"; // string | The free text query you'd like to search for

try {
    $result = $apiInstance->geocodeForward($client, $query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapApi->geocodeForward: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client UUID for whom geocoding is being done |
 **query** | **string**| The free text query you&#39;d like to search for |

### Return type

[**\Swagger\Client\Model\ForwardGeocodeResponse**](../Model/ForwardGeocodeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **geocodeReverse**
> \Swagger\Client\Model\ReverseGeocodeResponse geocodeReverse($client, $lat, $lon)



Perform a reverse geocode text search against map addresses.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MapApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client UUID for whom geocoding is being done
$lat = 1.2; // double | The latitude to search for
$lon = 1.2; // double | The longitude to search for

try {
    $result = $apiInstance->geocodeReverse($client, $lat, $lon);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapApi->geocodeReverse: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client UUID for whom geocoding is being done |
 **lat** | **double**| The latitude to search for |
 **lon** | **double**| The longitude to search for |

### Return type

[**\Swagger\Client\Model\ReverseGeocodeResponse**](../Model/ReverseGeocodeResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRoute**
> \Swagger\Client\Model\MapRouteResponse getRoute($client, $strategy, $coords, $src)



Route between two points on a map.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\MapApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client = "client_example"; // string | The client UUID for whom geocoding is being done
$strategy = "strategy_example"; // string | The routing strategy to employ while calculating the route, in the format `fastest,longest`
$coords = "coords_example"; // string | The coordinate pairs to route between in the format `[lon,lat],[lon,lat]`
$src = "src_example"; // string | 

try {
    $result = $apiInstance->getRoute($client, $strategy, $coords, $src);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapApi->getRoute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | **string**| The client UUID for whom geocoding is being done |
 **strategy** | **string**| The routing strategy to employ while calculating the route, in the format &#x60;fastest,longest&#x60; |
 **coords** | **string**| The coordinate pairs to route between in the format &#x60;[lon,lat],[lon,lat]&#x60; |
 **src** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\MapRouteResponse**](../Model/MapRouteResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

