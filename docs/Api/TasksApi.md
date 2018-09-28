# Swagger\Client\TasksApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tasksGet**](TasksApi.md#tasksGet) | **GET** /tasks | Get the list of Tasks.
[**tasksIdDelete**](TasksApi.md#tasksIdDelete) | **DELETE** /tasks/{id} | Deletes a Task
[**tasksIdGet**](TasksApi.md#tasksIdGet) | **GET** /tasks/{id} | Get information on a Task.
[**tasksIdPut**](TasksApi.md#tasksIdPut) | **PUT** /tasks/{id} | Update information on a Task.
[**tasksPost**](TasksApi.md#tasksPost) | **POST** /tasks | Create a new Task.


# **tasksGet**
> \Swagger\Client\Model\CbrainTask[] tasksGet()

Get the list of Tasks.

This method returns the list of Tasks accessible to the current user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->tasksGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->tasksGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\CbrainTask[]**](../Model/CbrainTask.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **tasksIdDelete**
> tasksIdDelete($id, $authenticity_token)

Deletes a Task

Deletes a Task from CBRAIN.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID number of the Task to delete.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new

try {
    $apiInstance->tasksIdDelete($id, $authenticity_token);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->tasksIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Task to delete. |
 **authenticity_token** | **string**| The token returned by /session/new | [optional]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **tasksIdGet**
> \Swagger\Client\Model\CbrainTask tasksIdGet($id)

Get information on a Task.

This method returns information on a Task, including its status, Task restartability and information on where the results are kept.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID number of the Task to delete.

try {
    $result = $apiInstance->tasksIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->tasksIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Task to delete. |

### Return type

[**\Swagger\Client\Model\CbrainTask**](../Model/CbrainTask.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **tasksIdPut**
> tasksIdPut($id, $cbrain_task_description, $authenticity_token, $cbrain_task_results_data_provider_id, $cbrain_task_user_id, $cbrain_task_group_id)

Update information on a Task.

This method updates information about a Task in CBRAIN.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID number of the Task to update.
$cbrain_task_description = "cbrain_task_description_example"; // string | Description of the Task.
$authenticity_token = "authenticity_token_example"; // string | The token returned by /session/new
$cbrain_task_results_data_provider_id = 1; // int | ID of the DataProvider to store the results of the Task on.
$cbrain_task_user_id = 56; // int | ID of the User the Task should be associated with.
$cbrain_task_group_id = 1; // int | ID of the Group the Task should be associated with.

try {
    $apiInstance->tasksIdPut($id, $cbrain_task_description, $authenticity_token, $cbrain_task_results_data_provider_id, $cbrain_task_user_id, $cbrain_task_group_id);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->tasksIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The ID number of the Task to update. |
 **cbrain_task_description** | **string**| Description of the Task. |
 **authenticity_token** | **string**| The token returned by /session/new |
 **cbrain_task_results_data_provider_id** | **int**| ID of the DataProvider to store the results of the Task on. | [optional] [default to 1]
 **cbrain_task_user_id** | **int**| ID of the User the Task should be associated with. | [optional]
 **cbrain_task_group_id** | **int**| ID of the Group the Task should be associated with. | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **tasksPost**
> \Swagger\Client\Model\CbrainTask[] tasksPost($cbrain_task)

Create a new Task.

This method allows the creation of a new Task.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cbrain_task = new \Swagger\Client\Model\CbrainTask(); // \Swagger\Client\Model\CbrainTask | The task to create.

try {
    $result = $apiInstance->tasksPost($cbrain_task);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->tasksPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cbrain_task** | [**\Swagger\Client\Model\CbrainTask**](../Model/CbrainTask.md)| The task to create. | [optional]

### Return type

[**\Swagger\Client\Model\CbrainTask[]**](../Model/CbrainTask.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

