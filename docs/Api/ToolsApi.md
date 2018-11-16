# Swagger\Client\ToolsApi

All URIs are relative to *https://portal.cbrain.mcgill.ca*

Method | HTTP request | Description
------------- | ------------- | -------------
[**toolsGet**](ToolsApi.md#toolsGet) | **GET** /tools | Get the list of Tools.


# **toolsGet**
> \Swagger\Client\Model\Tool[] toolsGet()

Get the list of Tools.

This method returns a list of all of the Tools that exist in CBRAIN. Tools encapsulate a scientific program designed to extract information from an input Userfile.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ToolsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->toolsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ToolsApi->toolsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Tool[]**](../Model/Tool.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

