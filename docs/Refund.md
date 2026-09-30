# Refund


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**refund_id** | **UUID** |  | 
**payment_id** | **UUID** |  | 
**amount** | **int** | Сумма в копейках. | 
**currency** | **str** |  | 
**status** | **str** |  | 
**reason_code** | [**RefundReason**](RefundReason.md) |  | [optional] 
**reason_comment** | **str** |  | [optional] 
**reason** | **str** |  | [optional] 
**failure_code** | **str** |  | [optional] 
**failure_message** | **str** |  | [optional] 
**accepted_at** | **datetime** |  | [optional] 
**declined_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from opayments_sdk.models.refund import Refund

# TODO update the JSON string below
json = "{}"
# create an instance of Refund from a JSON string
refund_instance = Refund.from_json(json)
# print the JSON string representation of the object
print(Refund.to_json())

# convert the object into a dict
refund_dict = refund_instance.to_dict()
# create an instance of Refund from a dict
refund_from_dict = Refund.from_dict(refund_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


