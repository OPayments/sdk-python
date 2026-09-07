# PaymentList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Payment]**](Payment.md) |  | 
**next_cursor** | **str** |  | 
**has_more** | **bool** |  | 

## Example

```python
from opayments_sdk.models.payment_list import PaymentList

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentList from a JSON string
payment_list_instance = PaymentList.from_json(json)
# print the JSON string representation of the object
print(PaymentList.to_json())

# convert the object into a dict
payment_list_dict = payment_list_instance.to_dict()
# create an instance of PaymentList from a dict
payment_list_from_dict = PaymentList.from_dict(payment_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


