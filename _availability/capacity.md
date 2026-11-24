---
title: "Resource capacity"
description: "Let a resource take several reservations or several people at the same time."
nav_order: 6
redirect_from:
  - /article/35-resource-capacity
verified: 2026-11-23
review: needs-espen
---

# Resource capacity

By default a resource has a capacity of 1: one reservation for one person fills a time. Raise the capacity when a resource can serve several reservations or several people at once, such as a room with 20 seats.

## Set the capacity

1. Open setup, select **Resources** and select the pencil next to the resource.
2. Enter the number in **Max number of reservations at the same time**.
3. Select **Save resource**.

With a capacity of 5, five customers can each book the same time.

## Several people in one reservation

How many people one reservation can include is set on the service, in **Max number of people allowed per reservation**. Each person uses one place of the resource's capacity.

| Capacity | People per reservation | A time is full with |
|---|---|---|
| 4 | up to 4 | one reservation for 4 people |
| 5 | up to 5 | five reservations for 1, or one for 2 and one for 3 |
| 20 | up to 4 | five reservations for 4, or twenty for 1 |

## One reservation takes the whole resource

To make a single reservation fill the resource regardless of how many people it includes, edit the service and tick **Reservation will block resource**.

## Related

- [Daily workload points]({% link _availability/workload-points.md %})
- [How available times are generated]({% link _availability/slot-generation.md %})
