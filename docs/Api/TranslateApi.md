# Swagger\Client\TranslateApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**exportLanguage**](TranslateApi.md#exportLanguage) | **GET** /translate/{language}/export | 


# **exportLanguage**
> \Swagger\Client\Model\Dictionary exportLanguage($language)



Exports the language strings for the specified language.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TranslateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$language = "language_example"; // string | The language code

try {
    $result = $apiInstance->exportLanguage($language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TranslateApi->exportLanguage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **language** | **string**| The language code |

### Return type

[**\Swagger\Client\Model\Dictionary**](../Model/Dictionary.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

