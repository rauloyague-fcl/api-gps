# Swagger\Client\VendorsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createVendor**](VendorsApi.md#createVendor) | **POST** /accounts/vendors | 
[**deleteVendorLogo**](VendorsApi.md#deleteVendorLogo) | **DELETE** /accounts/vendors/{id}/logo | 
[**getVendor**](VendorsApi.md#getVendor) | **GET** /accounts/vendors/{id} | 
[**getVendorLogo**](VendorsApi.md#getVendorLogo) | **GET** /accounts/vendors/{id}/logo | 
[**listVendors**](VendorsApi.md#listVendors) | **GET** /accounts/vendors | 
[**updateVendor**](VendorsApi.md#updateVendor) | **PUT** /accounts/vendors/{id} | 
[**updateVendorDetails**](VendorsApi.md#updateVendorDetails) | **PUT** /accounts/vendors/{id}/details | 
[**updateVendorLogo**](VendorsApi.md#updateVendorLogo) | **POST** /accounts/vendors/{id}/logo | 


# **createVendor**
> \Swagger\Client\Model\VendorResponse createVendor($request)



Creates a new vendor account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\VendorCreateRequest(); // \Swagger\Client\Model\VendorCreateRequest | 

try {
    $result = $apiInstance->createVendor($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->createVendor: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\VendorCreateRequest**](../Model/VendorCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\VendorResponse**](../Model/VendorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteVendorLogo**
> deleteVendorLogo($id, $size)



Permanently deletes a custom vendor logo. The logo will revert to the vendor's parent logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The vendor UUID.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->deleteVendorLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->deleteVendorLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The vendor UUID. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getVendor**
> \Swagger\Client\Model\VendorResponse getVendor($id)



Returns vendor details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the vendor

try {
    $result = $apiInstance->getVendor($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->getVendor: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the vendor |

### Return type

[**\Swagger\Client\Model\VendorResponse**](../Model/VendorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getVendorLogo**
> string getVendorLogo($id, $size)



Return the specified vendor's logo in binary format. Should the vendor not have a custom logo, the logo of the distributor will be supplied.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\VendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The vendor UUID you are requesting data for.
$size = "size_example"; // string | The size of the returned image. Can be either \"small\" or \"large\".

try {
    $result = $apiInstance->getVendorLogo($id, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->getVendorLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The vendor UUID you are requesting data for. |
 **size** | **string**| The size of the returned image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listVendors**
> \Swagger\Client\Model\VendorListResponse listVendors($owner, $offset, $limit, $sort, $filter, $counts)



Retrieve a list of vendors for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VendorsApi(
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
$counts = "counts_example"; // string | A list of entity types to return counts for that belong to this vendor, comma delimited, i.e. `counts=client,asset,device`. Each additional entity affects the performance of the query and should be used sparingly.

try {
    $result = $apiInstance->listVendors($owner, $offset, $limit, $sort, $filter, $counts);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->listVendors: ', $e->getMessage(), PHP_EOL;
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
 **counts** | **string**| A list of entity types to return counts for that belong to this vendor, comma delimited, i.e. &#x60;counts&#x3D;client,asset,device&#x60;. Each additional entity affects the performance of the query and should be used sparingly. | [optional]

### Return type

[**\Swagger\Client\Model\VendorListResponse**](../Model/VendorListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateVendor**
> \Swagger\Client\Model\VendorResponse updateVendor($id, $request)



Updates an existing vendor account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the vendor
$request = new \Swagger\Client\Model\VendorUpdateRequest(); // \Swagger\Client\Model\VendorUpdateRequest | 

try {
    $result = $apiInstance->updateVendor($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->updateVendor: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the vendor |
 **request** | [**\Swagger\Client\Model\VendorUpdateRequest**](../Model/VendorUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\VendorResponse**](../Model/VendorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateVendorDetails**
> \Swagger\Client\Model\VendorResponse updateVendorDetails($id, $request)



Updates an existing vendor account details. Unlike updateVendor, this route is available to vendor users.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the vendor
$request = new \Swagger\Client\Model\VendorDetailsUpdateRequest(); // \Swagger\Client\Model\VendorDetailsUpdateRequest | 

try {
    $result = $apiInstance->updateVendorDetails($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->updateVendorDetails: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the vendor |
 **request** | [**\Swagger\Client\Model\VendorDetailsUpdateRequest**](../Model/VendorDetailsUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\VendorResponse**](../Model/VendorResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateVendorLogo**
> updateVendorLogo($id, $size)



Updates the specified vendor's logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The vendor UUID you are requesting data for.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->updateVendorLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling VendorsApi->updateVendorLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The vendor UUID you are requesting data for. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

