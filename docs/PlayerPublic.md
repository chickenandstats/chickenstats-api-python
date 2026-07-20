# PlayerPublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_id** | **int** |  | 
**eh_id** | **str** |  | [optional] 
**name** | **str** |  | 
**position** | **str** |  | [optional] 
**shoots** | **str** |  | [optional] 
**catches** | **str** |  | [optional] 
**birth_date** | **date** |  | [optional] 
**birth_city** | **str** |  | [optional] 
**birth_state_province** | **str** |  | [optional] 
**birth_country** | **str** |  | [optional] 
**nationality** | **str** |  | [optional] 
**height** | **float** |  | [optional] 
**weight** | **int** |  | [optional] 

## Example

```python
from chickenstats_api.models.player_public import PlayerPublic

# TODO update the JSON string below
json = "{}"
# create an instance of PlayerPublic from a JSON string
player_public_instance = PlayerPublic.from_json(json)
# print the JSON string representation of the object
print(PlayerPublic.to_json())

# convert the object into a dict
player_public_dict = player_public_instance.to_dict()
# create an instance of PlayerPublic from a dict
player_public_from_dict = PlayerPublic.from_dict(player_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


