# LinesPublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**season** | **int** |  | 
**session** | **str** |  | 
**game_id** | **int** |  | 
**game_date** | **str** |  | 
**team** | **str** |  | 
**opp_team** | **str** |  | [optional] 
**strength_state** | **str** |  | [optional] 
**period** | **int** |  | [optional] 
**score_state** | **str** |  | [optional] 
**forwards** | **str** |  | [optional] 
**forwards_eh_id** | **str** |  | [optional] 
**forwards_api_id** | **str** |  | [optional] 
**defense** | **str** |  | [optional] 
**defense_eh_id** | **str** |  | [optional] 
**defense_api_id** | **str** |  | [optional] 
**own_goalie** | **str** |  | [optional] 
**own_goalie_eh_id** | **str** |  | [optional] 
**own_goalie_api_id** | **int** |  | [optional] 
**opp_forwards** | **str** |  | [optional] 
**opp_forwards_eh_id** | **str** |  | [optional] 
**opp_forwards_api_id** | **str** |  | [optional] 
**opp_defense** | **str** |  | [optional] 
**opp_defense_eh_id** | **str** |  | [optional] 
**opp_defense_api_id** | **str** |  | [optional] 
**opp_goalie** | **str** |  | [optional] 
**opp_goalie_eh_id** | **str** |  | [optional] 
**opp_goalie_api_id** | **int** |  | [optional] 
**toi** | **float** |  | 
**gf** | **int** |  | [optional] [default to 0]
**ga** | **int** |  | [optional] [default to 0]
**gf_adj** | **float** |  | [optional] [default to 0]
**ga_adj** | **float** |  | [optional] [default to 0]
**hdgf** | **int** |  | [optional] [default to 0]
**hdga** | **int** |  | [optional] [default to 0]
**xgf** | **float** |  | [optional] [default to 0]
**xga** | **float** |  | [optional] [default to 0]
**xgf_adj** | **float** |  | [optional] [default to 0]
**xga_adj** | **float** |  | [optional] [default to 0]
**sf** | **int** |  | [optional] [default to 0]
**sa** | **int** |  | [optional] [default to 0]
**sf_adj** | **float** |  | [optional] [default to 0]
**sa_adj** | **float** |  | [optional] [default to 0]
**hdsf** | **int** |  | [optional] [default to 0]
**hdsa** | **int** |  | [optional] [default to 0]
**ff** | **int** |  | [optional] [default to 0]
**fa** | **int** |  | [optional] [default to 0]
**ff_adj** | **float** |  | [optional] [default to 0]
**fa_adj** | **float** |  | [optional] [default to 0]
**hdff** | **int** |  | [optional] [default to 0]
**hdfa** | **int** |  | [optional] [default to 0]
**cf** | **int** |  | [optional] [default to 0]
**ca** | **int** |  | [optional] [default to 0]
**cf_adj** | **float** |  | [optional] [default to 0]
**ca_adj** | **float** |  | [optional] [default to 0]
**bsf** | **int** |  | [optional] [default to 0]
**bsa** | **int** |  | [optional] [default to 0]
**bsf_adj** | **float** |  | [optional] [default to 0]
**bsa_adj** | **float** |  | [optional] [default to 0]
**msf** | **int** |  | [optional] [default to 0]
**msa** | **int** |  | [optional] [default to 0]
**msf_adj** | **float** |  | [optional] [default to 0]
**msa_adj** | **float** |  | [optional] [default to 0]
**hdmsf** | **int** |  | [optional] [default to 0]
**hdmsa** | **int** |  | [optional] [default to 0]
**teammate_block** | **int** |  | [optional] [default to 0]
**teammate_block_adj** | **float** |  | [optional] [default to 0]
**hf** | **int** |  | [optional] [default to 0]
**ht** | **int** |  | [optional] [default to 0]
**give** | **int** |  | [optional] [default to 0]
**take** | **int** |  | [optional] [default to 0]
**ozf** | **int** |  | [optional] [default to 0]
**nzf** | **int** |  | [optional] [default to 0]
**dzf** | **int** |  | [optional] [default to 0]
**fow** | **int** |  | [optional] [default to 0]
**fol** | **int** |  | [optional] [default to 0]
**ozfw** | **int** |  | [optional] [default to 0]
**ozfl** | **int** |  | [optional] [default to 0]
**nzfw** | **int** |  | [optional] [default to 0]
**nzfl** | **int** |  | [optional] [default to 0]
**dzfw** | **int** |  | [optional] [default to 0]
**dzfl** | **int** |  | [optional] [default to 0]
**pent0** | **int** |  | [optional] [default to 0]
**pent2** | **int** |  | [optional] [default to 0]
**pent4** | **int** |  | [optional] [default to 0]
**pent5** | **int** |  | [optional] [default to 0]
**pent10** | **int** |  | [optional] [default to 0]
**pend0** | **int** |  | [optional] [default to 0]
**pend2** | **int** |  | [optional] [default to 0]
**pend4** | **int** |  | [optional] [default to 0]
**pend5** | **int** |  | [optional] [default to 0]
**pend10** | **int** |  | [optional] [default to 0]

## Example

```python
from chickenstats_api.models.lines_public import LinesPublic

# TODO update the JSON string below
json = "{}"
# create an instance of LinesPublic from a JSON string
lines_public_instance = LinesPublic.from_json(json)
# print the JSON string representation of the object
print(LinesPublic.to_json())

# convert the object into a dict
lines_public_dict = lines_public_instance.to_dict()
# create an instance of LinesPublic from a dict
lines_public_from_dict = LinesPublic.from_dict(lines_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


