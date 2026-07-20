# ShiftsPublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**season** | **int** |  | 
**session** | **str** |  | 
**game_id** | **int** |  | 
**api_id** | **int** |  | 
**team** | **str** |  | 
**shift_count** | **int** |  | 
**period** | **int** |  | 
**start_time_seconds** | **int** |  | 
**end_time_seconds** | **int** |  | 
**duration_seconds** | **int** |  | 
**goalie** | **int** |  | [optional] [default to 0]
**is_home** | **int** |  | 
**is_away** | **int** |  | 
**player** | [**PlayerPublic**](PlayerPublic.md) |  | [optional] 
**game** | [**GamePublic**](GamePublic.md) |  | [optional] 

## Example

```python
from chickenstats_api.models.shifts_public import ShiftsPublic

# TODO update the JSON string below
json = "{}"
# create an instance of ShiftsPublic from a JSON string
shifts_public_instance = ShiftsPublic.from_json(json)
# print the JSON string representation of the object
print(ShiftsPublic.to_json())

# convert the object into a dict
shifts_public_dict = shifts_public_instance.to_dict()
# create an instance of ShiftsPublic from a dict
shifts_public_from_dict = ShiftsPublic.from_dict(shifts_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


