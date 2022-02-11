---
uid: select-destination-system
---

# Select destination system

Select a destination system for the data in the subscription.

The Destination System step displays a list of the available AFserver.AFDatabase namespaces for each PI Connect node configured under your account. If a namespace is missing from the list then it is an indication that there is an issue either connecting to the PI Connect node from the cloud or connecting to PI AF from the PI Connect node. It is recommended that each subscription target a dedicated PI AF Database and be treated as read only to avoid potential conflicts with multiple subscriptions targeting the same AF Database. PI Point data for the Subscription will be written to the default PI Data Archive configured in PI System Explorer on the selected node. 

**Note:** You cannot subscribe data to the same PI Data Archive that the data was published from.

## Procedure

1. Select a destination.

1. Click the **arrow button** at the bottom of the screen.
