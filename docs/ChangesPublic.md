# ChangesPublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**season** | **int** |  | 
**session** | **str** |  | 
**game_id** | **int** |  | 
**event_team** | **str** |  | 
**event** | **str** |  | [optional] 
**event_type** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**period** | **int** |  | 
**period_seconds** | **int** |  | 
**game_seconds** | **int** |  | 
**change_on_count** | **int** |  | [optional] 
**change_off_count** | **int** |  | [optional] 
**change_on_api_id** | **str** |  | [optional] 
**change_off_api_id** | **str** |  | [optional] 
**change_on_forwards_count** | **int** |  | [optional] 
**change_off_forwards_count** | **int** |  | [optional] 
**change_on_forwards_api_id** | **str** |  | [optional] 
**change_off_forwards_api_id** | **str** |  | [optional] 
**change_on_defense_count** | **int** |  | [optional] 
**change_off_defense_count** | **int** |  | [optional] 
**change_on_defense_api_id** | **str** |  | [optional] 
**change_off_defense_api_id** | **str** |  | [optional] 
**change_on_goalie_count** | **int** |  | [optional] 
**change_off_goalie_count** | **int** |  | [optional] 
**change_on_goalie_api_id** | **str** |  | [optional] 
**change_off_goalie_api_id** | **str** |  | [optional] 
**is_home** | **int** |  | 
**game** | [**GamePublic**](GamePublic.md) |  | [optional] 

## Example

```python
from chickenstats_api.models.changes_public import ChangesPublic

# TODO update the JSON string below
json = "{}"
# create an instance of ChangesPublic from a JSON string
changes_public_instance = ChangesPublic.from_json(json)
# print the JSON string representation of the object
print(ChangesPublic.to_json())

# convert the object into a dict
changes_public_dict = changes_public_instance.to_dict()
# create an instance of ChangesPublic from a dict
changes_public_from_dict = ChangesPublic.from_dict(changes_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


