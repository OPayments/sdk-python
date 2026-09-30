# opayments_sdk.PaymentApi

All URIs are relative to *https://api.opayments.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_sbp_payment**](PaymentApi.md#create_sbp_payment) | **POST** /payments/sbp | Создать платёж по СБП
[**create_tpay_payment**](PaymentApi.md#create_tpay_payment) | **POST** /payments/tpay | Создать платёж через T-Pay


# **create_sbp_payment**
> Payment create_sbp_payment(create_sbp_payment_request, idempotency_key=idempotency_key)

Создать платёж по СБП

### Example

* Api Key Authentication (RequestSignature):
* Api Key Authentication (ProjectIdentity):

```python
import opayments_sdk
from opayments_sdk.models.create_sbp_payment_request import CreateSbpPaymentRequest
from opayments_sdk.models.payment import Payment
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
    api_instance = opayments_sdk.PaymentApi(api_client)
    create_sbp_payment_request = opayments_sdk.CreateSbpPaymentRequest() # CreateSbpPaymentRequest | 
    idempotency_key = 'idempotency_key_example' # str |  (optional)

    try:
        # Создать платёж по СБП
        api_response = api_instance.create_sbp_payment(create_sbp_payment_request, idempotency_key=idempotency_key)
        print("The response of PaymentApi->create_sbp_payment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PaymentApi->create_sbp_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_sbp_payment_request** | [**CreateSbpPaymentRequest**](CreateSbpPaymentRequest.md)|  | 
 **idempotency_key** | **str**|  | [optional] 

### Return type

[**Payment**](Payment.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ранее созданный платёж СБП. |  * Location -  <br>  * X-Request-Id -  <br>  |
**201** | Платёж через СБП создан. |  * Location -  <br>  * X-Request-Id -  <br>  |
**400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
**401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
**403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
**409** | Запрос конфликтует с текущим состоянием ресурса. |  * X-Request-Id -  <br>  |
**415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
**429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
**502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
**503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  * Retry-After -  <br>  |
**504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_tpay_payment**
> Payment create_tpay_payment(create_tpay_payment_request, idempotency_key=idempotency_key)

Создать платёж через T-Pay

### Example

* Api Key Authentication (RequestSignature):
* Api Key Authentication (ProjectIdentity):

```python
import opayments_sdk
from opayments_sdk.models.create_tpay_payment_request import CreateTpayPaymentRequest
from opayments_sdk.models.payment import Payment
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
    api_instance = opayments_sdk.PaymentApi(api_client)
    create_tpay_payment_request = opayments_sdk.CreateTpayPaymentRequest() # CreateTpayPaymentRequest | 
    idempotency_key = 'idempotency_key_example' # str |  (optional)

    try:
        # Создать платёж через T-Pay
        api_response = api_instance.create_tpay_payment(create_tpay_payment_request, idempotency_key=idempotency_key)
        print("The response of PaymentApi->create_tpay_payment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PaymentApi->create_tpay_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_tpay_payment_request** | [**CreateTpayPaymentRequest**](CreateTpayPaymentRequest.md)|  | 
 **idempotency_key** | **str**|  | [optional] 

### Return type

[**Payment**](Payment.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ранее созданный платёж T-Pay. |  * Location -  <br>  * X-Request-Id -  <br>  |
**201** | Платёж через T-Pay создан. |  * Location -  <br>  * X-Request-Id -  <br>  |
**400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
**401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
**403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
**409** | Запрос конфликтует с текущим состоянием ресурса. |  * X-Request-Id -  <br>  |
**415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
**429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
**502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
**503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  * Retry-After -  <br>  |
**504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

