# CreateRefundRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **int** | Сумма в копейках. | [optional] 
**reason** | **str** |  | [optional] 

## Example

```python
from opayments_sdk.models.create_refund_request import CreateRefundRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRefundRequest from a JSON string
create_refund_request_instance = CreateRefundRequest.from_json(json)
# print the JSON string representation of the object
print(CreateRefundRequest.to_json())

# convert the object into a dict
create_refund_request_dict = create_refund_request_instance.to_dict()
# create an instance of CreateRefundRequest from a dict
create_refund_request_from_dict = CreateRefundRequest.from_dict(create_refund_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


