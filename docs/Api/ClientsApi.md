# Swagger\Client\ClientsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createClient**](ClientsApi.md#createClient) | **POST** /accounts/clients | 
[**deleteClientLogo**](ClientsApi.md#deleteClientLogo) | **DELETE** /accounts/clients/{id}/logo | 
[**getClient**](ClientsApi.md#getClient) | **GET** /accounts/clients/{id} | 
[**getClientByPin**](ClientsApi.md#getClientByPin) | **GET** /accounts/clients/pin/{pin} | 
[**getClientLogo**](ClientsApi.md#getClientLogo) | **GET** /accounts/clients/{id}/logo | 
[**listClients**](ClientsApi.md#listClients) | **GET** /accounts/clients | 
[**updateClient**](ClientsApi.md#updateClient) | **PUT** /accounts/clients/{id} | 
[**updateClientDetails**](ClientsApi.md#updateClientDetails) | **PUT** /accounts/clients/{id}/details | 
[**updateClientLogo**](ClientsApi.md#updateClientLogo) | **POST** /accounts/clients/{id}/logo | 


# **createClient**
> \Swagger\Client\Model\ClientResponse createClient($request)



Creates a new client entity.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\ClientCreateRequest(); // \Swagger\Client\Model\ClientCreateRequest | The `ClientCreateRequest` that contains the required properties for the new entity.

try {
    $result = $apiInstance->createClient($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->createClient: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\ClientCreateRequest**](../Model/ClientCreateRequest.md)| The &#x60;ClientCreateRequest&#x60; that contains the required properties for the new entity. |

### Return type

[**\Swagger\Client\Model\ClientResponse**](../Model/ClientResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteClientLogo**
> deleteClientLogo($id, $size)



Permanently deletes a custom client logo. The logo will revert to the client's parent logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The client UUID.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->deleteClientLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->deleteClientLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The client UUID. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getClient**
> \Swagger\Client\Model\ClientResponse getClient($id)



Returns client details for the specified UUID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the client.

try {
    $result = $apiInstance->getClient($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->getClient: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the client. |

### Return type

[**\Swagger\Client\Model\ClientResponse**](../Model/ClientResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getClientByPin**
> \Swagger\Client\Model\IdName getClientByPin($pin)



Returns the client ID and name for the specified PIN. PINs are generated by the system and can be retrieved via the `pin` property on the  `ClientResponse` object retrieved with `getClient`.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pin = "pin_example"; // string | The PIN code of the client.

try {
    $result = $apiInstance->getClientByPin($pin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->getClientByPin: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pin** | **string**| The PIN code of the client. |

### Return type

[**\Swagger\Client\Model\IdName**](../Model/IdName.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getClientLogo**
> string getClientLogo($id, $size)



Return the specified client's logo in binary format. Should the client not have a custom logo, the logo of the vendor will be supplied.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The client UUID you are requesting data for.
$size = "size_example"; // string | The size of the returned image. Can be either \"small\" or \"large\".

try {
    $result = $apiInstance->getClientLogo($id, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->getClientLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The client UUID you are requesting data for. |
 **size** | **string**| The size of the returned image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listClients**
> \Swagger\Client\Model\ClientListResponse listClients($owner, $offset, $limit, $sort, $filter, $counts)



Retrieve a list of clients for a specified vendor.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The UUID of the vendor you are requesting data for.
$offset = 1.2; // double | An offset into the result set, useful for pagination.
$limit = 1.2; // double | Limit the number of results to this value.
$sort = "sort_example"; // string | Sorting column or attribute name with an optional direction, e.g. `sort=name:desc`
$filter = "filter_example"; // string | A filter to apply to the data in RQL format.
$counts = "counts_example"; // string | A list of entity types to return counts for that belong to this client, comma delimited, i.e. `counts=asset,device,simcard`. Each additional entity affects the performance of the query and should be used sparingly.

try {
    $result = $apiInstance->listClients($owner, $offset, $limit, $sort, $filter, $counts);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->listClients: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The UUID of the vendor you are requesting data for. |
 **offset** | **double**| An offset into the result set, useful for pagination. | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]
 **sort** | **string**| Sorting column or attribute name with an optional direction, e.g. &#x60;sort&#x3D;name:desc&#x60; | [optional]
 **filter** | **string**| A filter to apply to the data in RQL format. | [optional]
 **counts** | **string**| A list of entity types to return counts for that belong to this client, comma delimited, i.e. &#x60;counts&#x3D;asset,device,simcard&#x60;. Each additional entity affects the performance of the query and should be used sparingly. | [optional]

### Return type

[**\Swagger\Client\Model\ClientListResponse**](../Model/ClientListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateClient**
> \Swagger\Client\Model\ClientResponse updateClient($id, $request)



Updates an existing client entity by patching the existing object with the properties supplied in the `ClientUpdateRequest`.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the client
$request = new \Swagger\Client\Model\ClientUpdateRequest(); // \Swagger\Client\Model\ClientUpdateRequest | The `ClientUpdateRequest` that contains only the properites that are to be changed on the entity.

try {
    $result = $apiInstance->updateClient($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->updateClient: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the client |
 **request** | [**\Swagger\Client\Model\ClientUpdateRequest**](../Model/ClientUpdateRequest.md)| The &#x60;ClientUpdateRequest&#x60; that contains only the properites that are to be changed on the entity. |

### Return type

[**\Swagger\Client\Model\ClientResponse**](../Model/ClientResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateClientDetails**
> \Swagger\Client\Model\ClientResponse updateClientDetails($id, $request)



Updates an existing client account details. Unlike updateClient, this route is available to client users.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the client
$request = new \Swagger\Client\Model\ClientDetailsUpdateRequest(); // \Swagger\Client\Model\ClientDetailsUpdateRequest | 

try {
    $result = $apiInstance->updateClientDetails($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->updateClientDetails: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the client |
 **request** | [**\Swagger\Client\Model\ClientDetailsUpdateRequest**](../Model/ClientDetailsUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\ClientResponse**](../Model/ClientResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateClientLogo**
> updateClientLogo($id, $size)



Updates the specified client's logo.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The client UUID you are requesting data for.
$size = "size_example"; // string | The size of the image. Can be either \"small\" or \"large\".

try {
    $apiInstance->updateClientLogo($id, $size);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->updateClientLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The client UUID you are requesting data for. |
 **size** | **string**| The size of the image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

