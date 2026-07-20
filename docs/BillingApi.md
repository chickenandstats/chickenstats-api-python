# chickenstats_api.BillingApi

All URIs are relative to *https://api.chickenstats.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_checkout_session**](BillingApi.md#create_checkout_session) | **POST** /api/v1/billing/checkout | Create Checkout Session
[**create_portal_session**](BillingApi.md#create_portal_session) | **POST** /api/v1/billing/portal | Create Portal Session


# **create_checkout_session**
> Dict[str, str] create_checkout_session(tier)

Create Checkout Session

Create a Stripe Checkout session for the given tier and return its URL.

Created via a direct server-side Stripe API call rather than the Firebase
extension's client-SDK pattern (Firestore-triggered function, meant for a
JS SPA) -- this project's frontend is server-rendered. The extension's
handleWebhookEvents function still processes the resulting
checkout.session.completed event and sets the stripeRole claim, since
Stripe fires the same webhook regardless of how the session was created.

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
    api_instance = chickenstats_api.BillingApi(api_client)
    tier = 'tier_example' # str | 

    try:
        # Create Checkout Session
        api_response = api_instance.create_checkout_session(tier)
        print("The response of BillingApi->create_checkout_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->create_checkout_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tier** | **str**|  | 

### Return type

**Dict[str, str]**

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

# **create_portal_session**
> Dict[str, Optional[str]] create_portal_session()

Create Portal Session

Create a Stripe customer billing-portal session and return its URL.

Finds the customer by email -- the Firebase extension already creates a
Stripe customer per Firebase user ("Sync new users to Stripe customers"),
so no separate customer-ID storage is needed here.

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
    api_instance = chickenstats_api.BillingApi(api_client)

    try:
        # Create Portal Session
        api_response = api_instance.create_portal_session()
        print("The response of BillingApi->create_portal_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->create_portal_session: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**Dict[str, Optional[str]]**

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

