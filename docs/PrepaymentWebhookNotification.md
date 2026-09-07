# PrepaymentWebhookNotification


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**notification_id** | **UUID** |  | 
**notification_type** | **str** |  | 
**notification_date** | **datetime** |  | 
**payment** | [**PrepaymentPayment**](PrepaymentPayment.md) |  | 

## Example

```python
from opayments_sdk.models.prepayment_webhook_notification import PrepaymentWebhookNotification

# TODO update the JSON string below
json = "{}"
# create an instance of PrepaymentWebhookNotification from a JSON string
prepayment_webhook_notification_instance = PrepaymentWebhookNotification.from_json(json)
# print the JSON string representation of the object
print(PrepaymentWebhookNotification.to_json())

# convert the object into a dict
prepayment_webhook_notification_dict = prepayment_webhook_notification_instance.to_dict()
# create an instance of PrepaymentWebhookNotification from a dict
prepayment_webhook_notification_from_dict = PrepaymentWebhookNotification.from_dict(prepayment_webhook_notification_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


