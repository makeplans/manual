---
title: "Daily workload points"
description: "Limit how much demanding work a resource takes per day by giving services points and resources a daily maximum."
nav_order: 7
redirect_from:
  - /article/99-daily-workload-points
verified: 2026-11-26
---

# Daily workload points

Opening hours and capacity limit what can be booked at the same time. Workload points limit the total for a day. Use them when a person can only do so much of a demanding service per day, as with massage or physiotherapy.

You give each service a number of points and each resource a maximum per day. When a resource has used its points for a day, the booking site shows no more times for services that would exceed the maximum.

## Example

- Massage 30 min: 1 point
- Massage 60 min: 2 points
- The therapist: maximum 6 points per day

The therapist can then be booked for six 30-minute massages, three 60-minute massages, or a mix such as two of each.

## Set it up

1. Open setup, select **Services** and edit a service. Enter **Workload points**. The field is below the minimum and maximum number of people.
2. Open setup, select **Resources** and edit a resource. Enter **Max workload points per day**. The field is below the capacity.
3. Repeat for each service and resource you want to limit.

Both fields take whole numbers above 0. Leave a field empty to turn the limit off.

| Service points | Resource maximum | Result |
|---|---|---|
| Set | Set | The limit applies |
| Set | Empty | No limit |
| Empty | Set | No limit for that service. Its reservations use no points |
| Empty | Empty | No limit |

## How points are counted

- A reservation uses the service's points multiplied by the number of people. Two people on a 2-point service use 4 points.
- Points count on the day the reservation starts. A reservation that runs past midnight or over several days counts on its first day only.
- Confirmed reservations count. So do reservations waiting for confirmation, verification or payment, until they expire.
- Cancelled, declined and expired reservations do not count. Cancelling frees the points.
- The maximum is per resource. All services on the resource count against the same maximum.
- The limit is per day. There is no weekly or monthly limit.

## What customers see

- On a full day, a service that no longer fits shows no times. Services that still fit are shown.
- If the service displays occupied slots, for example because the waitlist is on, the times on a full day are shown as occupied and customers can join the waitlist.
- A customer moving a reservation sees no times on full days.
- A customer who tries to book a time on a full day anyway gets the usual message that the time is not available.

## What you see in the admin

The limit applies to reservations made on the booking site. You can still add and change reservations in the admin on a full day, in the same way as with capacity.

The overview of available times for a service in the admin hides full days, as the booking site does.

## API

Services have the field `workload_points` and resources the field `max_workload_points`. Both are `null` when not set, and both can be set through the API. See [Enable the API]({% link _integrations/api.md %}).

## Related

- [Resource capacity]({% link _availability/capacity.md %})
- [How available times are generated]({% link _availability/slot-generation.md %})
