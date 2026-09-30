# opayments_sdk.PaymentsApi

All URIs are relative to *https://api.opayments.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_payment**](PaymentsApi.md#get_payment) | **GET** /payments/{paymentId} | Получить платёж
[**list_payments**](PaymentsApi.md#list_payments) | **GET** /payments | Найти платежи


# **get_payment**
> PaymentDetails get_payment(payment_id)

Получить платёж

### Example

* Api Key Authentication (RequestSignature):
* Api Key Authentication (ProjectIdentity):

```python
import opayments_sdk
from opayments_sdk.models.payment_details import PaymentDetails
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
    api_instance = opayments_sdk.PaymentsApi(api_client)
    payment_id = UUID('c9ee7c85-4cc0-494f-a0de-0af7257a66a6') # UUID | 

    try:
        # Получить платёж
        api_response = api_instance.get_payment(payment_id)
        print("The response of PaymentsApi->get_payment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PaymentsApi->get_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payment_id** | **UUID**|  | 

### Return type

[**PaymentDetails**](PaymentDetails.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Платёж. |  * X-Request-Id -  <br>  |
**400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
**401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
**404** | Ресурс не найден. |  * X-Request-Id -  <br>  |
**429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_payments**
> PaymentList list_payments(order_id=order_id, status=status, payment_method=payment_method, amount_from=amount_from, amount_to=amount_to, created_from=created_from, created_to=created_to, completed_from=completed_from, completed_to=completed_to, failure_code=failure_code, search=search, sort=sort, sort_direction=sort_direction, cursor=cursor, limit=limit)

Найти платежи

Возвращает список платежей проекта.

### Example

* Api Key Authentication (RequestSignature):
* Api Key Authentication (ProjectIdentity):

```python
import opayments_sdk
from opayments_sdk.models.payment_list import PaymentList
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
    api_instance = opayments_sdk.PaymentsApi(api_client)
    order_id = 'order_id_example' # str | Идентификатор заказа в системе мерчанта. (optional)
    status = ['status_example'] # List[str] |  (optional)
    payment_method = 'payment_method_example' # str |  (optional)
    amount_from = 56 # int | Не больше amountTo, если он передан. (optional)
    amount_to = 56 # int | Не меньше amountFrom, если он передан. (optional)
    created_from = '2013-10-20T19:20:30+01:00' # datetime | Не позже createdTo, если он передан. (optional)
    created_to = '2013-10-20T19:20:30+01:00' # datetime | Не раньше createdFrom, если он передан. (optional)
    completed_from = '2013-10-20T19:20:30+01:00' # datetime | Не позже completedTo, если он передан. (optional)
    completed_to = '2013-10-20T19:20:30+01:00' # datetime | Не раньше completedFrom, если он передан. (optional)
    failure_code = 'failure_code_example' # str | Нормализованный код причины платежа. (optional)
    search = 'search_example' # str | Поиск по paymentId, orderId и описанию платежа. (optional)
    sort = 'createdAt' # str |  (optional) (default to 'createdAt')
    sort_direction = 'desc' # str |  (optional) (default to 'desc')
    cursor = 'cursor_example' # str | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. (optional)
    limit = 20 # int | Количество записей в ответе. (optional) (default to 20)

    try:
        # Найти платежи
        api_response = api_instance.list_payments(order_id=order_id, status=status, payment_method=payment_method, amount_from=amount_from, amount_to=amount_to, created_from=created_from, created_to=created_to, completed_from=completed_from, completed_to=completed_to, failure_code=failure_code, search=search, sort=sort, sort_direction=sort_direction, cursor=cursor, limit=limit)
        print("The response of PaymentsApi->list_payments:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PaymentsApi->list_payments: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **str**| Идентификатор заказа в системе мерчанта. | [optional] 
 **status** | [**List[str]**](str.md)|  | [optional] 
 **payment_method** | **str**|  | [optional] 
 **amount_from** | **int**| Не больше amountTo, если он передан. | [optional] 
 **amount_to** | **int**| Не меньше amountFrom, если он передан. | [optional] 
 **created_from** | **datetime**| Не позже createdTo, если он передан. | [optional] 
 **created_to** | **datetime**| Не раньше createdFrom, если он передан. | [optional] 
 **completed_from** | **datetime**| Не позже completedTo, если он передан. | [optional] 
 **completed_to** | **datetime**| Не раньше completedFrom, если он передан. | [optional] 
 **failure_code** | **str**| Нормализованный код причины платежа. | [optional] 
 **search** | **str**| Поиск по paymentId, orderId и описанию платежа. | [optional] 
 **sort** | **str**|  | [optional] [default to &#39;createdAt&#39;]
 **sort_direction** | **str**|  | [optional] [default to &#39;desc&#39;]
 **cursor** | **str**| Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. | [optional] 
 **limit** | **int**| Количество записей в ответе. | [optional] [default to 20]

### Return type

[**PaymentList**](PaymentList.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Страница платежей. |  * X-Request-Id -  <br>  |
**400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
**401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
**403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
**429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

