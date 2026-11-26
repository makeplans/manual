---
title: "Delete old data"
description: "Delete old reservations and customers, once or automatically, to avoid keeping personal data longer than you need."
nav_order: 11
verified: 2026-11-23
---

# Delete old data

Privacy rules say you should not keep personal data longer than you need. MakePlans can delete old reservations and customers for you.

## Delete automatically

1. Open setup and select **Account**.
2. In **Automatic deletion of personal identifiable information**, write how old data must be before it is deleted, counted back from today. For example `6 months ago` or `2 years ago`.
3. Select **Save**.

Old customers and reservations are then deleted continuously.

## Delete once

1. Open setup and select **Tools**, then **Delete old data**.
2. Choose a date in **Delete data before date**.
3. Select **DELETE DATA**.

This deletes:

- all reservations that ended before the date
- all customers who have not been updated since before the date and have no reservations after it
- all logs and other information belonging to these

{% include alert.html type="warning" content="Deleted data cannot be brought back. Other systems you have connected through integrations are not told about the deletion." %}

## Related

- [GDPR and privacy]({% link _account/gdpr.md %})
