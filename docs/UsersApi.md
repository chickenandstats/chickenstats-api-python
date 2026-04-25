# chickenstats_api.UsersApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_user_me**](UsersApi.md#delete_user_me) | **DELETE** /api/v1/users/me | Delete User Me
[**get_programmatic_credentials**](UsersApi.md#get_programmatic_credentials) | **GET** /api/v1/users/me/programmatic-credentials | Get Programmatic Credentials
[**read_user_me**](UsersApi.md#read_user_me) | **GET** /api/v1/users/me | Read User Me
[**resend_verification**](UsersApi.md#resend_verification) | **POST** /api/v1/users/me/resend-verification | Resend Verification
[**rotate_programmatic_credentials**](UsersApi.md#rotate_programmatic_credentials) | **POST** /api/v1/users/me/programmatic-credentials/rotate | Rotate Programmatic Credentials
[**signup**](UsersApi.md#signup) | **POST** /api/v1/users/signup | Signup
[**sync_ghost_tier**](UsersApi.md#sync_ghost_tier) | **POST** /api/v1/users/me/sync-ghost | Sync Ghost Tier
[**update_password_me**](UsersApi.md#update_password_me) | **PATCH** /api/v1/users/me/password | Update Password Me
[**update_user_me**](UsersApi.md#update_user_me) | **PATCH** /api/v1/users/me | Update User Me


# **delete_user_me**
> Message delete_user_me()

Delete User Me

Delete own user and block Auth0 account.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.message import Message
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        api_response = api_instance.delete_user_me()
        print("The response of UsersApi->delete_user_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->delete_user_me: %s\n" % e)
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

# **get_programmatic_credentials**
> ProgrammaticCredentials get_programmatic_credentials()

Get Programmatic Credentials

Return the CF client ID for programmatic access. The secret is never retrievable —.

rotate credentials if the secret was lost.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.programmatic_credentials import ProgrammaticCredentials
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        # Get Programmatic Credentials
        api_response = api_instance.get_programmatic_credentials()
        print("The response of UsersApi->get_programmatic_credentials:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->get_programmatic_credentials: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ProgrammaticCredentials**](ProgrammaticCredentials.md)

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

# **read_user_me**
> UserPublic read_user_me()

Read User Me

Get current user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.user_public import UserPublic
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        api_response = api_instance.read_user_me()
        print("The response of UsersApi->read_user_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->read_user_me: %s\n" % e)
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

# **resend_verification**
> Message resend_verification()

Resend Verification

Trigger Auth0 to resend the verification email.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.message import Message
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        # Resend Verification
        api_response = api_instance.resend_verification()
        print("The response of UsersApi->resend_verification:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->resend_verification: %s\n" % e)
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

# **rotate_programmatic_credentials**
> ProgrammaticCredentials rotate_programmatic_credentials()

Rotate Programmatic Credentials

Delete the existing CF service token and issue a new one. The new secret is.

returned once in the response and optionally emailed. Store it immediately.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.programmatic_credentials import ProgrammaticCredentials
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        # Rotate Programmatic Credentials
        api_response = api_instance.rotate_programmatic_credentials()
        print("The response of UsersApi->rotate_programmatic_credentials:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->rotate_programmatic_credentials: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ProgrammaticCredentials**](ProgrammaticCredentials.md)

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

# **signup**
> UserPublic signup(user_register)

Signup

Public self-registration. Creates a local user, an Auth0 user, and a Ghost member.

If the account exists but is inactive (previously deactivated/pruned), reactivates it
with the new credentials rather than rejecting the request.

### Example


```python
import chickenstats_api
from chickenstats_api.models.user_public import UserPublic
from chickenstats_api.models.user_register import UserRegister
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with chickenstats_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = chickenstats_api.UsersApi(api_client)
    user_register = chickenstats_api.UserRegister() # UserRegister | 

    try:
        # Signup
        api_response = api_instance.signup(user_register)
        print("The response of UsersApi->signup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->signup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_register** | [**UserRegister**](UserRegister.md)|  | 

### Return type

[**UserPublic**](UserPublic.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sync_ghost_tier**
> Message sync_ghost_tier()

Sync Ghost Tier

Refresh tier from Ghost subscription state. No-op for contributor/superuser.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.message import Message
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        # Sync Ghost Tier
        api_response = api_instance.sync_ghost_tier()
        print("The response of UsersApi->sync_ghost_tier:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->sync_ghost_tier: %s\n" % e)
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

# **update_password_me**
> Message update_password_me(update_password)

Update Password Me

Update own password in Auth0. Verifies current password against Auth0 before changing.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import chickenstats_api
from chickenstats_api.models.message import Message
from chickenstats_api.models.update_password import UpdatePassword
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        api_response = api_instance.update_password_me(update_password)
        print("The response of UsersApi->update_password_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->update_password_me: %s\n" % e)
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

# **update_user_me**
> UserPublic update_user_me(user_update_me)

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

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "http://localhost"
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
        api_response = api_instance.update_user_me(user_update_me)
        print("The response of UsersApi->update_user_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->update_user_me: %s\n" % e)
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

