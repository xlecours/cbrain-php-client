# Swagger\Client\BourreauxApi

All URIs are relative to *https://portal.cbrain.mcgill.ca*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bourreauxGet**](BourreauxApi.md#bourreauxGet) | **GET** /bourreaux | Get a list of the Bourreaux available to be used by the current user.
[**bourreauxIdGet**](BourreauxApi.md#bourreauxIdGet) | **GET** /bourreaux/{id} | Get information about a Bourreau.


# **bourreauxGet**
> \Swagger\Client\Model\Bourreau[] bourreauxGet()

Get a list of the Bourreaux available to be used by the current user.

This method returns a list of Bourreau objects.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\BourreauxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->bourreauxGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BourreauxApi->bourreauxGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Bourreau[]**](../Model/Bourreau.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **bourreauxIdGet**
> \Swagger\Client\Model\Bourreau bourreauxIdGet($id)

Get information about a Bourreau.

This method returns a single Bourreau object based on the ID parameter.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\BourreauxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | ID of the Bourreau to get information on.

try {
    $result = $apiInstance->bourreauxIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BourreauxApi->bourreauxIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the Bourreau to get information on. |

### Return type

[**\Swagger\Client\Model\Bourreau**](../Model/Bourreau.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

