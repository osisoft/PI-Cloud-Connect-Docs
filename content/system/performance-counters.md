---
uid: performance-counters
---

# Performance counters

The following performance counters are created on the local machine where the PI Connect Windows service is installed for each PI Cloud Connect Publication and Subscription instance configured against the machine:

- `BytesReceivedRate`: This is a total of bytes received over a ten minute period. This performance counter applies to subscriptions.

- `BytesSentRate`: This is a total of the bytes sent over a ten minute period. This performance counter applies to publications.

- `Heartbeat`: This counter increments whenever a new `BytesReceivedRate` or `BytesSentRate` counter value is received.

Performance counters can be accessed from Windows Monitoring Tools and/or [PI Interface for Performance Monitor](https://docs.osisoft.com/bundle/pi-interface-for-performance-monitor/page/pi-interface-for-performance-monitor.html). Keep in mind when leveraging PI Cloud Connect performance counters:

- Performance counters will not be created until the PI Connect service has been started and running for approximately 10 minutes.

- All counters update approximately every 10 minutes.

- The `BytesReceivedRate` and `BytesSentRate` counters are an aggregate of two individual data streams: one for the PI Data Archive and one for the PI AF Server.

- If the PI Connect service, Publication, or Subscription for a performance counter are stopped, no new values are recorded. This means that the `BytesReceivedRate` and `BytesSentRate` will not record a value of zero, but instead it will flat line at the last recorded value and the `Heartbeat` counter will stop incrementing.
