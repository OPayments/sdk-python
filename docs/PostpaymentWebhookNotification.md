# PostpaymentWebhookNotification


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**notification_id** | **UUID** |  | 
**notification_type** | **str** |  | 
**notification_date** | **datetime** |  | 
**payment** | [**FinalPayment**](FinalPayment.md) |  | 

## Example

```python
from opayments_sdk.models.postpayment_webhook_notification import PostpaymentWebhookNotification

# TODO update the JSON string below
json = "{}"
# create an instance of PostpaymentWebhookNotification from a JSON string
postpayment_webhook_notification_instance = PostpaymentWebhookNotification.from_json(json)
# print the JSON string representation of the object
print(PostpaymentWebhookNotification.to_json())

# convert the object into a dict
postpayment_webhook_notification_dict = postpayment_webhook_notification_instance.to_dict()
# create an instance of PostpaymentWebhookNotification from a dict
postpayment_webhook_notification_from_dict = PostpaymentWebhookNotification.from_dict(postpayment_webhook_notification_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


