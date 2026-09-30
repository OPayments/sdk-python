# CreateTpayPaymentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **str** | Идентификатор заказа в системе мерчанта. | 
**amount** | **int** | Сумма в копейках. | 
**description** | **str** |  | [optional] 
**metadata** | [**TpayPaymentMetadata**](TpayPaymentMetadata.md) |  | 
**callback_url** | **str** | HTTPS-адрес для уведомлений о платеже. | 
**success_url** | **str** | HTTPS-адрес для успешной оплаты. | 
**failed_url** | **str** | HTTPS-адрес для отменённой оплаты. | 

## Example

```python
from opayments_sdk.models.create_tpay_payment_request import CreateTpayPaymentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateTpayPaymentRequest from a JSON string
create_tpay_payment_request_instance = CreateTpayPaymentRequest.from_json(json)
# print the JSON string representation of the object
print(CreateTpayPaymentRequest.to_json())

# convert the object into a dict
create_tpay_payment_request_dict = create_tpay_payment_request_instance.to_dict()
# create an instance of CreateTpayPaymentRequest from a dict
create_tpay_payment_request_from_dict = CreateTpayPaymentRequest.from_dict(create_tpay_payment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


