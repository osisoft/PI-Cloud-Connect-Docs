---
uid: set-publishing-options
---

# Set publishing options

Include historical data that is available up to 30 days prior to the start of the publication.

The Publication Options step allows you to retrieve historical data that is available prior to the time the publication is started. A value from 0 to 30 can be entered to specify minutes, hours, or days. This setting only applies to the time series data for PI AF Attributes referencing PI Points and not PI AF objects. The start time for the publication data will be the same for all subscribers regardless of when a subscription is started.
 
An option to Delay Data forces the publication to wait for a specified time period before sending data. With this option, the publication scans the PI Data Archive directly, bypassing snapshot updates. As a result, the data sent is compressed on the publication PI Data Archive. Additionally, out-of-order events arriving past the delay interval will not be sent. Future data points are not supported with this option.

**Note:** During each PI Cloud Connect release a checkpoint is created for all publication queues. At that time, data associated with a checkpoint from more than six months prior is purged. This will change the start time for the publication data received by subscribers once a publication has been active for longer than six months.

## Procedure

1. Enter a time duration value (e.g., 7, 24, 30) and type (e.g., minutes, hours, days).

1. Select **Delay Data** to have the publication access event data from the Data Archive, which will mark it for compression. Deselect **Delay Data** to have the publication access event data from Snapshot, resulting in no compression of event data.

   **Note**: If the Delay Data option is not selected, the publication signs up for both snapshot and archive change events for the PI points referenced in the publication's AF attributes. If the publisher receives out-of-order events for these PI points, these events will be published even if their timestamps are prior to the publication start time.

1. Click the **arrow button** at the bottom of the screen.
