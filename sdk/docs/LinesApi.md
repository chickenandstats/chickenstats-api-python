# chickenstats_api.LinesApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chicken_nhl_create_lines**](LinesApi.md#chicken_nhl_create_lines) | **POST** /api/v1/chicken_nhl/lines | Create Lines
[**chicken_nhl_read_lines_game_ids**](LinesApi.md#chicken_nhl_read_lines_game_ids) | **GET** /api/v1/chicken_nhl/lines/game_ids | Read Lines Game Ids
[**chicken_nhl_read_team_stats_game_ids**](LinesApi.md#chicken_nhl_read_team_stats_game_ids) | **GET** /api/v1/chicken_nhl/team_stats/game_ids | Read Team Stats Game Ids


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
    api_instance = chickenstats_api.LinesApi(api_client)
    lines_create = chickenstats_api.LinesCreate() # LinesCreate | 

    try:
        # Create Lines
        api_response = api_instance.chicken_nhl_create_lines(lines_create)
        print("The response of LinesApi->chicken_nhl_create_lines:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinesApi->chicken_nhl_create_lines: %s\n" % e)
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
    api_instance = chickenstats_api.LinesApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Lines Game Ids
        api_response = api_instance.chicken_nhl_read_lines_game_ids(season=season, sessions=sessions)
        print("The response of LinesApi->chicken_nhl_read_lines_game_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinesApi->chicken_nhl_read_lines_game_ids: %s\n" % e)
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
    api_instance = chickenstats_api.LinesApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)

    try:
        # Read Team Stats Game Ids
        api_response = api_instance.chicken_nhl_read_team_stats_game_ids(season=season, sessions=sessions)
        print("The response of LinesApi->chicken_nhl_read_team_stats_game_ids:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinesApi->chicken_nhl_read_team_stats_game_ids: %s\n" % e)
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

