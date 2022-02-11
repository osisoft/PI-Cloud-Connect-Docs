---
uid: faq-publication
---

# Publication

## What is a publisher?
 
A publisher is the owner of data being sent to a publication queue with PI Cloud Connect.

## What AF objects are supported?
 
See [Supported AF objects](xref:support-af-objects).

## Are there Best Practices for using PI Cloud Connect?
 
See [Best practices](xref:best-practices).

## Are there restrictions on the amount of data I'm publishing?
 
See [Performance and throughput](xref:performance-and-throughput).

## Will I always know who has access to the data I publish?
 
Yes. A table on the Publication Details page displays a list of each user, whether they have accepted the invitation to subscribe, and whether they are receiving data.

## When I create a publication, will the publication start sending data right away?
 
No, the publication will not start sending data until it is started from the Publications page.

## How will I know that my publication is sending data?
 
The Status field on the Publication Details page indicates whether the publication is currently sending data, has been manually stopped, or has been started but is not sending data. If Status is Not Sending, contact [OSIsoft Technical Support](https://my.osisoft.com).

## How long does my data remain in the publication queue available to subscribers?
 
Data remains in the publication queue for six months. During each PI Cloud Connect release a checkpoint is created for all publication queues. At that time, data associated with a checkpoint from more than six months prior is purged.
