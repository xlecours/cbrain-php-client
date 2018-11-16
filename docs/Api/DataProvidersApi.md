# Swagger\Client\DataProvidersApi

All URIs are relative to *https://portal.cbrain.mcgill.ca*

Method | HTTP request | Description
------------- | ------------- | -------------
[**dataProvidersGet**](DataProvidersApi.md#dataProvidersGet) | **GET** /data_providers | Get a list of the Data Providers available to the current user.
[**dataProvidersIdBrowseGet**](DataProvidersApi.md#dataProvidersIdBrowseGet) | **GET** /data_providers/{id}/browse | List the files on a Data Provider.
[**dataProvidersIdDeletePost**](DataProvidersApi.md#dataProvidersIdDeletePost) | **POST** /data_providers/{id}/delete | Deletes unregistered files from a CBRAIN Data provider.
[**dataProvidersIdGet**](DataProvidersApi.md#dataProvidersIdGet) | **GET** /data_providers/{id} | Get information on a particular Data Provider.
[**dataProvidersIdIsAliveGet**](DataProvidersApi.md#dataProvidersIdIsAliveGet) | **GET** /data_providers/{id}/is_alive | Pings a Data Provider to check if it is running.
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

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
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

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdDeletePost**
> \Swagger\Client\Model\RegistrationInfo dataProvidersIdDeletePost($id, $multi_registration_mod_req)

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
$multi_registration_mod_req = new \Swagger\Client\Model\MultiRegistrationModReq(); // \Swagger\Client\Model\MultiRegistrationModReq | Arrays containing the files to delete.

try {
    $result = $apiInstance->dataProvidersIdDeletePost($id, $multi_registration_mod_req);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdDeletePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID of the Data Provider to delete files from. |
 **multi_registration_mod_req** | [**\Swagger\Client\Model\MultiRegistrationModReq**](../Model/MultiRegistrationModReq.md)| Arrays containing the files to delete. |

### Return type

[**\Swagger\Client\Model\RegistrationInfo**](../Model/RegistrationInfo.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json
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

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdIsAliveGet**
> string dataProvidersIdIsAliveGet($id)

Pings a Data Provider to check if it is running.

This method allows the querying of a Data Provider specified by the ID parameter to see if it is running or not.

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

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdRegisterPost**
> \Swagger\Client\Model\RegistrationInfo dataProvidersIdRegisterPost($id, $multi_registration_mod_req)

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
$multi_registration_mod_req = new \Swagger\Client\Model\MultiRegistrationModReq(); // \Swagger\Client\Model\MultiRegistrationModReq | Arrays containing the filenames and types to register.

try {
    $result = $apiInstance->dataProvidersIdRegisterPost($id, $multi_registration_mod_req);
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
 **multi_registration_mod_req** | [**\Swagger\Client\Model\MultiRegistrationModReq**](../Model/MultiRegistrationModReq.md)| Arrays containing the filenames and types to register. |

### Return type

[**\Swagger\Client\Model\RegistrationInfo**](../Model/RegistrationInfo.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dataProvidersIdUnregisterPost**
> \Swagger\Client\Model\RegistrationInfo dataProvidersIdUnregisterPost($id, $multi_registration_mod_req)

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
$multi_registration_mod_req = new \Swagger\Client\Model\MultiRegistrationModReq(); // \Swagger\Client\Model\MultiRegistrationModReq | Arrays containing the filenames to unregister.

try {
    $result = $apiInstance->dataProvidersIdUnregisterPost($id, $multi_registration_mod_req);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataProvidersApi->dataProvidersIdUnregisterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID of the Data Provider to unregister files from. |
 **multi_registration_mod_req** | [**\Swagger\Client\Model\MultiRegistrationModReq**](../Model/MultiRegistrationModReq.md)| Arrays containing the filenames to unregister. |

### Return type

[**\Swagger\Client\Model\RegistrationInfo**](../Model/RegistrationInfo.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

