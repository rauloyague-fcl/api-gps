# Swagger\Client\AssetsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAsset**](AssetsApi.md#createAsset) | **POST** /entities/assets | 
[**createSharedAssetLocationToken**](AssetsApi.md#createSharedAssetLocationToken) | **POST** /entities/assets/shared/location/{id} | 
[**deleteAssetAvatar**](AssetsApi.md#deleteAssetAvatar) | **DELETE** /entities/assets/{id}/avatar | 
[**deleteSharedAssetLocationToken**](AssetsApi.md#deleteSharedAssetLocationToken) | **DELETE** /entities/assets/shared/location/{token} | 
[**getAsset**](AssetsApi.md#getAsset) | **GET** /entities/assets/{id} | 
[**getAssetAvatar**](AssetsApi.md#getAssetAvatar) | **GET** /entities/assets/{id}/avatar | 
[**getAssetDeviceConfiguration**](AssetsApi.md#getAssetDeviceConfiguration) | **GET** /entities/assets/{id}/deviceconfig | 
[**getAssetLocation**](AssetsApi.md#getAssetLocation) | **GET** /entities/assets/{id}/location | 
[**getSharedAssetLocation**](AssetsApi.md#getSharedAssetLocation) | **GET** /entities/assets/shared/location/{token} | 
[**linkAssets**](AssetsApi.md#linkAssets) | **POST** /entities/assets/{id}/link | 
[**listAssets**](AssetsApi.md#listAssets) | **GET** /entities/assets | 
[**listSharedAssetLocationTokens**](AssetsApi.md#listSharedAssetLocationTokens) | **GET** /entities/assets/shared/location | 
[**moveAsset**](AssetsApi.md#moveAsset) | **POST** /entities/assets/{id}/move | 
[**setAssetPrivacy**](AssetsApi.md#setAssetPrivacy) | **PUT** /entities/assets/{id}/privacy | 
[**unlinkAssets**](AssetsApi.md#unlinkAssets) | **POST** /entities/assets/{id}/unlink/{asset} | 
[**updateAsset**](AssetsApi.md#updateAsset) | **PUT** /entities/assets/{id} | 
[**updateAssetAvatar**](AssetsApi.md#updateAssetAvatar) | **POST** /entities/assets/{id}/avatar | 
[**updateSharedAssetLocationToken**](AssetsApi.md#updateSharedAssetLocationToken) | **PUT** /entities/assets/shared/location/{token} | 


# **createAsset**
> \Swagger\Client\Model\AssetResponse createAsset($request)



Creates a new asset entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\AssetCreateRequest(); // \Swagger\Client\Model\AssetCreateRequest | 

try {
    $result = $apiInstance->createAsset($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->createAsset: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\AssetCreateRequest**](../Model/AssetCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetResponse**](../Model/AssetResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createSharedAssetLocationToken**
> \Swagger\Client\Model\AssetSharedLocationTokenResponse createSharedAssetLocationToken($id, $request)



Creates a new shared asset location token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset
$request = new \Swagger\Client\Model\AssetSharedLocationTokenRequest(); // \Swagger\Client\Model\AssetSharedLocationTokenRequest | 

try {
    $result = $apiInstance->createSharedAssetLocationToken($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->createSharedAssetLocationToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset |
 **request** | [**\Swagger\Client\Model\AssetSharedLocationTokenRequest**](../Model/AssetSharedLocationTokenRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetSharedLocationTokenResponse**](../Model/AssetSharedLocationTokenResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteAssetAvatar**
> deleteAssetAvatar($id)



Permanently deletes a asset avatar.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The asset UUID.

try {
    $apiInstance->deleteAssetAvatar($id);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->deleteAssetAvatar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The asset UUID. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteSharedAssetLocationToken**
> \Swagger\Client\Model\AssetSharedLocationTokenResponse deleteSharedAssetLocationToken($token)



Deletes a shared asset location token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token = "token_example"; // string | The shared asset token to delete

try {
    $result = $apiInstance->deleteSharedAssetLocationToken($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->deleteSharedAssetLocationToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **string**| The shared asset token to delete |

### Return type

[**\Swagger\Client\Model\AssetSharedLocationTokenResponse**](../Model/AssetSharedLocationTokenResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAsset**
> \Swagger\Client\Model\AssetResponse getAsset($id)



Returns asset details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset

try {
    $result = $apiInstance->getAsset($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->getAsset: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset |

### Return type

[**\Swagger\Client\Model\AssetResponse**](../Model/AssetResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAssetAvatar**
> string getAssetAvatar($id)



Return the asset avatar in binary format

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset

try {
    $result = $apiInstance->getAssetAvatar($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->getAssetAvatar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset |

### Return type

**string**

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAssetDeviceConfiguration**
> \Swagger\Client\Model\DeviceConfigurationResponse getAssetDeviceConfiguration($id)



Returns the device configuration of the device attached to this asset (also works for cloned assets)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset

try {
    $result = $apiInstance->getAssetDeviceConfiguration($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->getAssetDeviceConfiguration: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset |

### Return type

[**\Swagger\Client\Model\DeviceConfigurationResponse**](../Model/DeviceConfigurationResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAssetLocation**
> \Swagger\Client\Model\TelemetryStateResponse getAssetLocation($id)



Returns the latest known telemetry record for an asset

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset

try {
    $result = $apiInstance->getAssetLocation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->getAssetLocation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset |

### Return type

[**\Swagger\Client\Model\TelemetryStateResponse**](../Model/TelemetryStateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSharedAssetLocation**
> \Swagger\Client\Model\AssetSharedLocationResponse getSharedAssetLocation($token)



Returns the latest known telemetry record for an asset using a shared token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$token = "token_example"; // string | The shared token

try {
    $result = $apiInstance->getSharedAssetLocation($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->getSharedAssetLocation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **string**| The shared token |

### Return type

[**\Swagger\Client\Model\AssetSharedLocationResponse**](../Model/AssetSharedLocationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **linkAssets**
> \Swagger\Client\Model\AssetLinkResponse linkAssets($id, $request)



Links an asset from one account to one in another account. All data from the source asset will be duplicated for the destination asset. Returns both the source and destination asset if successful.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The source asset UUID you would like to link.
$request = new \Swagger\Client\Model\AssetLinkRequest(); // \Swagger\Client\Model\AssetLinkRequest | 

try {
    $result = $apiInstance->linkAssets($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->linkAssets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The source asset UUID you would like to link. |
 **request** | [**\Swagger\Client\Model\AssetLinkRequest**](../Model/AssetLinkRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetLinkResponse**](../Model/AssetLinkResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listAssets**
> \Swagger\Client\Model\AssetListResponse listAssets($owner, $offset, $limit, $sort, $filter)



Retrieve a list of assets for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
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
    $result = $apiInstance->listAssets($owner, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->listAssets: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\AssetListResponse**](../Model/AssetListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listSharedAssetLocationTokens**
> \Swagger\Client\Model\AssetSharedLocationTokenListResponse listSharedAssetLocationTokens($owner, $asset, $offset, $limit, $sort, $filter)



Retrieve a list of shared asset tokens for an asset or client.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id you are requesting data for
$asset = "asset_example"; // string | The asset id you are requesting data for
$offset = 1.2; // double | An offset into the result set, useful for pagination
$limit = 1.2; // double | Limit the number of results to this value.
$sort = "sort_example"; // string | Sorting column or attribute name with an optional direction, e.g. `sort=name:desc`
$filter = "filter_example"; // string | A filter to apply to the data in RQL format.

try {
    $result = $apiInstance->listSharedAssetLocationTokens($owner, $asset, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->listSharedAssetLocationTokens: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id you are requesting data for | [optional]
 **asset** | **string**| The asset id you are requesting data for | [optional]
 **offset** | **double**| An offset into the result set, useful for pagination | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **sort** | **string**| Sorting column or attribute name with an optional direction, e.g. &#x60;sort&#x3D;name:desc&#x60; | [optional]
 **filter** | **string**| A filter to apply to the data in RQL format. | [optional]

### Return type

[**\Swagger\Client\Model\AssetSharedLocationTokenListResponse**](../Model/AssetSharedLocationTokenListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **moveAsset**
> \Swagger\Client\Model\AssetResponse moveAsset($id, $request)



Moves an asset from one client to another by deleting the asset in the source client and recreating it in the destination client. Also moves any associated device and simcard if assigned.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The asset UUID you would like to move.
$request = new \Swagger\Client\Model\AssetMoveRequest(); // \Swagger\Client\Model\AssetMoveRequest | 

try {
    $result = $apiInstance->moveAsset($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->moveAsset: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The asset UUID you would like to move. |
 **request** | [**\Swagger\Client\Model\AssetMoveRequest**](../Model/AssetMoveRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetResponse**](../Model/AssetResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setAssetPrivacy**
> \Swagger\Client\Model\AssetResponse setAssetPrivacy($id, $request)



Update asset privacy mode

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the asset
$request = new \Swagger\Client\Model\AssetPrivacyRequest(); // \Swagger\Client\Model\AssetPrivacyRequest | 

try {
    $result = $apiInstance->setAssetPrivacy($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->setAssetPrivacy: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the asset |
 **request** | [**\Swagger\Client\Model\AssetPrivacyRequest**](../Model/AssetPrivacyRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetResponse**](../Model/AssetResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **unlinkAssets**
> \Swagger\Client\Model\AssetLinkResponse unlinkAssets($id, $asset)



Unlinks an asset linked to another.  Returns both the source and destination asset if successful.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The source asset UUID you would like to unlink from.
$asset = "asset_example"; // string | The destination asset UUID you would like to unlink from.

try {
    $result = $apiInstance->unlinkAssets($id, $asset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->unlinkAssets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The source asset UUID you would like to unlink from. |
 **asset** | **string**| The destination asset UUID you would like to unlink from. |

### Return type

[**\Swagger\Client\Model\AssetLinkResponse**](../Model/AssetLinkResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateAsset**
> \Swagger\Client\Model\AssetResponse updateAsset($id, $request)



Updates an existing asset

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$request = new \Swagger\Client\Model\AssetUpdateRequest(); // \Swagger\Client\Model\AssetUpdateRequest | 

try {
    $result = $apiInstance->updateAsset($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->updateAsset: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **request** | [**\Swagger\Client\Model\AssetUpdateRequest**](../Model/AssetUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetResponse**](../Model/AssetResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateAssetAvatar**
> updateAssetAvatar($id)



Updates the specified asset's avatar.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The asset UUID you are requesting data for.

try {
    $apiInstance->updateAssetAvatar($id);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->updateAssetAvatar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The asset UUID you are requesting data for. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateSharedAssetLocationToken**
> \Swagger\Client\Model\AssetSharedLocationTokenResponse updateSharedAssetLocationToken($token, $request)



Update a shared asset location token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\AssetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token = "token_example"; // string | The shared asset token to update
$request = new \Swagger\Client\Model\AssetSharedLocationTokenRequest(); // \Swagger\Client\Model\AssetSharedLocationTokenRequest | 

try {
    $result = $apiInstance->updateSharedAssetLocationToken($token, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetsApi->updateSharedAssetLocationToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **string**| The shared asset token to update |
 **request** | [**\Swagger\Client\Model\AssetSharedLocationTokenRequest**](../Model/AssetSharedLocationTokenRequest.md)|  |

### Return type

[**\Swagger\Client\Model\AssetSharedLocationTokenResponse**](../Model/AssetSharedLocationTokenResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

