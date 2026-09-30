# TpayPaymentMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ip** | **str** | IP-адрес плательщика: IPv4 или IPv6. | 
**device_data** | [**TpayDeviceData**](TpayDeviceData.md) |  | 

## Example

```python
from opayments_sdk.models.tpay_payment_metadata import TpayPaymentMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of TpayPaymentMetadata from a JSON string
tpay_payment_metadata_instance = TpayPaymentMetadata.from_json(json)
# print the JSON string representation of the object
print(TpayPaymentMetadata.to_json())

# convert the object into a dict
tpay_payment_metadata_dict = tpay_payment_metadata_instance.to_dict()
# create an instance of TpayPaymentMetadata from a dict
tpay_payment_metadata_from_dict = TpayPaymentMetadata.from_dict(tpay_payment_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


