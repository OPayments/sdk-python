# RefundWebhookNotification


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**notification_id** | **UUID** |  | 
**notification_type** | **str** |  | 
**notification_date** | **datetime** |  | 
**payment_id** | **UUID** |  | 
**refund** | [**FinalRefund**](FinalRefund.md) |  | 

## Example

```python
from opayments_sdk.models.refund_webhook_notification import RefundWebhookNotification

# TODO update the JSON string below
json = "{}"
# create an instance of RefundWebhookNotification from a JSON string
refund_webhook_notification_instance = RefundWebhookNotification.from_json(json)
# print the JSON string representation of the object
print(RefundWebhookNotification.to_json())

# convert the object into a dict
refund_webhook_notification_dict = refund_webhook_notification_instance.to_dict()
# create an instance of RefundWebhookNotification from a dict
refund_webhook_notification_from_dict = RefundWebhookNotification.from_dict(refund_webhook_notification_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


