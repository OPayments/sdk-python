# PrepaymentPayment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_id** | **UUID** |  | 
**order_id** | **str** |  | 
**amount** | **int** | Сумма в копейках. | 
**currency** | **str** |  | 
**description** | **str** |  | [optional] 
**payment_method** | **str** |  | 
**status** | **str** |  | 
**payment_url** | **str** | Адрес оплаты для платежа в статусе pending. | [optional] 
**failure_code** | **str** |  | [optional] 
**failure_message** | **str** | Нормализованное сообщение, безопасное для показа мерчанту; никогда не содержит сырой ответ провайдера, credentials или данные карты. | [optional] 
**refund_summary** | [**RefundSummary**](RefundSummary.md) |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from opayments_sdk.models.prepayment_payment import PrepaymentPayment

# TODO update the JSON string below
json = "{}"
# create an instance of PrepaymentPayment from a JSON string
prepayment_payment_instance = PrepaymentPayment.from_json(json)
# print the JSON string representation of the object
print(PrepaymentPayment.to_json())

# convert the object into a dict
prepayment_payment_dict = prepayment_payment_instance.to_dict()
# create an instance of PrepaymentPayment from a dict
prepayment_payment_from_dict = PrepaymentPayment.from_dict(prepayment_payment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


