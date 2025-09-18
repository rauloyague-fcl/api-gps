# Swagger\Client\DistributorsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDistributor**](DistributorsApi.md#createDistributor) | **POST** /accounts/distributors | 
[**deleteDistributorLogo**](DistributorsApi.md#deleteDistributorLogo) | **DELETE** /accounts/distributors/{id}/logo | 
[**getDistributor**](DistributorsApi.md#getDistributor) | **GET** /accounts/distributors/{id} | 
[**getDistributorLogo**](DistributorsApi.md#getDistributorLogo) | **GET** /accounts/distributors/{id}/logo | 
[**listDistributors**](DistributorsApi.md#listDistributors) | **GET** /accounts/distributors | 
[**updateDistributor**](DistributorsApi.md#updateDistributor) | **PUT** /accounts/distributors/{id} | 
[**updateDistributorDetails**](DistributorsApi.md#updateDistributorDetails) | **PUT** /accounts/distributors/{id}/details | 
[**updateDistributorLogo**](DistributorsApi.md#updateDistributorLogo) | **POST** /accounts/distributors/{id}/logo | 


# **createDistributor**
> \Swagger\Client\Model\DistributorResponse createDistributor($request)



Creates a new distributor account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\DistributorCreateRequest(); // \Swagger\Client\Model\DistributorCreateRequest | 

try {
    $result = $apiInstance->createDistributor($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->createDistributor: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\DistributorCreateRequest**](../Model/DistributorCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\DistributorResponse**](../Model/DistributorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteDistributorLogo**
> deleteDistributorLogo($id, $size)



Permanently deletes a custom distributor logo. The logo will revert to the Key Telematics logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The distributor UUID.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->deleteDistributorLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->deleteDistributorLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The distributor UUID. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDistributor**
> \Swagger\Client\Model\DistributorResponse getDistributor($id)



Returns distributor details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the distributor

try {
    $result = $apiInstance->getDistributor($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->getDistributor: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the distributor |

### Return type

[**\Swagger\Client\Model\DistributorResponse**](../Model/DistributorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDistributorLogo**
> string getDistributorLogo($id, $size)



Return the specified distributors's logo in binary format. Should the distributor not have a custom logo, the default Key Telematics logo will be supplied.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The distributor UUID you are requesting data for.
$size = "size_example"; // string | The size of the returned image. Can be either \"small\" or \"large\".

try {
    $result = $apiInstance->getDistributorLogo($id, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->getDistributorLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The distributor UUID you are requesting data for. |
 **size** | **string**| The size of the returned image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listDistributors**
> \Swagger\Client\Model\DistributorListResponse listDistributors($owner, $offset, $limit, $sort, $filter, $counts)



Retrieve a list of distributors for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
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
$counts = "counts_example"; // string | A list of entity types to return counts for that belong to this distributor, comma delimited, i.e. `counts=vendor,client,asset,device`. Each additional entity affects the performance of the query and should be used sparingly.

try {
    $result = $apiInstance->listDistributors($owner, $offset, $limit, $sort, $filter, $counts);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->listDistributors: ', $e->getMessage(), PHP_EOL;
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
 **counts** | **string**| A list of entity types to return counts for that belong to this distributor, comma delimited, i.e. &#x60;counts&#x3D;vendor,client,asset,device&#x60;. Each additional entity affects the performance of the query and should be used sparingly. | [optional]

### Return type

[**\Swagger\Client\Model\DistributorListResponse**](../Model/DistributorListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateDistributor**
> \Swagger\Client\Model\DistributorResponse updateDistributor($id, $request)



Updates an existing distributor account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the distributor
$request = new \Swagger\Client\Model\DistributorUpdateRequest(); // \Swagger\Client\Model\DistributorUpdateRequest | 

try {
    $result = $apiInstance->updateDistributor($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->updateDistributor: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the distributor |
 **request** | [**\Swagger\Client\Model\DistributorUpdateRequest**](../Model/DistributorUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\DistributorResponse**](../Model/DistributorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateDistributorDetails**
> \Swagger\Client\Model\DistributorResponse updateDistributorDetails($id, $request)



Updates an existing distributor account details. Unlike `updateDistributor`, this route is available to distributor users.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the distributor
$request = new \Swagger\Client\Model\DistributorDetailsUpdateRequest(); // \Swagger\Client\Model\DistributorDetailsUpdateRequest | 

try {
    $result = $apiInstance->updateDistributorDetails($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->updateDistributorDetails: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the distributor |
 **request** | [**\Swagger\Client\Model\DistributorDetailsUpdateRequest**](../Model/DistributorDetailsUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\DistributorResponse**](../Model/DistributorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateDistributorLogo**
> updateDistributorLogo($id, $size)



Updates the specified distributor's logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DistributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The distributor UUID you are requesting data for.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->updateDistributorLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling DistributorsApi->updateDistributorLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The distributor UUID you are requesting data for. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

