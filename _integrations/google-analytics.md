---
title: "Google Analytics"
description: "Send visits and reservations on your booking site to Google Analytics."
nav_order: 16
redirect_from:
  - /article/24-google-analytics
verified: 2026-11-26
---

# Google Analytics

MakePlans can send visits and events from your booking site to your Google Analytics account. You only need your measurement ID.

## Set it up

1. In Google Analytics, select **Admin** and check that you are in the right account and property.
2. Under the property, select **Data streams** and open your data stream.
3. Copy the measurement ID.
4. In MakePlans, open setup and select **Booking site**, then **General**.
5. Paste it in **Google Analytics tracking ID** and select **Save**.

## What is tracked

The booking site sends page views and these events:

| Event | When |
|---|---|
| `view_slots` | A visitor sees available times for a service. |
| `view_available_dates` | A visitor sees the calendar of dates for a service. |
| `no_availability` | A visitor looked for a time or date and none was free. |
| `booking_completed` | A reservation was completed. |
| `sign_up` | A new customer registered. |
| `login` | An existing customer logged in. |
| `purchase` | A payment was made, with amount, currency and items, so revenue reports work. |

Free reservations, and reservations paid later or by invoice, send `booking_completed` only. After a paid checkout of a cart, `booking_completed` is sent once for each reservation in the order.

The events carry details such as the service, the chosen resource and the number of available times. See the [Tracking events reference]({% link _integrations/tracking-events.md %}) for every field.

## Get useful reports

- Mark `booking_completed` as a key event in Google Analytics. This is your conversion.
- To see which service and resource an event is about, register `service_title` and `selected_resource_titles` as event-scoped custom dimensions under **Admin**, **Custom definitions**. Do not register `booking_id` or `from_date`. They have too many different values to be useful.
- Check that `purchase` is marked as a key event too, if you take payment.

{% include alert.html type="warning" content="If you use both Google Analytics and Google Tag Manager in MakePlans, do not forward `booking_completed` from Tag Manager to Google Analytics. MakePlans already sends it directly, so every reservation would be counted twice." %}

## Why the numbers are lower than your reservations

Some browsers block tracking, so Google Analytics usually shows fewer reservations than you really have. Tracking is also less reliable when the booking site is shown in an iframe.

## Related

- [Google Tag Manager](/integrations/google-tag-manager/)
- [Tracking events reference]({% link _integrations/tracking-events.md %})
