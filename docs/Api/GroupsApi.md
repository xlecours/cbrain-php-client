# Swagger\Client\GroupsApi

All URIs are relative to *https://portal.cbrain.mcgill.ca*

Method | HTTP request | Description
------------- | ------------- | -------------
[**groupsGet**](GroupsApi.md#groupsGet) | **GET** /groups | Get a list of the Groups (projects) available to the current user.
[**groupsIdDelete**](GroupsApi.md#groupsIdDelete) | **DELETE** /groups/{id} | Deletes a Group (project).
[**groupsIdGet**](GroupsApi.md#groupsIdGet) | **GET** /groups/{id} | Get information on a Group (project).
[**groupsIdPut**](GroupsApi.md#groupsIdPut) | **PUT** /groups/{id} | Update the properties of a Group (project).
[**groupsPost**](GroupsApi.md#groupsPost) | **POST** /groups | Creates a new Group.


# **groupsGet**
> \Swagger\Client\Model\Group[] groupsGet()

Get a list of the Groups (projects) available to the current user.

This method returns a list of all of the groups that the current user has access to.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->groupsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->groupsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Group[]**](../Model/Group.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **groupsIdDelete**
> groupsIdDelete($id)

Deletes a Group (project).

This method allows the removal of Groups (projects) that are no longer necessary. Groups that have Userfiles associated with them may not be deleted.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | ID of the Group to delete.

try {
    $apiInstance->groupsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->groupsIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the Group to delete. |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **groupsIdGet**
> \Swagger\Client\Model\Group groupsIdGet($id)

Get information on a Group (project).

This method returns information on a single Group (project), specified by the ID parameter. Information returned includes the list of Users who are members of the group, the ID of the Site the Group is part of, and whether or not the group is visible to Regular Users.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | ID of the Group to get information on.

try {
    $result = $apiInstance->groupsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->groupsIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the Group to get information on. |

### Return type

[**\Swagger\Client\Model\Group**](../Model/Group.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **groupsIdPut**
> groupsIdPut($id, $group_mod_req)

Update the properties of a Group (project).

This method allows the properties of a Group (project) to be updated. This includes the User membership, the ID of the site the Group belongs to, and the visibility status of the group to Regular Users.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | ID of the Group
$group_mod_req = new \Swagger\Client\Model\GroupModReq(); // \Swagger\Client\Model\GroupModReq | An object with the group information to update

try {
    $apiInstance->groupsIdPut($id, $group_mod_req);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->groupsIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the Group |
 **group_mod_req** | [**\Swagger\Client\Model\GroupModReq**](../Model/GroupModReq.md)| An object with the group information to update |

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **groupsPost**
> \Swagger\Client\Model\Group groupsPost($group_mod_req)

Creates a new Group.

This method creates a new Group, which allows users to organize their files and tasks.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_mod_req = new \Swagger\Client\Model\GroupModReq(); // \Swagger\Client\Model\GroupModReq | An object describing the group to create

try {
    $result = $apiInstance->groupsPost($group_mod_req);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->groupsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_mod_req** | [**\Swagger\Client\Model\GroupModReq**](../Model/GroupModReq.md)| An object describing the group to create |

### Return type

[**\Swagger\Client\Model\Group**](../Model/Group.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

