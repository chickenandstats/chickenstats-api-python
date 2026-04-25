# ProgrammaticCredentials


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cf_client_id** | **str** |  | 
**cf_client_secret** | **str** |  | [optional] 
**auth0_token_endpoint** | **str** |  | [optional] [default to 'POST /api/v1/login/auth0-token']
**note** | **str** |  | [optional] [default to 'The secret is shown once. Store it securely — rotate if lost.']

## Example

```python
from chickenstats_api.models.programmatic_credentials import ProgrammaticCredentials

# TODO update the JSON string below
json = "{}"
# create an instance of ProgrammaticCredentials from a JSON string
programmatic_credentials_instance = ProgrammaticCredentials.from_json(json)
# print the JSON string representation of the object
print(ProgrammaticCredentials.to_json())

# convert the object into a dict
programmatic_credentials_dict = programmatic_credentials_instance.to_dict()
# create an instance of ProgrammaticCredentials from a dict
programmatic_credentials_from_dict = ProgrammaticCredentials.from_dict(programmatic_credentials_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


