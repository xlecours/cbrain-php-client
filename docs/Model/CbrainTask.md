# CbrainTask

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique identifier for the Task. | [optional] 
**type** | **string** | The task type | [optional] 
**user_id** | **int** | ID of the User who created the Task. | [optional] 
**group_id** | **int** | ID of the group that this task is being run in. | [optional] 
**bourreau_id** | **int** | ID of the Bourreau the Task was launched on. | [optional] 
**tool_config_id** | **int** | ID number that specifies which Tool Config to use. The Tool Config specifies environment variables and other system-specific scripts necessary for the Task to be run in the target environment. | [optional] 
**batch_id** | **int** | ID of the batch this task was launched as part of. Batches of tasks consist of the same task, with the same parameters, being run on many different input files. | [optional] 
**params** | **object** | Parameters used as inputs to the scientific calculation associated with the task. | [optional] 
**status** | **string** | Current status of the task. | [optional] 
**created_at** | **string** | Date created. | [optional] 
**updated_at** | **string** | Last updated. | [optional] 
**run_number** | **int** | The number of times that this task was run. | [optional] 
**results_data_provider_id** | **int** | ID of the Data Provider that contains the Userfile that represents the results of the task. | [optional] 
**cluster_workdir_size** | **int** | size of workdirectory | [optional] 
**workdir_archived** | **string** | Boolean variable that indicates whether the working directory of the task is available on the processing server or has been archived and is no longer accessible. | [optional] 
**workdir_archive_userfile_id** | **int** | ID of the userfile created as part of the archival process, if the working directory of the task has been archived. | [optional] 
**description** | **string** | Description of the Task. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


