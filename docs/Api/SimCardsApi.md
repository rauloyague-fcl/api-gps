# Swagger\Client\SimCardsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSimCard**](SimCardsApi.md#createSimCard) | **POST** /entities/simcards | 
[**getSimCard**](SimCardsApi.md#getSimCard) | **GET** /entities/simcards/{id} | 
[**listSimCards**](SimCardsApi.md#listSimCards) | **GET** /entities/simcards | 
[**updateSimCard**](SimCardsApi.md#updateSimCard) | **PUT** /entities/simcards/{id} | 


# **createSimCard**
> \Swagger\Client\Model\SimCardResponse createSimCard($request)



Creates a new SIM card

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SimCardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\SimCardCreateRequest(); // \Swagger\Client\Model\SimCardCreateRequest | 

try {
    $result = $apiInstance->createSimCard($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SimCardsApi->createSimCard: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\SimCardCreateRequest**](../Model/SimCardCreateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SimCardResponse**](../Model/SimCardResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSimCard**
> \Swagger\Client\Model\SimCardResponse getSimCard($id)



Returns SIM card details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SimCardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the SIM card

try {
    $result = $apiInstance->getSimCard($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SimCardsApi->getSimCard: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the SIM card |

### Return type

[**\Swagger\Client\Model\SimCardResponse**](../Model/SimCardResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listSimCards**
> \Swagger\Client\Model\SimCardListResponse listSimCards($owner, $offset, $limit, $sort, $filter)



Retrieve a list of SIM cards for a specified owner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SimCardsApi(
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
    $result = $apiInstance->listSimCards($owner, $offset, $limit, $sort, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SimCardsApi->listSimCards: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\SimCardListResponse**](../Model/SimCardListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateSimCard**
> \Swagger\Client\Model\SimCardResponse updateSimCard($id, $request)



Updates an existing SIM card

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SimCardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$request = new \Swagger\Client\Model\SimCardUpdateRequest(); // \Swagger\Client\Model\SimCardUpdateRequest | 

try {
    $result = $apiInstance->updateSimCard($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SimCardsApi->updateSimCard: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **request** | [**\Swagger\Client\Model\SimCardUpdateRequest**](../Model/SimCardUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\SimCardResponse**](../Model/SimCardResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

