---
uid: faq-subscription
---

# Subscription

## What is a subscriber?
 
A subscriber is a user who has configured a subscription to receive PI Cloud Connect data.

## What if I subscribe to identical PI Points from multiple publications?
 
When creating a subscription you can add a unique alphanumeric prefix to the PI Points in the subscription. See [Enter subscription name](xref:enter-subscription-name) for more information.

## Should I create a special place in my AF element hierarchy for the content I subscribe to? How should I structure that?
 
For each subscription, you should use a separate PI AF Database.

## Does it cause problems if the PI AF structure of the publisher does not match that of the subscriber?
 
When you set up a subscription, you create a copy of the PI AF scope that the publisher is sharing, so you do not need to create your own hierarchy first. Additionally, PI AF databases for PI Cloud Connect subscriptions should be treated as read only.

## Is only one subscription allowed for each publication?
 
You can grant multiple users access to a single publication. This way, a single publication can be consumed by multiple subscribers at the same time.

## Can I make changes to the PI AF metadata that I am subscribed to? If yes, do my edits alter the publisher's source content?
 
You should not make any changes to the PI AF metadata you receive as a subscriber. PI Cloud Connect enables you to maintain a copy of the data that is being published; it is not intended to merge data. However, if you make edits to the PI AF metadata by mistake, it will not affect the publisher's original data, and the next time the publisher modifies the PI AF object, your subscription will be ‘corrected’. You can use standard AF tools to link and re-organize the data copied in a different database.

## Does subscribed content look any different than other content in my PI AF hierarchy?
 
It does not look any different. For each subscription, you might want to put subscribed content under a specifically labeled element in your PI AF structure so that you can easily find it. You can also put this content in a different PI AF database.

## Are there restrictions on what types of objects I can subscribe to?
 
You can receive any objects that are included in the publication, but not all PI AF objects are supported. Please see [Supported AF objects](xref:supported-af-objects) for information on supported PI AF objects.

## How do I know if my subscription is receiving data?
 
The Subscriptions and Publication Details pages display two fields that provide visibility into subscription data. The Status field indicates whether the subscription is currently receiving data, has been manually stopped, or is not receiving data. This field is automatically updated with a refresh rate of every 10 minutes. The Receiving Progress bar is a field that indicates the percentage of total bytes currently received from a publication for a subscription. The progress bar can be manually refreshed at a rate of once per minute.

If the Status is Not Receiving, or if the Receiving Progress bar is not incrementing, contact [OSIsoft Technical Support](https://my.osisoft.com).

## When I create a subscription, will I receive data from that point on or will older data also be included?
 
The start time for subscription data will be at most 6 months prior, equal to either the start time of the publication or six months ago (whichever is more recent.) During each PI Cloud Connect release a checkpoint is created for all Publication queues. At that time, data associated with a checkpoint older than six months is purged.
