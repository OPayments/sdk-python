# ErrorErrorDetailsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_field** | **str** |  | 
**code** | **str** |  | 
**message** | **str** |  | 

## Example

```python
from opayments_sdk.models.error_error_details_inner import ErrorErrorDetailsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ErrorErrorDetailsInner from a JSON string
error_error_details_inner_instance = ErrorErrorDetailsInner.from_json(json)
# print the JSON string representation of the object
print(ErrorErrorDetailsInner.to_json())

# convert the object into a dict
error_error_details_inner_dict = error_error_details_inner_instance.to_dict()
# create an instance of ErrorErrorDetailsInner from a dict
error_error_details_inner_from_dict = ErrorErrorDetailsInner.from_dict(error_error_details_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


