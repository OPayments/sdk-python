# CreateSbpPaymentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **str** | Идентификатор заказа в системе мерчанта. | 
**amount** | **int** | Сумма в копейках. | 
**description** | **str** |  | [optional] 
**metadata** | [**PaymentMetadata**](PaymentMetadata.md) |  | 
**callback_url** | **str** | HTTPS-адрес для уведомлений о платеже. | 
**success_url** | **str** | HTTPS-адрес для успешной оплаты. | 
**failed_url** | **str** | HTTPS-адрес для отменённой оплаты. | 

## Example

```python
from opayments_sdk.models.create_sbp_payment_request import CreateSbpPaymentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSbpPaymentRequest from a JSON string
create_sbp_payment_request_instance = CreateSbpPaymentRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSbpPaymentRequest.to_json())

# convert the object into a dict
create_sbp_payment_request_dict = create_sbp_payment_request_instance.to_dict()
# create an instance of CreateSbpPaymentRequest from a dict
create_sbp_payment_request_from_dict = CreateSbpPaymentRequest.from_dict(create_sbp_payment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


