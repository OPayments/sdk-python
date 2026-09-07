# opayments_sdk.RefundsApi

All URIs are relative to *https://api.opayments.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_payment_refund**](RefundsApi.md#create_payment_refund) | **POST** /payments/{paymentId}/refund | Создать возврат
[**get_payment_refund**](RefundsApi.md#get_payment_refund) | **GET** /payments/{paymentId}/refund | Получить возврат


# **create_payment_refund**
> Refund create_payment_refund(payment_id, create_refund_request)

Создать возврат

### Example

* Api Key Authentication (RequestSignature):
* Api Key Authentication (ProjectIdentity):

```python
import opayments_sdk
from opayments_sdk.models.create_refund_request import CreateRefundRequest
from opayments_sdk.models.refund import Refund
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
    api_instance = opayments_sdk.RefundsApi(api_client)
    payment_id = UUID('c9ee7c85-4cc0-494f-a0de-0af7257a66a6') # UUID | 
    create_refund_request = opayments_sdk.CreateRefundRequest() # CreateRefundRequest | 

    try:
        # Создать возврат
        api_response = api_instance.create_payment_refund(payment_id, create_refund_request)
        print("The response of RefundsApi->create_payment_refund:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RefundsApi->create_payment_refund: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payment_id** | **UUID**|  | 
 **create_refund_request** | [**CreateRefundRequest**](CreateRefundRequest.md)|  | 

### Return type

[**Refund**](Refund.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ранее созданный возврат с теми же параметрами. |  * Location -  <br>  * X-Request-Id -  <br>  |
**202** | Возврат принят в обработку. |  * Location -  <br>  * X-Request-Id -  <br>  |
**400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
**401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
**404** | Ресурс не найден. |  * X-Request-Id -  <br>  |
**409** | Параметры ранее созданного возврата отличаются. |  * X-Request-Id -  <br>  |
**415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
**422** | Операция невозможна в текущем статусе платежа. |  * X-Request-Id -  <br>  |
**429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
**500** | Внутренняя ошибка сервиса. |  * X-Request-Id -  <br>  |
**502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
**503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  |
**504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_payment_refund**
> Refund get_payment_refund(payment_id)

Получить возврат

### Example

* Api Key Authentication (RequestSignature):
* Api Key Authentication (ProjectIdentity):

```python
import opayments_sdk
from opayments_sdk.models.refund import Refund
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
    api_instance = opayments_sdk.RefundsApi(api_client)
    payment_id = UUID('c9ee7c85-4cc0-494f-a0de-0af7257a66a6') # UUID | 

    try:
        # Получить возврат
        api_response = api_instance.get_payment_refund(payment_id)
        print("The response of RefundsApi->get_payment_refund:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RefundsApi->get_payment_refund: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payment_id** | **UUID**|  | 

### Return type

[**Refund**](Refund.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Возврат. |  * X-Request-Id -  <br>  |
**400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
**401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
**404** | Возврат не найден. |  * X-Request-Id -  <br>  |
**429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

