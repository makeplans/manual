---
title: "How available times are generated"
description: "What decides the times customers can choose on the booking site: opening hours, duration, slot generation, rounding, capacity and booking limits."
nav_order: 8
redirect_from:
  - /article/43-available-slots
verified: 2026-11-23
---

# How available times are generated

The times a customer can choose on the booking site are called slots. MakePlans works them out from the settings below. If the booking site shows times you did not expect, go through this list.

| Setting | Where | Effect |
|---|---|---|
| Opening hours | Resource, and adjusted dates in the calendar | Slots are only generated while a resource offering the service is open. See [Opening hours]({% link _availability/opening-hours.md %}). |
| Duration | Service | A new slot starts when the previous one ends. A 30-minute service gives a slot every 30 minutes. |
| Slot frequency | Service, **Available slot every** | Offers slots more or less often than the duration. See [Slot frequency]({% link _availability/slot-frequency.md %}). |
| Slot generation | Booking site rules, or per service | **Dynamic** or **Fixed**, explained below. |
| Rounding | Booking site rules, or per service | Moves the next slot to a round time, explained below. |
| Public holidays | Booking site rules | No slots on public holidays unless you turn this off. See [Vacations, holidays and blocking dates]({% link _availability/time-off.md %}). |
| Capacity | Resource | How many reservations fit in the same slot. See [Resource capacity]({% link _availability/capacity.md %}). |
| Workload points | Service and resource | A daily limit per resource. See [Daily workload points]({% link _availability/workload-points.md %}). |
| Booking limits | Booking site rules | The earliest and latest time customers can book. See [Limit how far ahead customers can book]({% link _availability/booking-window.md %}). |

## Dynamic and fixed slot generation

**Dynamic** is the default. Slots are generated from the time that is actually free, so a new slot starts right after an existing reservation ends.

**Fixed** always counts from the opening hour, so slots stay on the same grid all day.

Example: the resource is open 09:00 to 17:00, the service lasts 60 minutes, rounding is the closest half hour, and there is already a reservation from 10:30 to 11:30.

| | Slots offered |
|---|---|
| **Dynamic** | 09:00, 11:30, 12:30, 13:30, 14:30, 15:30 |
| **Fixed** | 09:00, 12:00, 13:00, 14:00, 15:00, 16:00 |

With **Dynamic**, the day continues from 11:30, right after the reservation. With **Fixed**, the slots stay on the hour, so 10:00 and 11:00 are lost and the next slot is 12:00.

To change it for all services, open setup, select **Booking site**, then **Rules**, and set **Generation of available slots**. To change it for one service, edit the service and set **Time generation**.

## Rounding

Rounding moves the next available slot forward to a round time. If a reservation ends at 14:50, the next slot can be offered at 15:00 instead.

The default is the closest half hour. The options are the closest hour, half hour, 20 minutes, quarter, 10 minutes or 5 minutes, or no rounding. No rounding is not recommended because it can produce slots at odd times.

To change it for all services, open setup, select **Booking site**, then **Rules**, and set **Default rounding to next available time for reservation**. To change it for one service, edit the service and set **Rounding for next available time**.

{% include alert.html type="tip" content="After you change these settings, open your booking site and check the times for a day that already has reservations." %}

## Related

- [Slot frequency]({% link _availability/slot-frequency.md %})
- [Buffer time between appointments]({% link _availability/buffer-time.md %})
