# Swagger\Client\SearchApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchEntities**](SearchApi.md#searchEntities) | **GET** /search/entities | 


# **searchEntities**
> \Swagger\Client\Model\EntitySearchResponse searchEntities($query, $deleted)



Perform a free text search against the entities available to the user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = "query_example"; // string | The free text query you'd like to search for
$deleted = true; // bool | Specify whether to include deleted items in the response

try {
    $result = $apiInstance->searchEntities($query, $deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchEntities: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string**| The free text query you&#39;d like to search for |
 **deleted** | **bool**| Specify whether to include deleted items in the response | [optional]

### Return type

[**\Swagger\Client\Model\EntitySearchResponse**](../Model/EntitySearchResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

