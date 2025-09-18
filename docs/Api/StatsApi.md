# Swagger\Client\StatsApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getOutputForEntity**](StatsApi.md#getOutputForEntity) | **POST** /stats/entity/{type}/{id}/{metric} | 


# **getOutputForEntity**
> \Swagger\Client\Model\CellSetResponse getOutputForEntity($type, $id, $metric, $options)



Retrieve data for a stats report.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$type = "type_example"; // string | 
$id = "id_example"; // string | The type of the entity. The UUID of the entity. The stats metric.
$metric = "metric_example"; // string | 
$options = new \Swagger\Client\Model\StatsEntityOutputOptions(); // \Swagger\Client\Model\StatsEntityOutputOptions | 

try {
    $result = $apiInstance->getOutputForEntity($type, $id, $metric, $options);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->getOutputForEntity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**|  |
 **id** | **string**| The type of the entity. The UUID of the entity. The stats metric. |
 **metric** | **string**|  |
 **options** | [**\Swagger\Client\Model\StatsEntityOutputOptions**](../Model/StatsEntityOutputOptions.md)|  |

### Return type

[**\Swagger\Client\Model\CellSetResponse**](../Model/CellSetResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

