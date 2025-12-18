# chickenstats_api.TeamStatsApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chicken_nhl_create_team_stats**](TeamStatsApi.md#chicken_nhl_create_team_stats) | **POST** /api/v1/chicken_nhl/team_stats | Create Team Stats


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
    api_instance = chickenstats_api.TeamStatsApi(api_client)
    team_stats_create = chickenstats_api.TeamStatsCreate() # TeamStatsCreate | 

    try:
        # Create Team Stats
        api_response = api_instance.chicken_nhl_create_team_stats(team_stats_create)
        print("The response of TeamStatsApi->chicken_nhl_create_team_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TeamStatsApi->chicken_nhl_create_team_stats: %s\n" % e)
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

