---
title: "Buffer time between appointments"
description: "Leave time between appointments by setting slot frequency longer than the duration, or by using rounding and breaks."
nav_order: 10
redirect_from:
  - /article/92-buffer-time-between-appointments
verified: 2026-11-23
review: needs-espen
---

# Buffer time between appointments

MakePlans has no separate buffer setting. You create time between appointments with the slot frequency of the service.

## Use slot frequency

Set **Available slot every** on the service to a longer time than its duration. The difference is the buffer.

| Duration | Available slot every | Time between appointments |
|---|---|---|
| 45 minutes | 60 minutes | 15 minutes |
| 30 minutes | 60 minutes | 30 minutes |
| 40 minutes | 100 minutes | 60 minutes |

For example, with a 45-minute service and a slot every 60 minutes, a reservation from 09:30 to 10:15 makes 10:30 the next slot.

1. Open setup, select **Services** and edit the service.
2. Enter the minutes in **Available slot every**.
3. Select **Save service**.

Use settings that fit together for all services on the same resource. Otherwise the buffer will not be the same after every appointment.

## How rounding affects the buffer

Slot frequency is applied first, then [rounding]({% link _availability/slot-generation.md %}). If rounding is set to the closest hour, a slot that would start at 10:30 moves to 11:00. When you use slot frequency for buffers, choose a rounding that matches, such as the closest half hour.

Rounding alone can also act as a buffer. A 50-minute service rounded to the closest hour leaves 10 minutes after each appointment. A reservation you add yourself at an odd time, such as 09:05 to 10:00, can remove that gap.

## Other ways to keep time free

- Add breaks to the [opening hours]({% link _availability/opening-hours.md %}), for example 09:00 to 12:00 and 13:00 to 15:00.
- Enter the opening hours as blocks with pauses between them, such as 09:00 to 11:00 and 11:30 to 13:30.
- Add a **Busy** reservation when you need preparation time that varies from day to day.

After a change, check your booking site. If slots do not line up with existing reservations and opening hours, gaps shorter than the service can appear, and they cannot be booked.

## Related

- [Slot frequency]({% link _availability/slot-frequency.md %})
