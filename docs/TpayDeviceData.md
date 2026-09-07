# TpayDeviceData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_type** | **str** |  | 
**os** | **str** |  | 
**browser** | **str** |  | 
**language** | **str** |  | [optional] 
**timezone_name** | **str** |  | [optional] 
**user_agent** | **str** |  | [optional] 

## Example

```python
from opayments_sdk.models.tpay_device_data import TpayDeviceData

# TODO update the JSON string below
json = "{}"
# create an instance of TpayDeviceData from a JSON string
tpay_device_data_instance = TpayDeviceData.from_json(json)
# print the JSON string representation of the object
print(TpayDeviceData.to_json())

# convert the object into a dict
tpay_device_data_dict = tpay_device_data_instance.to_dict()
# create an instance of TpayDeviceData from a dict
tpay_device_data_from_dict = TpayDeviceData.from_dict(tpay_device_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


