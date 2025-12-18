# chickenstats_api.ChickenNhlApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chicken_nhl_create_lines**](ChickenNhlApi.md#chicken_nhl_create_lines) | **POST** /api/v1/chicken_nhl/lines | Create Lines
[**chicken_nhl_create_pbp**](ChickenNhlApi.md#chicken_nhl_create_pbp) | **POST** /api/v1/chicken_nhl/play_by_play | Create Pbp
[**chicken_nhl_create_stats**](ChickenNhlApi.md#chicken_nhl_create_stats) | **POST** /api/v1/chicken_nhl/stats | Create Stats
[**chicken_nhl_create_team_stats**](ChickenNhlApi.md#chicken_nhl_create_team_stats) | **POST** /api/v1/chicken_nhl/team_stats | Create Team Stats
[**chicken_nhl_read_game_stats**](ChickenNhlApi.md#chicken_nhl_read_game_stats) | **GET** /api/v1/chicken_nhl/stats/game | Read Game Stats
[**chicken_nhl_read_lines_game_ids**](ChickenNhlApi.md#chicken_nhl_read_lines_game_ids) | **GET** /api/v1/chicken_nhl/lines/game_ids | Read Lines Game Ids
[**chicken_nhl_read_pbp**](ChickenNhlApi.md#chicken_nhl_read_pbp) | **GET** /api/v1/chicken_nhl/play_by_play | Read Pbp
[**chicken_nhl_read_pbp_game_ids**](ChickenNhlApi.md#chicken_nhl_read_pbp_game_ids) | **GET** /api/v1/chicken_nhl/play_by_play/game_ids | Read Pbp Game Ids
[**chicken_nhl_read_pbp_play_ids**](ChickenNhlApi.md#chicken_nhl_read_pbp_play_ids) | **GET** /api/v1/chicken_nhl/play_by_play/play_ids | Read Pbp Play Ids
[**chicken_nhl_read_season_stats**](ChickenNhlApi.md#chicken_nhl_read_season_stats) | **GET** /api/v1/chicken_nhl/stats/season | Read Season Stats
[**chicken_nhl_read_stats_game_ids**](ChickenNhlApi.md#chicken_nhl_read_stats_game_ids) | **GET** /api/v1/chicken_nhl/stats/game_ids | Read Stats Game Ids
[**chicken_nhl_read_team_stats_game_ids**](ChickenNhlApi.md#chicken_nhl_read_team_stats_game_ids) | **GET** /api/v1/chicken_nhl/team_stats/game_ids | Read Team Stats Game Ids


# **chicken_nhl_create_lines**
> LinesPublic chicken_nhl_create_lines(lines_create)

Create Lines

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.lines_create import LinesCreate
from chickenstats_api.models.lines_public import LinesPublic
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    lines_create = chickenstats_api.LinesCreate() # LinesCreate | 

    try:
        # Create Lines
        api_response = api_instance.chicken_nhl_create_lines(lines_create)
        print("The response of ChickenNhlApi->chicken_nhl_create_lines:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_create_lines: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lines_create** | [**LinesCreate**](LinesCreate.md)|  | 

### Return type

[**LinesPublic**](LinesPublic.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chicken_nhl_create_pbp**
> PbpPublic chicken_nhl_create_pbp(pbp_public)

Create Pbp

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.pbp_public import PbpPublic
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    pbp_public = chickenstats_api.PbpPublic() # PbpPublic | 

    try:
        # Create Pbp
        api_response = api_instance.chicken_nhl_create_pbp(pbp_public)
        print("The response of ChickenNhlApi->chicken_nhl_create_pbp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_create_pbp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pbp_public** | [**PbpPublic**](PbpPublic.md)|  | 

### Return type

[**PbpPublic**](PbpPublic.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chicken_nhl_create_stats**
> StatsGame chicken_nhl_create_stats(stats_create)

Create Stats

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.stats_create import StatsCreate
from chickenstats_api.models.stats_game import StatsGame
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    stats_create = chickenstats_api.StatsCreate() # StatsCreate | 

    try:
        # Create Stats
        api_response = api_instance.chicken_nhl_create_stats(stats_create)
        print("The response of ChickenNhlApi->chicken_nhl_create_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_create_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stats_create** | [**StatsCreate**](StatsCreate.md)|  | 

### Return type

[**StatsGame**](StatsGame.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chicken_nhl_create_team_stats**
> TeamStatsPublic chicken_nhl_create_team_stats(team_stats_create)

Create Team Stats

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.team_stats_create import TeamStatsCreate
from chickenstats_api.models.team_stats_public import TeamStatsPublic
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    team_stats_create = chickenstats_api.TeamStatsCreate() # TeamStatsCreate | 

    try:
        # Create Team Stats
        api_response = api_instance.chicken_nhl_create_team_stats(team_stats_create)
        print("The response of ChickenNhlApi->chicken_nhl_create_team_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_create_team_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **team_stats_create** | [**TeamStatsCreate**](TeamStatsCreate.md)|  | 

### Return type

[**TeamStatsPublic**](TeamStatsPublic.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chicken_nhl_read_game_stats**
> List[StatsGame] chicken_nhl_read_game_stats(season=season, sessions=sessions, game_id=game_id, level=level, player=player, api_id=api_id, eh_id=eh_id, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, teammates=teammates, opposition=opposition)

Read Game Stats

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.stats_game import StatsGame
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    game_id = [56] # List[int] |  (optional)
    level = 'level_example' # str |  (optional)
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
        # Read Game Stats
        api_response = api_instance.chicken_nhl_read_game_stats(season=season, sessions=sessions, game_id=game_id, level=level, player=player, api_id=api_id, eh_id=eh_id, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, teammates=teammates, opposition=opposition)
        print("The response of ChickenNhlApi->chicken_nhl_read_game_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_game_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 
 **game_id** | [**List[int]**](int.md)|  | [optional] 
 **level** | **str**|  | [optional] 
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

[**List[StatsGame]**](StatsGame.md)

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

# **chicken_nhl_read_lines_game_ids**
> List[int] chicken_nhl_read_lines_game_ids(season=season, sessions=sessions)

Read Lines Game Ids

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Lines Game Ids
        api_response = api_instance.chicken_nhl_read_lines_game_ids(season=season, sessions=sessions)
        print("The response of ChickenNhlApi->chicken_nhl_read_lines_game_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_lines_game_ids: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 

### Return type

**List[int]**

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

# **chicken_nhl_read_pbp**
> List[PbpPublic] chicken_nhl_read_pbp(season=season, sessions=sessions, game_id=game_id, event=event, player_1=player_1, goalie=goalie, event_team=event_team, opp_team=opp_team, strength_state=strength_state)

Read Pbp

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.pbp_public import PbpPublic
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    game_id = [56] # List[int] |  (optional)
    event = ['event_example'] # List[str] |  (optional)
    player_1 = ['player_1_example'] # List[str] |  (optional)
    goalie = ['goalie_example'] # List[str] |  (optional)
    event_team = ['event_team_example'] # List[str] |  (optional)
    opp_team = ['opp_team_example'] # List[str] |  (optional)
    strength_state = ['strength_state_example'] # List[str] |  (optional)

    try:
        # Read Pbp
        api_response = api_instance.chicken_nhl_read_pbp(season=season, sessions=sessions, game_id=game_id, event=event, player_1=player_1, goalie=goalie, event_team=event_team, opp_team=opp_team, strength_state=strength_state)
        print("The response of ChickenNhlApi->chicken_nhl_read_pbp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_pbp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 
 **game_id** | [**List[int]**](int.md)|  | [optional] 
 **event** | [**List[str]**](str.md)|  | [optional] 
 **player_1** | [**List[str]**](str.md)|  | [optional] 
 **goalie** | [**List[str]**](str.md)|  | [optional] 
 **event_team** | [**List[str]**](str.md)|  | [optional] 
 **opp_team** | [**List[str]**](str.md)|  | [optional] 
 **strength_state** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[PbpPublic]**](PbpPublic.md)

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

# **chicken_nhl_read_pbp_game_ids**
> List[int] chicken_nhl_read_pbp_game_ids(season=season, sessions=sessions)

Read Pbp Game Ids

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Pbp Game Ids
        api_response = api_instance.chicken_nhl_read_pbp_game_ids(season=season, sessions=sessions)
        print("The response of ChickenNhlApi->chicken_nhl_read_pbp_game_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_pbp_game_ids: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 

### Return type

**List[int]**

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

# **chicken_nhl_read_pbp_play_ids**
> List[int] chicken_nhl_read_pbp_play_ids(season=season, sessions=sessions, game_id=game_id)

Read Pbp Play Ids

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    game_id = [56] # List[int] |  (optional)

    try:
        # Read Pbp Play Ids
        api_response = api_instance.chicken_nhl_read_pbp_play_ids(season=season, sessions=sessions, game_id=game_id)
        print("The response of ChickenNhlApi->chicken_nhl_read_pbp_play_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_pbp_play_ids: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 
 **game_id** | [**List[int]**](int.md)|  | [optional] 

### Return type

**List[int]**

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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
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
        print("The response of ChickenNhlApi->chicken_nhl_read_season_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_season_stats: %s\n" % e)
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

# **chicken_nhl_read_stats_game_ids**
> List[int] chicken_nhl_read_stats_game_ids(season=season, sessions=sessions)

Read Stats Game Ids

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Stats Game Ids
        api_response = api_instance.chicken_nhl_read_stats_game_ids(season=season, sessions=sessions)
        print("The response of ChickenNhlApi->chicken_nhl_read_stats_game_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_stats_game_ids: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 

### Return type

**List[int]**

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

# **chicken_nhl_read_team_stats_game_ids**
> List[int] chicken_nhl_read_team_stats_game_ids(season=season, sessions=sessions)

Read Team Stats Game Ids

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
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
    api_instance = chickenstats_api.ChickenNhlApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Team Stats Game Ids
        api_response = api_instance.chicken_nhl_read_team_stats_game_ids(season=season, sessions=sessions)
        print("The response of ChickenNhlApi->chicken_nhl_read_team_stats_game_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChickenNhlApi->chicken_nhl_read_team_stats_game_ids: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 

### Return type

**List[int]**

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

