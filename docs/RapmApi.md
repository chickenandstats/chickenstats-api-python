# chickenstats_api.RapmApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**read_rapm**](RapmApi.md#read_rapm) | **GET** /api/v1/chicken_nhl/rapm | Read Rapm


# **read_rapm**
> RapmResponse read_rapm(season=season, sessions=sessions, api_id=api_id, name=name, team=team, situation=situation, limit=limit, offset=offset)

Read Rapm

### Example


```python
import chickenstats_api
from chickenstats_api.models.rapm_response import RapmResponse
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.chickenstats.com
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "https://api.chickenstats.com"
)


# Enter a context with an instance of the API client
with chickenstats_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = chickenstats_api.RapmApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    api_id = [56] # List[int] |  (optional)
    name = ['name_example'] # List[str] |  (optional)
    team = ['team_example'] # List[str] |  (optional)
    situation = ['situation_example'] # List[str] |  (optional)
    limit = 10000 # int |  (optional) (default to 10000)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Read Rapm
        api_response = api_instance.read_rapm(season=season, sessions=sessions, api_id=api_id, name=name, team=team, situation=situation, limit=limit, offset=offset)
        print("The response of RapmApi->read_rapm:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RapmApi->read_rapm: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **season** | [**List[int]**](int.md)|  | [optional] 
 **sessions** | [**List[str]**](str.md)|  | [optional] 
 **api_id** | [**List[int]**](int.md)|  | [optional] 
 **name** | [**List[str]**](str.md)|  | [optional] 
 **team** | [**List[str]**](str.md)|  | [optional] 
 **situation** | [**List[str]**](str.md)|  | [optional] 
 **limit** | **int**|  | [optional] [default to 10000]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**RapmResponse**](RapmResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

