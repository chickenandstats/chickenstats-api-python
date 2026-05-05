# chickenstats_api.LinesApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**read_game_lines**](LinesApi.md#read_game_lines) | **GET** /api/v1/chicken_nhl/lines/game | Read Game Lines
[**read_line_ids**](LinesApi.md#read_line_ids) | **GET** /api/v1/chicken_nhl/lines/line_ids | Read Line Ids
[**read_lines_game_ids**](LinesApi.md#read_lines_game_ids) | **GET** /api/v1/chicken_nhl/lines/game_ids | Read Lines Game Ids
[**read_season_lines**](LinesApi.md#read_season_lines) | **GET** /api/v1/chicken_nhl/lines/season | Read Season Lines


# **read_game_lines**
> LinesGameResponse read_game_lines(season=season, sessions=sessions, game_id=game_id, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, level=level, linemates=linemates, opposition=opposition, limit=limit, offset=offset)

Read Game Lines

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.lines_game_response import LinesGameResponse
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
    api_instance = chickenstats_api.LinesApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    game_id = [56] # List[int] |  (optional)
    team = ['team_example'] # List[str] |  (optional)
    opp_team = ['opp_team_example'] # List[str] |  (optional)
    strength_state = ['strength_state_example'] # List[str] |  (optional)
    score_state = True # bool |  (optional)
    level = 'level_example' # str |  (optional)
    linemates = True # bool |  (optional)
    opposition = True # bool |  (optional)
    limit = 10000 # int |  (optional) (default to 10000)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Read Game Lines
        api_response = api_instance.read_game_lines(season=season, sessions=sessions, game_id=game_id, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, level=level, linemates=linemates, opposition=opposition, limit=limit, offset=offset)
        print("The response of LinesApi->read_game_lines:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinesApi->read_game_lines: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 
 **game_id** | [**List[int]**](int.md)|  | [optional] 
 **team** | [**List[str]**](str.md)|  | [optional] 
 **opp_team** | [**List[str]**](str.md)|  | [optional] 
 **strength_state** | [**List[str]**](str.md)|  | [optional] 
 **score_state** | **bool**|  | [optional] 
 **level** | **str**|  | [optional] 
 **linemates** | **bool**|  | [optional] 
 **opposition** | **bool**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 10000]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**LinesGameResponse**](LinesGameResponse.md)

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

# **read_line_ids**
> List[str] read_line_ids(season=season, sessions=sessions)

Read Line Ids

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
    api_instance = chickenstats_api.LinesApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Line Ids
        api_response = api_instance.read_line_ids(season=season, sessions=sessions)
        print("The response of LinesApi->read_line_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinesApi->read_line_ids: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 

### Return type

**List[str]**

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

# **read_lines_game_ids**
> List[int] read_lines_game_ids(season=season, sessions=sessions)

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
    api_instance = chickenstats_api.LinesApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Lines Game Ids
        api_response = api_instance.read_lines_game_ids(season=season, sessions=sessions)
        print("The response of LinesApi->read_lines_game_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinesApi->read_lines_game_ids: %s\n" % e)
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

# **read_season_lines**
> LinesSeasonResponse read_season_lines(season=season, sessions=sessions, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, linemates=linemates, opposition=opposition, limit=limit, offset=offset)

Read Season Lines

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.lines_season_response import LinesSeasonResponse
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
    api_instance = chickenstats_api.LinesApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    team = ['team_example'] # List[str] |  (optional)
    opp_team = ['opp_team_example'] # List[str] |  (optional)
    strength_state = ['strength_state_example'] # List[str] |  (optional)
    score_state = True # bool |  (optional)
    linemates = True # bool |  (optional)
    opposition = True # bool |  (optional)
    limit = 10000 # int |  (optional) (default to 10000)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Read Season Lines
        api_response = api_instance.read_season_lines(season=season, sessions=sessions, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, linemates=linemates, opposition=opposition, limit=limit, offset=offset)
        print("The response of LinesApi->read_season_lines:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinesApi->read_season_lines: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 
 **team** | [**List[str]**](str.md)|  | [optional] 
 **opp_team** | [**List[str]**](str.md)|  | [optional] 
 **strength_state** | [**List[str]**](str.md)|  | [optional] 
 **score_state** | **bool**|  | [optional] 
 **linemates** | **bool**|  | [optional] 
 **opposition** | **bool**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 10000]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**LinesSeasonResponse**](LinesSeasonResponse.md)

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

