# chickenstats_api.PlayersApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**read_player**](PlayersApi.md#read_player) | **GET** /api/v1/chicken_nhl/players/{api_id} | Read Player
[**read_players**](PlayersApi.md#read_players) | **GET** /api/v1/chicken_nhl/players | Read Players


# **read_player**
> PlayerPublic read_player(api_id)

Read Player

### Example


```python
import chickenstats_api
from chickenstats_api.models.player_public import PlayerPublic
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
    api_instance = chickenstats_api.PlayersApi(api_client)
    api_id = 56 # int | 

    try:
        # Read Player
        api_response = api_instance.read_player(api_id)
        print("The response of PlayersApi->read_player:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PlayersApi->read_player: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_id** | **int**|  | 

### Return type

[**PlayerPublic**](PlayerPublic.md)

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

# **read_players**
> PlayerResponse read_players(name=name, position=position, eh_id=eh_id, limit=limit, offset=offset)

Read Players

### Example


```python
import chickenstats_api
from chickenstats_api.models.player_response import PlayerResponse
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
    api_instance = chickenstats_api.PlayersApi(api_client)
    name = 'name_example' # str |  (optional)
    position = 'position_example' # str |  (optional)
    eh_id = 'eh_id_example' # str |  (optional)
    limit = 10000 # int |  (optional) (default to 10000)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Read Players
        api_response = api_instance.read_players(name=name, position=position, eh_id=eh_id, limit=limit, offset=offset)
        print("The response of PlayersApi->read_players:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PlayersApi->read_players: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**|  | [optional] 
 **position** | **str**|  | [optional] 
 **eh_id** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 10000]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**PlayerResponse**](PlayerResponse.md)

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

