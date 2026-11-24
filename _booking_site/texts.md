---
title: "Texts on the booking site"
description: "Change the footer and the messages customers see when there are no free times, while they wait for approval and after they have booked."
nav_order: 7
verified: 2026-11-23
review: needs-espen
---

# Texts on the booking site

Open setup and select **Booking site**, then **Texts**. Empty fields use the standard text. Select **Save** when you are done.

{% include figure.html src="/assets/images/booking-site/texts/01-texts.webp" alt="The Booking site texts page" %}

| Field | Where customers see it |
|---|---|
| **Footer** | At the bottom of every page. |
| **Text displayed when there is no availability** | When a day or service has no free times. |
| **Text for fully booked slots** | On slots that are full, when the service displays occupied slots. |
| **Text for slots in the past** | On slots that have passed, when the service displays them. |
| **Text displayed when booking is waiting for confirmation** | After booking, when you [approve reservations manually]({% link _bookings/approve.md %}). |
| **Text displayed on confirmation page** | After a reservation is completed. |

The last two can include details from the reservation, such as the customer's name or the time, through merge fields. See the [custom messages documentation](https://github.com/makeplans/makeplans-custom-messages).

## Other texts

- **Text displayed before reservation form** is under **Booking site**, then **Forms**.
- **Text for slots with waitlist** is under **Booking site**, then **Rules**. See [Waitlist]({% link _services/waitlist.md %}).
- A service can have its own texts. See [Service form]({% link _services/service-form.md %}).

Some texts are not shown in every theme. See [Design]({% link _booking_site/design.md %}).
