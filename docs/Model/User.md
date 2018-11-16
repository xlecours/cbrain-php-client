# User

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique numerical ID for the user. | [optional] 
**login** | **string** | UNIX-style username. | [optional] 
**password** | **string** | Password field | [optional] 
**password_confirmation** | **string** | Password field (generally same as &#39;password&#39;) | [optional] 
**full_name** | **string** | Full name of the user. | [optional] 
**email** | **string** | email address of the user. | [optional] 
**city** | **string** | city where the user is located | [optional] 
**country** | **string** | country where the user is located | [optional] 
**time_zone** | **string** | time-zone (should make it this an enum) | [optional] 
**type** | **string** | Classification of user permission level | [optional] [default to 'NormalUser']
**site_id** | **int** | ID of the site affiliation for the user. | [optional] 
**last_connected_at** | **string** | time of last connection by the user. (can be empty) | [optional] 
**account_locked** | **string** | Whether or not the account is locked. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


