# Swagger\Client\UserfilesApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**userfilesChangeProviderPost**](UserfilesApi.md#userfilesChangeProviderPost) | **POST** /userfiles/change_provider | Moves the Userfiles from their current Data Provider to a new one.
[**userfilesCompressPost**](UserfilesApi.md#userfilesCompressPost) | **POST** /userfiles/compress | Compresses many Userfiles each into their own GZIP archive.
[**userfilesDeleteFilesDelete**](UserfilesApi.md#userfilesDeleteFilesDelete) | **DELETE** /userfiles/delete_files | Delete several files that have been registered as Userfiles
[**userfilesDownloadPost**](UserfilesApi.md#userfilesDownloadPost) | **POST** /userfiles/download | Download several files
[**userfilesGet**](UserfilesApi.md#userfilesGet) | **GET** /userfiles | List of the Userfiles accessible to the current user.
[**userfilesIdContentGet**](UserfilesApi.md#userfilesIdContentGet) | **GET** /userfiles/{id}/content | Get the content of a Userfile
[**userfilesIdGet**](UserfilesApi.md#userfilesIdGet) | **GET** /userfiles/{id} | Get information on a Userfile.
[**userfilesIdPut**](UserfilesApi.md#userfilesIdPut) | **PUT** /userfiles/{id} | Update information on a Userfile.
[**userfilesPost**](UserfilesApi.md#userfilesPost) | **POST** /userfiles | Creates a new Userfile and upload its content.
[**userfilesSyncMultiplePost**](UserfilesApi.md#userfilesSyncMultiplePost) | **POST** /userfiles/sync_multiple | Syncs Userfiles to the local Data Providers cache.
[**userfilesUncompressPost**](UserfilesApi.md#userfilesUncompressPost) | **POST** /userfiles/uncompress | Uncompresses many Userfiles.


# **userfilesChangeProviderPost**
> userfilesChangeProviderPost($multi_userfile_mod_req)

Moves the Userfiles from their current Data Provider to a new one.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$multi_userfile_mod_req = new \Swagger\Client\Model\MultiUserfilesModReq(); // \Swagger\Client\Model\MultiUserfilesModReq | The IDs of the files to move.

try {
    $apiInstance->userfilesChangeProviderPost($multi_userfile_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesChangeProviderPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_userfile_mod_req** | [**\Swagger\Client\Model\MultiUserfilesModReq**](../Model/MultiUserfilesModReq.md)| The IDs of the files to move. |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesCompressPost**
> userfilesCompressPost($multi_userfile_mod_req)

Compresses many Userfiles each into their own GZIP archive.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$multi_userfile_mod_req = new \Swagger\Client\Model\MultiUserfilesModReq(); // \Swagger\Client\Model\MultiUserfilesModReq | The IDs of the files to compress.

try {
    $apiInstance->userfilesCompressPost($multi_userfile_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesCompressPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_userfile_mod_req** | [**\Swagger\Client\Model\MultiUserfilesModReq**](../Model/MultiUserfilesModReq.md)| The IDs of the files to compress. |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesDeleteFilesDelete**
> userfilesDeleteFilesDelete($multi_userfile_mod_req)

Delete several files that have been registered as Userfiles

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$multi_userfile_mod_req = new \Swagger\Client\Model\MultiUserfilesModReq(); // \Swagger\Client\Model\MultiUserfilesModReq | The IDs of the files to destroy.

try {
    $apiInstance->userfilesDeleteFilesDelete($multi_userfile_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesDeleteFilesDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_userfile_mod_req** | [**\Swagger\Client\Model\MultiUserfilesModReq**](../Model/MultiUserfilesModReq.md)| The IDs of the files to destroy. |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesDownloadPost**
> userfilesDownloadPost($multi_userfile_mod_req)

Download several files

This method compresses several Userfiles in .gz format and prepares them to be downloaded.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$multi_userfile_mod_req = new \Swagger\Client\Model\MultiUserfilesModReq(); // \Swagger\Client\Model\MultiUserfilesModReq | The IDs of the files to be downloaded. If more than one file is specified, they will be zipped into a gzip archive.

try {
    $apiInstance->userfilesDownloadPost($multi_userfile_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesDownloadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_userfile_mod_req** | [**\Swagger\Client\Model\MultiUserfilesModReq**](../Model/MultiUserfilesModReq.md)| The IDs of the files to be downloaded. If more than one file is specified, they will be zipped into a gzip archive. |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesGet**
> \Swagger\Client\Model\Userfile[] userfilesGet()

List of the Userfiles accessible to the current user.

This method returns a list of Userfiles that are available to the current User.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->userfilesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Userfile[]**](../Model/Userfile.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesIdContentGet**
> string userfilesIdContentGet($id)

Get the content of a Userfile

This method allows you to download the content of a userfile.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID number of the Userfile to download

try {
    $result = $apiInstance->userfilesIdContentGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesIdContentGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Userfile to download |

### Return type

**string**

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesIdGet**
> \Swagger\Client\Model\Userfile userfilesIdGet($id)

Get information on a Userfile.

This method returns information about a single Userfile, specified by its ID. Information returned includes the ID of the owner, the Group (project) it is a part of, a description, information about where the acutal copy of the file currently is, and what the status is of any synhronization operations that may have been requested.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID number of the Userfile to get information on.

try {
    $result = $apiInstance->userfilesIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Userfile to get information on. |

### Return type

[**\Swagger\Client\Model\Userfile**](../Model/Userfile.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesIdPut**
> userfilesIdPut($id, $userfile_mod_req)

Update information on a Userfile.

This method allows a User to update information on a userfile.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | The ID number of the Userfile to update.
$userfile_mod_req = new \Swagger\Client\Model\UserfileModReq(); // \Swagger\Client\Model\UserfileModReq | 

try {
    $apiInstance->userfilesIdPut($id, $userfile_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Userfile to update. |
 **userfile_mod_req** | [**\Swagger\Client\Model\UserfileModReq**](../Model/UserfileModReq.md)|  |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesPost**
> object userfilesPost($upload_file, $data_provider_id, $userfile_group_id, $file_type, $_do_extract, $_up_ex_mode)

Creates a new Userfile and upload its content.

This method creates a new Userfile in CBRAIN, with the current user as the owner of the file.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$upload_file = "/path/to/file.txt"; // \SplFileObject | File content to upload to CBRAIN
$data_provider_id = 56; // int | The ID of the Data Provider to upload the file to.
$userfile_group_id = 56; // int | ID of the group that will have access to the Userfile
$file_type = "SingleFile"; // string | The type of the file
$_do_extract = "_do_extract_example"; // string | set to the string 'on' to indicate that the uploaded content is a tar.gz or .zip archive that need to be extracted. See also the parameter _up_ex_mode
$_up_ex_mode = "_up_ex_mode_example"; // string | if '_do_extract' is set to 'on', set this to 'collection' to create a single collection, or 'multiple' to create one file per entry in the uploaded content

try {
    $result = $apiInstance->userfilesPost($upload_file, $data_provider_id, $userfile_group_id, $file_type, $_do_extract, $_up_ex_mode);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **upload_file** | **\SplFileObject**| File content to upload to CBRAIN |
 **data_provider_id** | **int**| The ID of the Data Provider to upload the file to. |
 **userfile_group_id** | **int**| ID of the group that will have access to the Userfile |
 **file_type** | **string**| The type of the file | [default to SingleFile]
 **_do_extract** | **string**| set to the string &#39;on&#39; to indicate that the uploaded content is a tar.gz or .zip archive that need to be extracted. See also the parameter _up_ex_mode | [optional]
 **_up_ex_mode** | **string**| if &#39;_do_extract&#39; is set to &#39;on&#39;, set this to &#39;collection&#39; to create a single collection, or &#39;multiple&#39; to create one file per entry in the uploaded content | [optional]

### Return type

**object**

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesSyncMultiplePost**
> userfilesSyncMultiplePost($multi_userfile_mod_req)

Syncs Userfiles to the local Data Providers cache.

Synchronizing files to their the local cache allows you to download, visualize and do processing on them that is not available if not synced. CBRAIN operations will sync files automatically, and this is only necessary if a file is changed on its host Data Provdier by an external process.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$multi_userfile_mod_req = new \Swagger\Client\Model\MultiUserfilesModReq(); // \Swagger\Client\Model\MultiUserfilesModReq | The IDs of the files to synchronize.

try {
    $apiInstance->userfilesSyncMultiplePost($multi_userfile_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesSyncMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_userfile_mod_req** | [**\Swagger\Client\Model\MultiUserfilesModReq**](../Model/MultiUserfilesModReq.md)| The IDs of the files to synchronize. |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesUncompressPost**
> userfilesUncompressPost($multi_userfile_mod_req)

Uncompresses many Userfiles.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$multi_userfile_mod_req = new \Swagger\Client\Model\MultiUserfilesModReq(); // \Swagger\Client\Model\MultiUserfilesModReq | The IDs of the files to uncompress.

try {
    $apiInstance->userfilesUncompressPost($multi_userfile_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesUncompressPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_userfile_mod_req** | [**\Swagger\Client\Model\MultiUserfilesModReq**](../Model/MultiUserfilesModReq.md)| The IDs of the files to uncompress. |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

