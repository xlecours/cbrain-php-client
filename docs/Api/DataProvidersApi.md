# Swagger\Client\DataProvidersApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**dataProvidersGet**](DataProvidersApi.md#dataProvidersGet) | **GET** /data_providers | Get a list of the Data Providers available to the current user.
[**dataProvidersIdBrowseGet**](DataProvidersApi.md#dataProvidersIdBrowseGet) | **GET** /data_providers/{id}/browse | List the files on a Data Provider.
[**dataProvidersIdDeletePost**](DataProvidersApi.md#dataProvidersIdDeletePost) | **POST** /data_providers/{id}/delete | Deletes unregistered files from a CBRAIN Data provider.
[**dataProvidersIdGet**](DataProvidersApi.md#dataProvidersIdGet) | **GET** /data_providers/{id} | Get information on a particular Data Provider.
[**dataProvidersIdIsAliveGet**](DataProvidersApi.md#dataProvidersIdIsAliveGet) | **GET** /data_providers/{id}/is_alive | Pings a Data Provider to check if it&#39;s running.
[**dataProvidersIdRegisterPost**](DataProvidersApi.md#dataProvidersIdRegisterPost) | **POST** /data_providers/{id}/register | Registers a file as a Userfile in CBRAIN.
[**dataProvidersIdUnregisterPost**](DataProvidersApi.md#dataProvidersIdUnregisterPost) | **POST** /data_providers/{id}/unregister | Unregisters files as Userfile in CBRAIN.


# **dataProvidersGet**
> \Swagger\Client\Model\DataProvider[] dataProvidersGet()

Get a list of the Data Providers available to the current user.

This method returns a list of Data Provider objects that represent servers with disk space accessible for storing Userfiles.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->dataProvidersGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\DataProvider[]**](../Model/DataProvider.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdBrowseGet**
> \Swagger\Client\Model\FileInfo[] dataProvidersIdBrowseGet($id)

List the files on a Data Provider.

This method allows the inspection of what files are present on a Data Provider specified by the ID parameter. Files that are not yet registered as Userfiles are visible using this method, as well as regularly accessible Userfiles.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the Data Provider to browse.

try {
    $result = $apiInstance->dataProvidersIdBrowseGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdBrowseGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID of the Data Provider to browse. |

### Return type

[**\Swagger\Client\Model\FileInfo[]**](../Model/FileInfo.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdDeletePost**
> dataProvidersIdDeletePost($id, $basenames, $authenticity_token, $as_user_id)

Deletes unregistered files from a CBRAIN Data provider.

This method allows files that have not been registered from CBRAIN to be deleted. This may be necessary if files were uploaded in error, or if they were unregistered but not immediately deleted.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the Data Provider to delete files from.
$basenames = array("basenames_example"); // string[] | An array containing the filenames to delete.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$as_user_id = 56; // int | The ID of the user to delete files as.

try {
    $apiInstance->dataProvidersIdDeletePost($id, $basenames, $authenticity_token, $as_user_id);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdDeletePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID of the Data Provider to delete files from. |
 **basenames** | [**string[]**](../Model/string.md)| An array containing the filenames to delete. |
 **authenticity_token** | **string**| The token returned by /session/new |
 **as_user_id** | **int**| The ID of the user to delete files as. | [optional]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdGet**
> \Swagger\Client\Model\DataProvider dataProvidersIdGet($id)

Get information on a particular Data Provider.

This method returns a single Data Provider specified by the ID parameter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | ID of the Data Provider to get information on.

try {
    $result = $apiInstance->dataProvidersIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the Data Provider to get information on. |

### Return type

[**\Swagger\Client\Model\DataProvider**](../Model/DataProvider.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdIsAliveGet**
> string dataProvidersIdIsAliveGet($id)

Pings a Data Provider to check if it's running.

This method allows the querying of a Data Provider specified by the ID parameter to see if it's running or not.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | The ID of the Data Provider to query.

try {
    $result = $apiInstance->dataProvidersIdIsAliveGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdIsAliveGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID of the Data Provider to query. |

### Return type

**string**

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdRegisterPost**
> \Swagger\Client\Model\InlineResponse2005 dataProvidersIdRegisterPost($id, $basenames, $filetypes, $authenticity_token)

Registers a file as a Userfile in CBRAIN.

This method allows new files to be added to CBRAIN. The files must first be transfered to the Data Provider via SFTP. For more information on SFTP file transfers, consult the CBRAIN Wiki documentation. Once files are present on the Data Provider, this method registers them in CBRAIN by specifying the file type. You can also specify to copy/move the files to another Data Provider after file registration.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the Data Provider to register files on.
$basenames = array("basenames_example"); // string[] | An array containing the filenames to register.
$filetypes = array("filetypes_example"); // string[] | An array containing the filetypes associated with the files to register
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new

try {
    $result = $apiInstance->dataProvidersIdRegisterPost($id, $basenames, $filetypes, $authenticity_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdRegisterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID of the Data Provider to register files on. |
 **basenames** | [**string[]**](../Model/string.md)| An array containing the filenames to register. |
 **filetypes** | [**string[]**](../Model/string.md)| An array containing the filetypes associated with the files to register |
 **authenticity_token** | **string**| The token returned by /session/new |

### Return type

[**\Swagger\Client\Model\InlineResponse2005**](../Model/InlineResponse2005.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdUnregisterPost**
> dataProvidersIdUnregisterPost($id, $basenames, $authenticity_token, $as_user_id, $delete)

Unregisters files as Userfile in CBRAIN.

This method allows files to be unregistered from CBRAIN. This will not delete the files, but removes them from the CBRAIN database, so Tools may no longer be run on them.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DataProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the Data Provider to unregister files from.
$basenames = array("basenames_example"); // string[] | An array containing the filenames to unregister.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$as_user_id = 56; // int | The ID of the user to unregister files as.
$delete = true; // bool | Specifies to delete the files once they are unregistered.

try {
    $apiInstance->dataProvidersIdUnregisterPost($id, $basenames, $authenticity_token, $as_user_id, $delete);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdUnregisterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID of the Data Provider to unregister files from. |
 **basenames** | [**string[]**](../Model/string.md)| An array containing the filenames to unregister. |
 **authenticity_token** | **string**| The token returned by /session/new |
 **as_user_id** | **int**| The ID of the user to unregister files as. | [optional]
 **delete** | **bool**| Specifies to delete the files once they are unregistered. | [optional] [default to true]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

