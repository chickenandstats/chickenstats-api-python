# UpdatePassword


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_password** | **str** |  | 
**new_password** | **str** |  | 

## Example

```python
from chickenstats_api.models.update_password import UpdatePassword

# TODO update the JSON string below
json = "{}"
# create an instance of UpdatePassword from a JSON string
update_password_instance = UpdatePassword.from_json(json)
# print the JSON string representation of the object
print(UpdatePassword.to_json())

# convert the object into a dict
update_password_dict = update_password_instance.to_dict()
# create an instance of UpdatePassword from a dict
update_password_from_dict = UpdatePassword.from_dict(update_password_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


