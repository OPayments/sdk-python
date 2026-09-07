# opayments_sdk.BalanceApi

All URIs are relative to *https://api.opayments.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_balance**](BalanceApi.md#get_balance) | **GET** /balance | Получить баланс


# **get_balance**
> Balance get_balance()

Получить баланс

Возвращает текущий баланс проекта.

### Example

* Api Key Authentication (RequestSignature):
* Api Key Authentication (ProjectIdentity):

```python
import opayments_sdk
from opayments_sdk.models.balance import Balance
from opayments_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.opayments.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = opayments_sdk.Configuration(
    host = "https://api.opayments.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: RequestSignature
configuration.api_key['RequestSignature'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['RequestSignature'] = 'Bearer'

# Configure API key authorization: ProjectIdentity
configuration.api_key['ProjectIdentity'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ProjectIdentity'] = 'Bearer'

# Enter a context with an instance of the API client
with opayments_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = opayments_sdk.BalanceApi(api_client)

    try:
        # Получить баланс
        api_response = api_instance.get_balance()
        print("The response of BalanceApi->get_balance:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BalanceApi->get_balance: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**Balance**](Balance.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Баланс проекта. |  * X-Request-Id -  <br>  |
**400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
**401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
**429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
**503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

