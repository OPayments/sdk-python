# RefundPage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Refund]**](Refund.md) |  | 
**next_cursor** | **str** | Непрозрачный курсор следующей страницы. | 
**has_more** | **bool** |  | 

## Example

```python
from opayments_sdk.models.refund_page import RefundPage

# TODO update the JSON string below
json = "{}"
# create an instance of RefundPage from a JSON string
refund_page_instance = RefundPage.from_json(json)
# print the JSON string representation of the object
print(RefundPage.to_json())

# convert the object into a dict
refund_page_dict = refund_page_instance.to_dict()
# create an instance of RefundPage from a dict
refund_page_from_dict = RefundPage.from_dict(refund_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


