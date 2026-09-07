# PendingRefund


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_id** | **UUID** |  | 
**amount** | **int** | Сумма в копейках. | 
**currency** | **str** |  | 
**status** | **str** |  | 
**reason** | **str** |  | [optional] 
**failure_code** | **str** |  | [optional] 
**failure_message** | **str** |  | [optional] 
**accepted_at** | **datetime** |  | [optional] 
**declined_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from opayments_sdk.models.pending_refund import PendingRefund

# TODO update the JSON string below
json = "{}"
# create an instance of PendingRefund from a JSON string
pending_refund_instance = PendingRefund.from_json(json)
# print the JSON string representation of the object
print(PendingRefund.to_json())

# convert the object into a dict
pending_refund_dict = pending_refund_instance.to_dict()
# create an instance of PendingRefund from a dict
pending_refund_from_dict = PendingRefund.from_dict(pending_refund_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


