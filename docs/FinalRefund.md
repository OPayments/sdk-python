# FinalRefund


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
from opayments_sdk.models.final_refund import FinalRefund

# TODO update the JSON string below
json = "{}"
# create an instance of FinalRefund from a JSON string
final_refund_instance = FinalRefund.from_json(json)
# print the JSON string representation of the object
print(FinalRefund.to_json())

# convert the object into a dict
final_refund_dict = final_refund_instance.to_dict()
# create an instance of FinalRefund from a dict
final_refund_from_dict = FinalRefund.from_dict(final_refund_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


