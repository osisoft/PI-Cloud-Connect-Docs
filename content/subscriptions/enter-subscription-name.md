---
uid: enter-subscription-name
---

# Enter subscription name

The Subscription name step allows you to add a name and description to your subscription. The subscription name will appear on your Subscription page and cannot be changed after the subscription is created. The description can be edited after the subscription is created.
 
**Note:** The default write mode of subscriptions is **Replace**, rather than **Insert**. **Replace** mode does not support compression of incoming event data. The following instructions show you how to retain compression of incoming data. However, if this change is causing complications to your operation, contact OSIsoft Technical Support and we can manually revert your subscription’s default setting to Insert.

## Procedure

1. Enter a name for the subscription.

1. Select the writing mode for the new subscription. To compress incoming data at the destination, you must select **Insert** for the writing mode, which causes buffering to mark incoming event data for compression. If you select **Replace** for the writing mode, buffering will not mark incoming data for compression.

   **Note:** Conversely, if you wish to utilize the **Replace** writing mode in the subscription, but still wish to compress incoming event data, you can compress data at the publication source rather than the subscription destination. Use the **Delay Publication** setting in the [Enter publication name](xref:enter-publication-name) portion of the Creating Publications section in this document.

1. Enter a Data Prefix (recommended). This feature enables users to distinguish between identically named PI Points and Digital State Sets from different publications. All PI Points and Digital State Sets included in the subscription will be prepended with the data prefix entered followed by a period. The data prefix must contain only alphanumeric characters and cannot be edited after the subscription is created. The data prefix does not apply to PI AF objects such as PI AF Templates.

1. Enter a Description (optional).

1. Review the subscription summary to ensure all information is accurate. To edit information, click the back arrow button at the bottom of the page.

1. Click the **checkmark button** at the bottom of the page to complete the subscription.
		 
	
	
 
