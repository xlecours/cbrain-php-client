# Swagger\Client\UserfilesApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**userfilesChangeProviderPost**](UserfilesApi.md#userfilesChangeProviderPost) | **POST** /userfiles/change_provider | Moves the Userfiles from their current Data Provider to a new one.
[**userfilesCompressPost**](UserfilesApi.md#userfilesCompressPost) | **POST** /userfiles/compress | Compresses many Userfiles each into their own GZIP archive.
[**userfilesDeleteFilesPost**](UserfilesApi.md#userfilesDeleteFilesPost) | **POST** /userfiles/delete_files | Delete several files that have been registered as Userfiles
[**userfilesDownloadPost**](UserfilesApi.md#userfilesDownloadPost) | **POST** /userfiles/download | Download several files
[**userfilesGet**](UserfilesApi.md#userfilesGet) | **GET** /userfiles | List of the Userfiles accessible to the current user.
[**userfilesIdContentGet**](UserfilesApi.md#userfilesIdContentGet) | **GET** /userfiles/{id}/content | Get the content of a Userfile
[**userfilesIdDelete**](UserfilesApi.md#userfilesIdDelete) | **DELETE** /userfiles/{id} | Delete a Userfile.
[**userfilesIdGet**](UserfilesApi.md#userfilesIdGet) | **GET** /userfiles/{id} | Get information on a Userfile.
[**userfilesIdPut**](UserfilesApi.md#userfilesIdPut) | **PUT** /userfiles/{id} | Update information on a Userfile.
[**userfilesPost**](UserfilesApi.md#userfilesPost) | **POST** /userfiles | Creates a new Userfile.
[**userfilesSyncMultiplePost**](UserfilesApi.md#userfilesSyncMultiplePost) | **POST** /userfiles/sync_multiple | Syncs Userfiles to their Data Providers&#39; cache.
[**userfilesUncompressPost**](UserfilesApi.md#userfilesUncompressPost) | **POST** /userfiles/uncompress | Uncompresses many Userfiles.


# **userfilesChangeProviderPost**
> userfilesChangeProviderPost($file_ids, $data_provider_id_for_mv_cp, $authenticity_token, $crush_destination)

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
$file_ids = array(56); // int[] | The ID's of the Userfiles to be moved or copied to a new Data Provider.
$data_provider_id_for_mv_cp = 56; // int | The ID of the Data Provider to move or copy the files to.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$crush_destination = false; // bool | Specifies whether to overwrite files on the destination Data Provider if a file already exists there with the same name

try {
    $apiInstance->userfilesChangeProviderPost($file_ids, $data_provider_id_for_mv_cp, $authenticity_token, $crush_destination);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesChangeProviderPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_ids** | [**int[]**](../Model/int.md)| The ID&#39;s of the Userfiles to be moved or copied to a new Data Provider. |
 **data_provider_id_for_mv_cp** | **int**| The ID of the Data Provider to move or copy the files to. |
 **authenticity_token** | **string**| The token returned by /session/new |
 **crush_destination** | **bool**| Specifies whether to overwrite files on the destination Data Provider if a file already exists there with the same name | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesCompressPost**
> userfilesCompressPost($file_ids, $authenticity_token)

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
$file_ids = array(56); // int[] | A list of Userfile ID numbers to compress.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new

try {
    $apiInstance->userfilesCompressPost($file_ids, $authenticity_token);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesCompressPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_ids** | [**int[]**](../Model/int.md)| A list of Userfile ID numbers to compress. |
 **authenticity_token** | **string**| The token returned by /session/new |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesDeleteFilesPost**
> userfilesDeleteFilesPost($file_ids, $authenticity_token)

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
$file_ids = array(56); // int[] | The ID numbers of the files to be deleted
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new

try {
    $apiInstance->userfilesDeleteFilesPost($file_ids, $authenticity_token);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesDeleteFilesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_ids** | [**int[]**](../Model/int.md)| The ID numbers of the files to be deleted |
 **authenticity_token** | **string**| The token returned by /session/new |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesDownloadPost**
> userfilesDownloadPost($authenticity_token, $file_ids, $specified_filename)

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
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$file_ids = array(56); // int[] | The ID numbers of the files to be downloaded. If more than one file is specified, they will be zipped into a gzip archive.
$specified_filename = "specified_filename_example"; // string | The name of the archive file that the Userfiles will be compressed into for downloading.

try {
    $apiInstance->userfilesDownloadPost($authenticity_token, $file_ids, $specified_filename);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesDownloadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authenticity_token** | **string**| The token returned by /session/new |
 **file_ids** | [**int[]**](../Model/int.md)| The ID numbers of the files to be downloaded. If more than one file is specified, they will be zipped into a gzip archive. | [optional]
 **specified_filename** | **string**| The name of the archive file that the Userfiles will be compressed into for downloading. | [optional]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
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

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesIdContentGet**
> userfilesIdContentGet($id)

Get the content of a Userfile

This method allows you to download Userfiles.

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
    $apiInstance->userfilesIdContentGet($id);
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

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesIdDelete**
> userfilesIdDelete($id, $authenticity_token)

Delete a Userfile.

This method allows a User to delete a Userfile.

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
$id = 56; // int | The ID number of the Userfile to delete.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new

try {
    $apiInstance->userfilesIdDelete($id, $authenticity_token);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Userfile to delete. |
 **authenticity_token** | **string**| The token returned by /session/new |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
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

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesIdPut**
> userfilesIdPut($id, $authenticity_token, $userfile_type, $userfile_user_id, $userfile_group_id, $tag_ids, $userfile_group_writable, $userfile_hidden, $userfile_immutable, $userfile_description)

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
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$userfile_type = "SingleFile"; // string | Type of file that the Userfile is registered in CBRAIN as. This parameter affects what kinds of Tools can be used on the file.
$userfile_user_id = 1; // int | ID of the user who owns the file.
$userfile_group_id = 1; // int | ID of the group that will have access to the Userfile.
$tag_ids = array(56); // int[] | ID numbers of the tags that describe the Userfile.
$userfile_group_writable = true; // bool | Specifies whether other members of the group that owns the file can modify the Userfile.
$userfile_hidden = false; // bool | Specifies whether the Userfile is hidden or visible in the normal file listing.
$userfile_immutable = false; // bool | Specifies whether the Userfile can be modified.
$userfile_description = "userfile_description_example"; // string | Description of the Userfile.

try {
    $apiInstance->userfilesIdPut($id, $authenticity_token, $userfile_type, $userfile_user_id, $userfile_group_id, $tag_ids, $userfile_group_writable, $userfile_hidden, $userfile_immutable, $userfile_description);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Userfile to update. |
 **authenticity_token** | **string**| The token returned by /session/new |
 **userfile_type** | **string**| Type of file that the Userfile is registered in CBRAIN as. This parameter affects what kinds of Tools can be used on the file. | [optional] [default to SingleFile]
 **userfile_user_id** | **int**| ID of the user who owns the file. | [optional] [default to 1]
 **userfile_group_id** | **int**| ID of the group that will have access to the Userfile. | [optional] [default to 1]
 **tag_ids** | [**int[]**](../Model/int.md)| ID numbers of the tags that describe the Userfile. | [optional]
 **userfile_group_writable** | **bool**| Specifies whether other members of the group that owns the file can modify the Userfile. | [optional]
 **userfile_hidden** | **bool**| Specifies whether the Userfile is hidden or visible in the normal file listing. | [optional] [default to false]
 **userfile_immutable** | **bool**| Specifies whether the Userfile can be modified. | [optional] [default to false]
 **userfile_description** | **string**| Description of the Userfile. | [optional]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesPost**
> userfilesPost($upload_file, $data_provider_id, $userfile_group_id, $file_type, $authenticity_token, $archive, $_up_ex_mode)

Creates a new Userfile.

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
$upload_file = "/path/to/file.txt"; // \SplFileObject | File to upload to CBRAIN
$data_provider_id = 1; // int | The ID of the Data Provider to upload the file to.
$userfile_group_id = 1; // int | ID of the group that will have access to the Userfile
$file_type = "SingleFile"; // string | The type of the file
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$archive = "archive_example"; // string | Archive
$_up_ex_mode = "_up_ex_mode_example"; // string | usually \"collection\"

try {
    $apiInstance->userfilesPost($upload_file, $data_provider_id, $userfile_group_id, $file_type, $authenticity_token, $archive, $_up_ex_mode);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **upload_file** | **\SplFileObject**| File to upload to CBRAIN |
 **data_provider_id** | **int**| The ID of the Data Provider to upload the file to. | [default to 1]
 **userfile_group_id** | **int**| ID of the group that will have access to the Userfile | [default to 1]
 **file_type** | **string**| The type of the file | [default to SingleFile]
 **authenticity_token** | **string**| The token returned by /session/new |
 **archive** | **string**| Archive | [optional]
 **_up_ex_mode** | **string**| usually \&quot;collection\&quot; | [optional]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesSyncMultiplePost**
> userfilesSyncMultiplePost($file_ids, $authenticity_token, $operation)

Syncs Userfiles to their Data Providers' cache.

Synchronizing files to their Data Providers' caches allows you to download, visualize and do processing on them that is not available if not synced. CBRAIN operations will sync files automatically, and this is only necessary if a file is changed on its host Data Provdier by an external process.

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
$file_ids = array(56); // int[] | A list of Userfile ID numbers to synchronize.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$operation = "sync_local"; // string | Either \"sync_local\" or \"all_newer\". \"sync_local\" will ensure that the version of the file in the CBRAIN portal cache is the most recent version that exists on the Data Provider. \"all_newer\" will ensure that ALL caches known to CBRAIN are updated with the most recent version of the files in the host Data Provider.

try {
    $apiInstance->userfilesSyncMultiplePost($file_ids, $authenticity_token, $operation);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesSyncMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_ids** | [**int[]**](../Model/int.md)| A list of Userfile ID numbers to synchronize. |
 **authenticity_token** | **string**| The token returned by /session/new |
 **operation** | **string**| Either \&quot;sync_local\&quot; or \&quot;all_newer\&quot;. \&quot;sync_local\&quot; will ensure that the version of the file in the CBRAIN portal cache is the most recent version that exists on the Data Provider. \&quot;all_newer\&quot; will ensure that ALL caches known to CBRAIN are updated with the most recent version of the files in the host Data Provider. | [optional] [default to sync_local]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userfilesUncompressPost**
> userfilesUncompressPost($file_ids, $authenticity_token)

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
$file_ids = array(56); // int[] | A list of Userfile ID numbers to uncompress.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new

try {
    $apiInstance->userfilesUncompressPost($file_ids, $authenticity_token);
} catch (Exception $e) {
    echo 'Exception when calling UserfilesApi->userfilesUncompressPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_ids** | [**int[]**](../Model/int.md)| A list of Userfile ID numbers to uncompress. |
 **authenticity_token** | **string**| The token returned by /session/new |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

