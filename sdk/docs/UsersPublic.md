# UsersPublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[UserPublic]**](UserPublic.md) |  | 
**count** | **int** |  | 

## Example

```python
from chickenstats_api.models.users_public import UsersPublic

# TODO update the JSON string below
json = "{}"
# create an instance of UsersPublic from a JSON string
users_public_instance = UsersPublic.from_json(json)
# print the JSON string representation of the object
print(UsersPublic.to_json())

# convert the object into a dict
users_public_dict = users_public_instance.to_dict()
# create an instance of UsersPublic from a dict
users_public_from_dict = UsersPublic.from_dict(users_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


