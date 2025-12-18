# chickenstats_api.LoginApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**login_login_access_token**](LoginApi.md#login_login_access_token) | **POST** /api/v1/login/access-token | Login Access Token
[**login_recover_password**](LoginApi.md#login_recover_password) | **POST** /api/v1/password-recovery/{email} | Recover Password
[**login_recover_password_html_content**](LoginApi.md#login_recover_password_html_content) | **POST** /api/v1/password-recovery-html-content/{email} | Recover Password Html Content
[**login_reset_password**](LoginApi.md#login_reset_password) | **POST** /api/v1/reset-password/ | Reset Password
[**login_test_token**](LoginApi.md#login_test_token) | **POST** /api/v1/login/test-token | Test Token


# **login_login_access_token**
> Token login_login_access_token(username, password, grant_type=grant_type, scope=scope, client_id=client_id, client_secret=client_secret)

Login Access Token

OAuth2 compatible token login, get an access token for future requests.

### Example


```python
import chickenstats_api
from chickenstats_api.models.token import Token
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
    api_instance = chickenstats_api.LoginApi(api_client)
    username = 'username_example' # str | 
    password = 'password_example' # str | 
    grant_type = 'grant_type_example' # str |  (optional)
    scope = '' # str |  (optional) (default to '')
    client_id = 'client_id_example' # str |  (optional)
    client_secret = 'client_secret_example' # str |  (optional)

    try:
        # Login Access Token
        api_response = api_instance.login_login_access_token(username, password, grant_type=grant_type, scope=scope, client_id=client_id, client_secret=client_secret)
        print("The response of LoginApi->login_login_access_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginApi->login_login_access_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**|  | 
 **password** | **str**|  | 
 **grant_type** | **str**|  | [optional] 
 **scope** | **str**|  | [optional] [default to &#39;&#39;]
 **client_id** | **str**|  | [optional] 
 **client_secret** | **str**|  | [optional] 

### Return type

[**Token**](Token.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login_recover_password**
> Message login_recover_password(email)

Recover Password

Password Recovery.

### Example


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


# Enter a context with an instance of the API client
with chickenstats_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = chickenstats_api.LoginApi(api_client)
    email = 'email_example' # str | 

    try:
        # Recover Password
        api_response = api_instance.login_recover_password(email)
        print("The response of LoginApi->login_recover_password:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginApi->login_recover_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **str**|  | 

### Return type

[**Message**](Message.md)

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

# **login_recover_password_html_content**
> str login_recover_password_html_content(email)

Recover Password Html Content

HTML Content for Password Recovery.

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
    api_instance = chickenstats_api.LoginApi(api_client)
    email = 'email_example' # str | 

    try:
        # Recover Password Html Content
        api_response = api_instance.login_recover_password_html_content(email)
        print("The response of LoginApi->login_recover_password_html_content:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginApi->login_recover_password_html_content: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **str**|  | 

### Return type

**str**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/html, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login_reset_password**
> Message login_reset_password(new_password)

Reset Password

Reset password.

### Example


```python
import chickenstats_api
from chickenstats_api.models.message import Message
from chickenstats_api.models.new_password import NewPassword
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
    api_instance = chickenstats_api.LoginApi(api_client)
    new_password = chickenstats_api.NewPassword() # NewPassword | 

    try:
        # Reset Password
        api_response = api_instance.login_reset_password(new_password)
        print("The response of LoginApi->login_reset_password:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginApi->login_reset_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_password** | [**NewPassword**](NewPassword.md)|  | 

### Return type

[**Message**](Message.md)

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

# **login_test_token**
> UserPublic login_test_token()

Test Token

Test access token.

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
    api_instance = chickenstats_api.LoginApi(api_client)

    try:
        # Test Token
        api_response = api_instance.login_test_token()
        print("The response of LoginApi->login_test_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginApi->login_test_token: %s\n" % e)
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

