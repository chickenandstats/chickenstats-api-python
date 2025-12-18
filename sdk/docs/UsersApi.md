# chickenstats_api.UsersApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**users_create_user**](UsersApi.md#users_create_user) | **POST** /api/v1/users/ | Create User
[**users_delete_user**](UsersApi.md#users_delete_user) | **DELETE** /api/v1/users/{user_id} | Delete User
[**users_delete_user_me**](UsersApi.md#users_delete_user_me) | **DELETE** /api/v1/users/me | Delete User Me
[**users_read_user_by_id**](UsersApi.md#users_read_user_by_id) | **GET** /api/v1/users/{user_id} | Read User By Id
[**users_read_user_me**](UsersApi.md#users_read_user_me) | **GET** /api/v1/users/me | Read User Me
[**users_read_users**](UsersApi.md#users_read_users) | **GET** /api/v1/users/ | Read Users
[**users_update_password_me**](UsersApi.md#users_update_password_me) | **PATCH** /api/v1/users/me/password | Update Password Me
[**users_update_user**](UsersApi.md#users_update_user) | **PATCH** /api/v1/users/{user_id} | Update User
[**users_update_user_me**](UsersApi.md#users_update_user_me) | **PATCH** /api/v1/users/me | Update User Me


# **users_create_user**
> UserPublic users_create_user(user_create)

Create User

Create new user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.user_create import UserCreate
from chickenstats_api.models.user_public import UserPublic
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
    api_instance = chickenstats_api.UsersApi(api_client)
    user_create = chickenstats_api.UserCreate() # UserCreate | 

    try:
        # Create User
        api_response = api_instance.users_create_user(user_create)
        print("The response of UsersApi->users_create_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_create_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_create** | [**UserCreate**](UserCreate.md)|  | 

### Return type

[**UserPublic**](UserPublic.md)

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

# **users_delete_user**
> Message users_delete_user(user_id)

Delete User

Delete a user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.message import Message
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
    api_instance = chickenstats_api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Delete User
        api_response = api_instance.users_delete_user(user_id)
        print("The response of UsersApi->users_delete_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_delete_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

### Return type

[**Message**](Message.md)

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

# **users_delete_user_me**
> Message users_delete_user_me()

Delete User Me

Delete own user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.message import Message
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
    api_instance = chickenstats_api.UsersApi(api_client)

    try:
        # Delete User Me
        api_response = api_instance.users_delete_user_me()
        print("The response of UsersApi->users_delete_user_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_delete_user_me: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**Message**](Message.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **users_read_user_by_id**
> UserPublic users_read_user_by_id(user_id)

Read User By Id

Get a specific user by id.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.user_public import UserPublic
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
    api_instance = chickenstats_api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Read User By Id
        api_response = api_instance.users_read_user_by_id(user_id)
        print("The response of UsersApi->users_read_user_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_read_user_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

### Return type

[**UserPublic**](UserPublic.md)

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

# **users_read_user_me**
> UserPublic users_read_user_me()

Read User Me

Get current user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.user_public import UserPublic
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
    api_instance = chickenstats_api.UsersApi(api_client)

    try:
        # Read User Me
        api_response = api_instance.users_read_user_me()
        print("The response of UsersApi->users_read_user_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_read_user_me: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**UserPublic**](UserPublic.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **users_read_users**
> UsersPublic users_read_users(skip=skip, limit=limit)

Read Users

Retrieve users.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.users_public import UsersPublic
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
    api_instance = chickenstats_api.UsersApi(api_client)
    skip = 0 # int |  (optional) (default to 0)
    limit = 100 # int |  (optional) (default to 100)

    try:
        # Read Users
        api_response = api_instance.users_read_users(skip=skip, limit=limit)
        print("The response of UsersApi->users_read_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_read_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **skip** | **int**|  | [optional] [default to 0]
 **limit** | **int**|  | [optional] [default to 100]

### Return type

[**UsersPublic**](UsersPublic.md)

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

# **users_update_password_me**
> Message users_update_password_me(update_password)

Update Password Me

Update own password.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.message import Message
from chickenstats_api.models.update_password import UpdatePassword
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
    api_instance = chickenstats_api.UsersApi(api_client)
    update_password = chickenstats_api.UpdatePassword() # UpdatePassword | 

    try:
        # Update Password Me
        api_response = api_instance.users_update_password_me(update_password)
        print("The response of UsersApi->users_update_password_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_update_password_me: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_password** | [**UpdatePassword**](UpdatePassword.md)|  | 

### Return type

[**Message**](Message.md)

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

# **users_update_user**
> UserPublic users_update_user(user_id, user_update)

Update User

Update a user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.user_public import UserPublic
from chickenstats_api.models.user_update import UserUpdate
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
    api_instance = chickenstats_api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 
    user_update = chickenstats_api.UserUpdate() # UserUpdate | 

    try:
        # Update User
        api_response = api_instance.users_update_user(user_id, user_update)
        print("The response of UsersApi->users_update_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_update_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 
 **user_update** | [**UserUpdate**](UserUpdate.md)|  | 

### Return type

[**UserPublic**](UserPublic.md)

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

# **users_update_user_me**
> UserPublic users_update_user_me(user_update_me)

Update User Me

Update own user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.user_public import UserPublic
from chickenstats_api.models.user_update_me import UserUpdateMe
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
    api_instance = chickenstats_api.UsersApi(api_client)
    user_update_me = chickenstats_api.UserUpdateMe() # UserUpdateMe | 

    try:
        # Update User Me
        api_response = api_instance.users_update_user_me(user_update_me)
        print("The response of UsersApi->users_update_user_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->users_update_user_me: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_update_me** | [**UserUpdateMe**](UserUpdateMe.md)|  | 

### Return type

[**UserPublic**](UserPublic.md)

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

