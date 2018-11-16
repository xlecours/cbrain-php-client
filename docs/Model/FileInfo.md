# FileInfo

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userfile_id** | **int** | id of the userfile | [optional] 
**name** | **string** | the base filename | [optional] 
**group** | **string** | string representation of gid, the name of the group | [optional] 
**gid** | **int** | numeric group id of the file | [optional] 
**owner** | **string** | string representation of uid, the name of the owner | [optional] 
**uid** | **int** | numeric uid of owner | [optional] 
**permissions** | **int** | an int interpreted in octal, e.g. 0640 | [optional] 
**size** | **int** | size of file in bytes | [optional] 
**state_ok** | **bool** | flag that tell whether or not it is OK to register/unregister | [optional] 
**message** | **string** | a message to give more information about the state_ok flag | [optional] 
**symbolic_type** | **string** | one of :regular, :symlink, :directory | [optional] 
**atime** | **int** | access time (an int, since Epoch) | [optional] 
**mtime** | **int** | modification time (an int, since Epoch) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


