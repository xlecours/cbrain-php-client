# MultiUserfilesModReq

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_ids** | **string[]** |  | [optional] 
**data_provider_id_for_mv_cp** | **int** |  | [optional] 
**specified_filename** | **string** | The name of the archive file that the Userfiles will be compressed into when downloading. | [optional] 
**operation** | **string** | Used when affecting the synchronization status of files. Either \&quot;sync_local\&quot; or \&quot;all_newer\&quot;. \&quot;sync_local\&quot; will ensure that the version of the file in the CBRAIN portal cache is the most recent version that exists on the Data Provider. \&quot;all_newer\&quot; will ensure that ALL caches known to CBRAIN are updated with the most recent version of the files in the host Data Provider. | [optional] [default to 'sync_local']

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


