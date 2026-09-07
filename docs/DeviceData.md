# DeviceData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_type** | **str** |  | [optional] 
**os** | **str** |  | [optional] 
**browser** | **str** |  | [optional] 
**language** | **str** |  | [optional] 
**timezone_name** | **str** |  | [optional] 
**user_agent** | **str** |  | [optional] 

## Example

```python
from opayments_sdk.models.device_data import DeviceData

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceData from a JSON string
device_data_instance = DeviceData.from_json(json)
# print the JSON string representation of the object
print(DeviceData.to_json())

# convert the object into a dict
device_data_dict = device_data_instance.to_dict()
# create an instance of DeviceData from a dict
device_data_from_dict = DeviceData.from_dict(device_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


