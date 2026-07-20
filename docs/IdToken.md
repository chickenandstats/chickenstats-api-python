# IdToken


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id_token** | **str** |  | 

## Example

```python
from chickenstats_api.models.id_token import IdToken

# TODO update the JSON string below
json = "{}"
# create an instance of IdToken from a JSON string
id_token_instance = IdToken.from_json(json)
# print the JSON string representation of the object
print(IdToken.to_json())

# convert the object into a dict
id_token_dict = id_token_instance.to_dict()
# create an instance of IdToken from a dict
id_token_from_dict = IdToken.from_dict(id_token_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


