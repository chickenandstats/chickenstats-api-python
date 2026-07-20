# GamePublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**game_id** | **int** |  | 
**season** | **int** |  | 
**session** | **str** |  | 
**game_date** | **str** |  | 
**start_time** | **str** |  | [optional] 
**start_time_utc** | **datetime** |  | [optional] 
**game_state** | **str** |  | [optional] 
**game_schedule_state** | **str** |  | [optional] 
**game_outcome** | **str** |  | [optional] 
**home_team** | **str** |  | 
**away_team** | **str** |  | 
**home_score** | **int** |  | [optional] 
**away_score** | **int** |  | [optional] 
**venue** | **str** |  | [optional] 
**venue_location** | **str** |  | [optional] 
**venue_timezone** | **str** |  | [optional] 
**neutral_site** | **int** |  | [optional] 

## Example

```python
from chickenstats_api.models.game_public import GamePublic

# TODO update the JSON string below
json = "{}"
# create an instance of GamePublic from a JSON string
game_public_instance = GamePublic.from_json(json)
# print the JSON string representation of the object
print(GamePublic.to_json())

# convert the object into a dict
game_public_dict = game_public_instance.to_dict()
# create an instance of GamePublic from a dict
game_public_from_dict = GamePublic.from_dict(game_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


