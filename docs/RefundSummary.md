# RefundSummary

Суммы принятых возвратов в минимальных единицах валюты платежа. Возвраты в статусе pending не уменьшают refundableAmount.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**refunded_amount** | **int** |  | 
**refundable_amount** | **int** |  | 
**refund_count** | **int** |  | 

## Example

```python
from opayments_sdk.models.refund_summary import RefundSummary

# TODO update the JSON string below
json = "{}"
# create an instance of RefundSummary from a JSON string
refund_summary_instance = RefundSummary.from_json(json)
# print the JSON string representation of the object
print(RefundSummary.to_json())

# convert the object into a dict
refund_summary_dict = refund_summary_instance.to_dict()
# create an instance of RefundSummary from a dict
refund_summary_from_dict = RefundSummary.from_dict(refund_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


