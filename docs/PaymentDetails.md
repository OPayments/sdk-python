# PaymentDetails


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
**refunds** | [**List[Refund]**](Refund.md) | Устарело, так как список неограничен. Используйте GET /payments/{paymentId}/refunds. | [optional] 

## Example

```python
from opayments_sdk.models.payment_details import PaymentDetails

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDetails from a JSON string
payment_details_instance = PaymentDetails.from_json(json)
# print the JSON string representation of the object
print(PaymentDetails.to_json())

# convert the object into a dict
payment_details_dict = payment_details_instance.to_dict()
# create an instance of PaymentDetails from a dict
payment_details_from_dict = PaymentDetails.from_dict(payment_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


