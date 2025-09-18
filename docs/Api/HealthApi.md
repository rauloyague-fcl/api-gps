# Swagger\Client\HealthApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getIssue**](HealthApi.md#getIssue) | **GET** /health/issues/{id} | 
[**listIssues**](HealthApi.md#listIssues) | **GET** /health/issues | 
[**updateIssue**](HealthApi.md#updateIssue) | **PUT** /health/issues/{id} | 


# **getIssue**
> \Swagger\Client\Model\HealthIssueResponse getIssue($id)



Returns a health issue for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the health issue

try {
    $result = $apiInstance->getIssue($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getIssue: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the health issue |

### Return type

[**\Swagger\Client\Model\HealthIssueResponse**](../Model/HealthIssueResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listIssues**
> \Swagger\Client\Model\HealthIssueListResponse listIssues($owner, $target_id, $resolved, $offset, $limit)



Retrieve a list of health issues.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = "owner_example"; // string | The owner id you are requesting data for
$target_id = "target_id_example"; // string | The id of the entity on which to filter issues for
$resolved = true; // bool | Filter issues by their resolved status
$offset = 1.2; // double | An offset into the result set, useful for pagination
$limit = 1.2; // double | Limit the number of results to this value.

try {
    $result = $apiInstance->listIssues($owner, $target_id, $resolved, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->listIssues: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| The owner id you are requesting data for | [optional]
 **target_id** | **string**| The id of the entity on which to filter issues for | [optional]
 **resolved** | **bool**| Filter issues by their resolved status | [optional]
 **offset** | **double**| An offset into the result set, useful for pagination | [optional]
 **limit** | **double**| Limit the number of results to this value. | [optional]

### Return type

[**\Swagger\Client\Model\HealthIssueListResponse**](../Model/HealthIssueListResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateIssue**
> \Swagger\Client\Model\HealthIssueResponse updateIssue($id, $request)



Update a health issue for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the health issue
$request = new \Swagger\Client\Model\HealthIssueUpdateRequest(); // \Swagger\Client\Model\HealthIssueUpdateRequest | 

try {
    $result = $apiInstance->updateIssue($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->updateIssue: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the health issue |
 **request** | [**\Swagger\Client\Model\HealthIssueUpdateRequest**](../Model/HealthIssueUpdateRequest.md)|  |

### Return type

[**\Swagger\Client\Model\HealthIssueResponse**](../Model/HealthIssueResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

