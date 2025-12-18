# chickenstats_api.SeasonStatsApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chicken_nhl_read_season_stats**](SeasonStatsApi.md#chicken_nhl_read_season_stats) | **GET** /api/v1/chicken_nhl/stats/season | Read Season Stats


# **chicken_nhl_read_season_stats**
> List[StatsSeason] chicken_nhl_read_season_stats(season=season, sessions=sessions, player=player, api_id=api_id, eh_id=eh_id, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, teammates=teammates, opposition=opposition)

Read Season Stats

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.stats_season import StatsSeason
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.chickenstats.com
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "https://api.chickenstats.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with chickenstats_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = chickenstats_api.SeasonStatsApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    player = ['player_example'] # List[str] |  (optional)
    api_id = [56] # List[int] |  (optional)
    eh_id = ['eh_id_example'] # List[str] |  (optional)
    team = ['team_example'] # List[str] |  (optional)
    opp_team = ['opp_team_example'] # List[str] |  (optional)
    strength_state = ['strength_state_example'] # List[str] |  (optional)
    score_state = True # bool |  (optional)
    teammates = True # bool |  (optional)
    opposition = True # bool |  (optional)

    try:
        # Read Season Stats
        api_response = api_instance.chicken_nhl_read_season_stats(season=season, sessions=sessions, player=player, api_id=api_id, eh_id=eh_id, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, teammates=teammates, opposition=opposition)
        print("The response of SeasonStatsApi->chicken_nhl_read_season_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SeasonStatsApi->chicken_nhl_read_season_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 
 **player** | [**List[str]**](str.md)|  | [optional] 
 **api_id** | [**List[int]**](int.md)|  | [optional] 
 **eh_id** | [**List[str]**](str.md)|  | [optional] 
 **team** | [**List[str]**](str.md)|  | [optional] 
 **opp_team** | [**List[str]**](str.md)|  | [optional] 
 **strength_state** | [**List[str]**](str.md)|  | [optional] 
 **score_state** | **bool**|  | [optional] 
 **teammates** | **bool**|  | [optional] 
 **opposition** | **bool**|  | [optional] 

### Return type

[**List[StatsSeason]**](StatsSeason.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

