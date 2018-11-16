# SwaggerClient-php
API for interacting with the CBRAIN Platform

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 5.1.0
- Build package: io.swagger.codegen.languages.PhpClientCodegen
For more information, please visit [https://github.com/aces/cbrain](https://github.com/aces/cbrain)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "vcs",
      "url": "git@github.com:xlecours/cbrain-php-client.git"
    }
  ],
  "require": {
    "xlecours/cbrain-php-client": "dev-master"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *http://localhost:3001*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BourreauxApi* | [**bourreauxGet**](docs/Api/BourreauxApi.md#bourreauxget) | **GET** /bourreaux | Get a list of the Bourreaux available to be used by the current user.
*BourreauxApi* | [**bourreauxIdGet**](docs/Api/BourreauxApi.md#bourreauxidget) | **GET** /bourreaux/{id} | Get information about a Bourreau.
*DataProvidersApi* | [**dataProvidersGet**](docs/Api/DataProvidersApi.md#dataprovidersget) | **GET** /data_providers | Get a list of the Data Providers available to the current user.
*DataProvidersApi* | [**dataProvidersIdBrowseGet**](docs/Api/DataProvidersApi.md#dataprovidersidbrowseget) | **GET** /data_providers/{id}/browse | List the files on a Data Provider.
*DataProvidersApi* | [**dataProvidersIdDeletePost**](docs/Api/DataProvidersApi.md#dataprovidersiddeletepost) | **POST** /data_providers/{id}/delete | Deletes unregistered files from a CBRAIN Data provider.
*DataProvidersApi* | [**dataProvidersIdGet**](docs/Api/DataProvidersApi.md#dataprovidersidget) | **GET** /data_providers/{id} | Get information on a particular Data Provider.
*DataProvidersApi* | [**dataProvidersIdIsAliveGet**](docs/Api/DataProvidersApi.md#dataprovidersidisaliveget) | **GET** /data_providers/{id}/is_alive | Pings a Data Provider to check if it is running.
*DataProvidersApi* | [**dataProvidersIdRegisterPost**](docs/Api/DataProvidersApi.md#dataprovidersidregisterpost) | **POST** /data_providers/{id}/register | Registers a file as a Userfile in CBRAIN.
*DataProvidersApi* | [**dataProvidersIdUnregisterPost**](docs/Api/DataProvidersApi.md#dataprovidersidunregisterpost) | **POST** /data_providers/{id}/unregister | Unregisters files as Userfile in CBRAIN.
*GroupsApi* | [**groupsGet**](docs/Api/GroupsApi.md#groupsget) | **GET** /groups | Get a list of the Groups (projects) available to the current user.
*GroupsApi* | [**groupsIdDelete**](docs/Api/GroupsApi.md#groupsiddelete) | **DELETE** /groups/{id} | Deletes a Group (project).
*GroupsApi* | [**groupsIdGet**](docs/Api/GroupsApi.md#groupsidget) | **GET** /groups/{id} | Get information on a Group (project).
*GroupsApi* | [**groupsIdPut**](docs/Api/GroupsApi.md#groupsidput) | **PUT** /groups/{id} | Update the properties of a Group (project).
*GroupsApi* | [**groupsPost**](docs/Api/GroupsApi.md#groupspost) | **POST** /groups | Creates a new Group.
*SessionsApi* | [**sessionDelete**](docs/Api/SessionsApi.md#sessiondelete) | **DELETE** /session | Destroy the current session
*SessionsApi* | [**sessionGet**](docs/Api/SessionsApi.md#sessionget) | **GET** /session | Get session information
*SessionsApi* | [**sessionPost**](docs/Api/SessionsApi.md#sessionpost) | **POST** /session | Create a new session
*TagsApi* | [**tagsGet**](docs/Api/TagsApi.md#tagsget) | **GET** /tags | Get a list of the tags currently in CBRAIN.
*TagsApi* | [**tagsIdDelete**](docs/Api/TagsApi.md#tagsiddelete) | **DELETE** /tags/{id} | Delete a tag.
*TagsApi* | [**tagsIdGet**](docs/Api/TagsApi.md#tagsidget) | **GET** /tags/{id} | Get one tag.
*TagsApi* | [**tagsIdPut**](docs/Api/TagsApi.md#tagsidput) | **PUT** /tags/{id} | Update a tag.
*TagsApi* | [**tagsPost**](docs/Api/TagsApi.md#tagspost) | **POST** /tags | Create a new tag.
*TasksApi* | [**tasksGet**](docs/Api/TasksApi.md#tasksget) | **GET** /tasks | Get the list of Tasks.
*TasksApi* | [**tasksIdGet**](docs/Api/TasksApi.md#tasksidget) | **GET** /tasks/{id} | Get information on a Task.
*TasksApi* | [**tasksPost**](docs/Api/TasksApi.md#taskspost) | **POST** /tasks | Create a new Task.
*ToolConfigsApi* | [**toolConfigsGet**](docs/Api/ToolConfigsApi.md#toolconfigsget) | **GET** /tool_configs | Get a list of tool versions installed.
*ToolConfigsApi* | [**toolConfigsIdGet**](docs/Api/ToolConfigsApi.md#toolconfigsidget) | **GET** /tool_configs/{id} | Get information about a particular tool configuration
*ToolsApi* | [**toolsGet**](docs/Api/ToolsApi.md#toolsget) | **GET** /tools | Get the list of Tools.
*UserfilesApi* | [**userfilesChangeProviderPost**](docs/Api/UserfilesApi.md#userfileschangeproviderpost) | **POST** /userfiles/change_provider | Moves the Userfiles from their current Data Provider to a new one.
*UserfilesApi* | [**userfilesCompressPost**](docs/Api/UserfilesApi.md#userfilescompresspost) | **POST** /userfiles/compress | Compresses many Userfiles each into their own GZIP archive.
*UserfilesApi* | [**userfilesDeleteFilesDelete**](docs/Api/UserfilesApi.md#userfilesdeletefilesdelete) | **DELETE** /userfiles/delete_files | Delete several files that have been registered as Userfiles
*UserfilesApi* | [**userfilesDownloadPost**](docs/Api/UserfilesApi.md#userfilesdownloadpost) | **POST** /userfiles/download | Download several files
*UserfilesApi* | [**userfilesGet**](docs/Api/UserfilesApi.md#userfilesget) | **GET** /userfiles | List of the Userfiles accessible to the current user.
*UserfilesApi* | [**userfilesIdContentGet**](docs/Api/UserfilesApi.md#userfilesidcontentget) | **GET** /userfiles/{id}/content | Get the content of a Userfile
*UserfilesApi* | [**userfilesIdGet**](docs/Api/UserfilesApi.md#userfilesidget) | **GET** /userfiles/{id} | Get information on a Userfile.
*UserfilesApi* | [**userfilesIdPut**](docs/Api/UserfilesApi.md#userfilesidput) | **PUT** /userfiles/{id} | Update information on a Userfile.
*UserfilesApi* | [**userfilesPost**](docs/Api/UserfilesApi.md#userfilespost) | **POST** /userfiles | Creates a new Userfile and upload its content.
*UserfilesApi* | [**userfilesSyncMultiplePost**](docs/Api/UserfilesApi.md#userfilessyncmultiplepost) | **POST** /userfiles/sync_multiple | Syncs Userfiles to the local Data Providers cache.
*UserfilesApi* | [**userfilesUncompressPost**](docs/Api/UserfilesApi.md#userfilesuncompresspost) | **POST** /userfiles/uncompress | Uncompresses many Userfiles.
*UsersApi* | [**usersGet**](docs/Api/UsersApi.md#usersget) | **GET** /users | Returns all of the users in CBRAIN. Only available to admins.
*UsersApi* | [**usersIdDelete**](docs/Api/UsersApi.md#usersiddelete) | **DELETE** /users/{id} | Deletes a CBRAIN user
*UsersApi* | [**usersIdGet**](docs/Api/UsersApi.md#usersidget) | **GET** /users/{id} | Returns information about a user
*UsersApi* | [**usersIdPatch**](docs/Api/UsersApi.md#usersidpatch) | **PATCH** /users/{id} | Update information about a user
*UsersApi* | [**usersPost**](docs/Api/UsersApi.md#userspost) | **POST** /users | Create a new user in CBRAIN. Only available to admins.


## Documentation For Models

 - [Bourreau](docs/Model/Bourreau.md)
 - [CbrainTask](docs/Model/CbrainTask.md)
 - [CbrainTaskModReq](docs/Model/CbrainTaskModReq.md)
 - [DataProvider](docs/Model/DataProvider.md)
 - [FileInfo](docs/Model/FileInfo.md)
 - [Group](docs/Model/Group.md)
 - [GroupModReq](docs/Model/GroupModReq.md)
 - [MultiRegistrationModReq](docs/Model/MultiRegistrationModReq.md)
 - [MultiUserfilesModReq](docs/Model/MultiUserfilesModReq.md)
 - [RegistrationInfo](docs/Model/RegistrationInfo.md)
 - [SessionInfo](docs/Model/SessionInfo.md)
 - [Tag](docs/Model/Tag.md)
 - [TagModReq](docs/Model/TagModReq.md)
 - [Tool](docs/Model/Tool.md)
 - [ToolConfig](docs/Model/ToolConfig.md)
 - [User](docs/Model/User.md)
 - [UserModReq](docs/Model/UserModReq.md)
 - [Userfile](docs/Model/Userfile.md)
 - [UserfileModReq](docs/Model/UserfileModReq.md)


## Documentation For Authorization


## BrainPortalSession

- **Type**: API key
- **API key parameter name**: cbrain_api_token
- **Location**: URL query string


## Author




