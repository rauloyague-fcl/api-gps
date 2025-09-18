# Swagger\Client\SslCertificatesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSslCertificate**](SslCertificatesApi.md#createSslCertificate) | **POST** /entities/sslcertificates | 
[**getSslCertificate**](SslCertificatesApi.md#getSslCertificate) | **GET** /entities/sslcertificates/{id} | 
[**listSslCertificates**](SslCertificatesApi.md#listSslCertificates) | **GET** /entities/sslcertificates | 
[**provisionSslCertificate**](SslCertificatesApi.md#provisionSslCertificate) | **POST** /entities/sslcertificates/{id}/provision | 
[**updateSslCertificate**](SslCertificatesApi.md#updateSslCertificate) | **PUT** /entities/sslcertificates/{id} | 
[**validateSslCertificate**](SslCertificatesApi.md#validateSslCertificate) | **POST** /entities/sslcertificates/{id}/validate | 


# **createSslCertificate**
> \Swagger\Client\Model\SslCertificateResponse createSslCertificate($request)



Creates a new ssl certificate entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SslCertificatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\SslCertificateCreateRequest(); // \Swagger\Client\Model\SslCertificateCreateRequest | 

try {
    $result = $apiInstance->createSslCertificate($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SslCertificatesApi->createSslCertificate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\SslCertificateCreateRequest**](../Model/SslCertificateCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SslCertificateResponse**](../Model/SslCertificateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSslCertificate**
> \Swagger\Client\Model\SslCertificateResponse getSslCertificate($id)



Returns ssl certificate details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SslCertificatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the ssl certificate

try {
    $result = $apiInstance->getSslCertificate($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SslCertificatesApi->getSslCertificate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the ssl certificate |

### Return type

[**\Swagger\Client\Model\SslCertificateResponse**](../Model/SslCertificateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listSslCertificates**
> \Swagger\Client\Model\SslCertificateListResponse listSslCertificates($owner, $offset, $limit, $sort, $filter)



Retrieve a list of ssl certificates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SslCertificatesApi(
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
    $result = $apiInstance->listSslCertificates($owner, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SslCertificatesApi->listSslCertificates: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\SslCertificateListResponse**](../Model/SslCertificateListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **provisionSslCertificate**
> \Swagger\Client\Model\SslCertificateProvisionResponse provisionSslCertificate($id)



Attempts to provision the ssl certificate

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SslCertificatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the ssl certificate

try {
    $result = $apiInstance->provisionSslCertificate($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SslCertificatesApi->provisionSslCertificate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the ssl certificate |

### Return type

[**\Swagger\Client\Model\SslCertificateProvisionResponse**](../Model/SslCertificateProvisionResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateSslCertificate**
> \Swagger\Client\Model\SslCertificateResponse updateSslCertificate($id, $request)



Updates an existing ssl certificate entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SslCertificatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the ssl certificate
$request = new \Swagger\Client\Model\SslCertificateUpdateRequest(); // \Swagger\Client\Model\SslCertificateUpdateRequest | 

try {
    $result = $apiInstance->updateSslCertificate($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SslCertificatesApi->updateSslCertificate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the ssl certificate |
 **request** | [**\Swagger\Client\Model\SslCertificateUpdateRequest**](../Model/SslCertificateUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SslCertificateResponse**](../Model/SslCertificateResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **validateSslCertificate**
> \Swagger\Client\Model\SslCertificateValidationResponse validateSslCertificate($id)



Validates the ssl certificate and all prerequisites

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SslCertificatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the ssl certificate

try {
    $result = $apiInstance->validateSslCertificate($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SslCertificatesApi->validateSslCertificate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the ssl certificate |

### Return type

[**\Swagger\Client\Model\SslCertificateValidationResponse**](../Model/SslCertificateValidationResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

