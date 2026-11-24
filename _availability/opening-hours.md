---
title: "Opening hours"
description: "Set default opening hours per resource, add breaks, change hours for specific dates and open only on certain dates."
nav_order: 4
redirect_from:
  - /article/9-defining-opening-hours
  - /article/29-bookings-within-a-limited-timeframe
verified: 2026-11-23
review: needs-espen
---

# Opening hours

Availability on the booking site is defined by the opening hours of your resources. There are two layers:

- **Default availability** on the resource applies to every week.
- **Adjusted availability** in the calendar applies only to the dates you change.

## Default availability

1. Open setup and select **Resources**.
2. Select the pencil next to the resource.
3. Under **Default availability**, tick each day the resource is open and enter **From** and **To**.
4. Select **Save resource**.

A new resource is open Monday to Friday, 09:00 to 17:00.

## Breaks

To make part of a day unavailable, give the day more than one period. Select **+ and** below the day and enter the next period.

For example, 09:00 to 12:00 and 12:30 to 15:00 closes the resource between 12:00 and 12:30. You can add as many periods as you need.

## Different hours on specific dates

1. Open the **Calendar** and go to the week you want to change.
2. Select the clock button, **Adjust availability for this period**.
3. Find the resource and the date. Clear **Open** to close the day, or change **From** and **To**.
4. Select **Save**.

{% include figure.html src="/assets/images/availability/opening-hours/01-adjust-availability.webp" alt="The Adjust availability form with one row per resource and one column per day" caption="Here Sam Taylor closes at 13:00 on Thursday and is closed on Friday. Priya Shah keeps the default hours." %}

Only the dates you changed are affected. All other weeks keep the default availability.

Each resource row also has two shortcuts:

- **Closed all period** closes the resource on every day shown.
- **Reset** puts the resource back to its default availability for the period, if you change your mind.

Select **+ add** on a day to give it a second period, and **remove** to take one away.

## Open only on certain dates

Use this when a service can be booked only during a limited period, such as meetings during a two-day conference.

1. Create a resource for each person or room that can be booked.
2. In **Default availability**, clear every weekday so the resource is closed by default.
3. Create a service and tick those resources.
4. In the **Calendar**, go to the week you want to open and select the clock button.
5. Tick **Open** and set the hours for the dates you want, then select **Save**.

Customers who select the service can book only on the dates you opened.

## Different hours for one service

Opening hours on a resource apply to every service it offers. To give one service its own hours, such as a service offered Monday to Wednesday only, see [Different opening hours for one service]({% link _services/provider-availability.md %}).

## Related

- [Vacations, holidays and blocking dates]({% link _availability/time-off.md %})
- [How available times are generated]({% link _availability/slot-generation.md %})
