# Swagger\Client\CompaniesApi

All URIs are relative to *https://localhost/fleet/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCompany**](CompaniesApi.md#getCompany) | **GET** /accounts/companies/{id} | 
[**getCompanyLogo**](CompaniesApi.md#getCompanyLogo) | **GET** /accounts/companies/{id}/logo | 


# **getCompany**
> \Swagger\Client\Model\CompanyResponse getCompany($id)



Returns company details for the specified id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('x-access-token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-access-token', 'Bearer');

$apiInstance = new Swagger\Client\Api\CompaniesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The UUID of the client

try {
    $result = $apiInstance->getCompany($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompaniesApi->getCompany: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The UUID of the client |

### Return type

[**\Swagger\Client\Model\CompanyResponse**](../Model/CompanyResponse.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCompanyLogo**
> string getCompanyLogo($id, $size, $recurse)



Return the specified company's logo in binary format.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CompaniesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | The client UUID you are requesting data for.
$size = "size_example"; // string | The size of the returned image. Can be either \"small\" or \"large\".
$recurse = true; // bool | Set recurse to true if you'd like the parent tree to be searched for a logo if none exists for this company.

try {
    $result = $apiInstance->getCompanyLogo($id, $size, $recurse);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompaniesApi->getCompanyLogo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The client UUID you are requesting data for. |
 **size** | **string**| The size of the returned image. Can be either \&quot;small\&quot; or \&quot;large\&quot;. |
 **recurse** | **bool**| Set recurse to true if you&#39;d like the parent tree to be searched for a logo if none exists for this company. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

