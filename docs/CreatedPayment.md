# CreatedPayment


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
**payment_url** | **str** |  | 
**failure_code** | **str** |  | [optional] 
**failure_message** | **str** | Нормализованное сообщение, безопасное для показа мерчанту; никогда не содержит сырой ответ провайдера, credentials или данные карты. | [optional] 
**refund_summary** | [**RefundSummary**](RefundSummary.md) |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from opayments_sdk.models.created_payment import CreatedPayment

# TODO update the JSON string below
json = "{}"
# create an instance of CreatedPayment from a JSON string
created_payment_instance = CreatedPayment.from_json(json)
# print the JSON string representation of the object
print(CreatedPayment.to_json())

# convert the object into a dict
created_payment_dict = created_payment_instance.to_dict()
# create an instance of CreatedPayment from a dict
created_payment_from_dict = CreatedPayment.from_dict(created_payment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


