---
uid: best-practices
---

# Best practices

Please adhere to the following best practices to ensure optimum performance:

- Each subscription should target its own PI AF database and be treated as read-only.

- All objects included in PI Cloud Connect publications should only contain supported AF objects. See the [Supported AF objects](xref:supported-af-objects) section for more information.

- Ensure that the total events per second transmitted through a PI Connect node are within the recommendations for [Performance and throughput](xref:performance-and-throughput).

- Avoid potential circular publications and subscriptions. The destination `AFServer.AFDatabase` namespace pair for a subscription should never be the same `AFServer.AFDatabase` namespace pair of its publication. Also, the PI Data Archive for subscription data cannot be the same PI Data Archive that the data was Published from.
