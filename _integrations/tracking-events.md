---
title: "Tracking events reference"
description: "Every event the booking site sends to Google Analytics and Google Tag Manager: fields, when each event fires, a recommended container setup and reporting tips."
nav_order: 18
verified: 2026-11-26
---

# Tracking events reference

This page is for the person who sets up your Google Tag Manager container or Google Analytics reports. To turn tracking on, see [Google Analytics]({% link _integrations/google-analytics.md %}) or [Google Tag Manager]({% link _integrations/google-tag-manager.md %}).

The events and their fields are the same in both. With Google Tag Manager they are pushed to the dataLayer. With only Google Analytics they are sent to GA4 directly.

## When each event fires

| Event | Fires when |
|---|---|
| `view_slots` | The times page is shown with at least one bookable time. |
| `view_available_dates` | The calendar of dates is shown with at least one available day. |
| `no_availability` | A visitor looked for a time or date and none was available. It fires instead of the two events above when the count is 0. |
| `booking_completed` | A reservation was completed, on the confirmation page. After a paid checkout of a cart, it also fires on the order confirmation page, once per reservation in the order. |
| `sign_up` | A new customer registered, at their first booking or by registering. It does not fire on later bookings by the same customer, and never for customers created by staff. |
| `login` | An existing customer logged in with a code, a link or a third-party login. It does not fire when the customer is logged in automatically by a cookie. |
| `purchase` | A payment was captured. Free reservations, and reservations paid later or by invoice, never fire it. They fire `booking_completed` only. |

A new registration fires `sign_up` only, never both `sign_up` and `login`.

## Fields

All values are strings unless the table says otherwise. A field that can hold several values is one comma-separated string, because GA4 does not support lists as parameters. An empty string means the visitor has not filtered.

### view_slots

| Field | Example | Notes |
|---|---|---|
| `service_id` | `"1201"` | Stays the same if the service is renamed. |
| `service_title` | `"Eye exam"` | |
| `selected_resource_ids` | `"88"` or `""` | Only set when the visitor has filtered on a resource. |
| `selected_resource_titles` | `"Oslo clinic"` or `""` | Only set when the visitor has filtered on a resource. |
| `slots_available` | `3` (number) | Times shown in the date range on screen. |
| `from_date`, `to_date` | `"2026-09-14"` | The date range on screen. The two differ on calendar templates that show a week. |
| `next_available_date` | `"2026-10-02"` or `null` | Only set when nothing was available. |
| `days_to_next_available` | `18` (number) or `null` | `next_available_date` minus `from_date`, calculated for you. |

### view_available_dates

The same fields as `view_slots`, with `dates_available` instead of `slots_available`. `dates_available` is the number of days with availability. It counts days, not times, which is why it is a separate field.

### no_availability

The same fields as the view the visitor was on, with a count of 0. This is your signal that demand was higher than capacity.

### booking_completed

| Field | Example | Notes |
|---|---|---|
| `booking_id` | `4711` (number) | |
| `booking_title` | `"Eye exam"` | |
| `booking_count` | `1` (number) | The number of people, usually 1. |
| `resource_id` | `"88"` | The resource that was booked. |
| `resource_title` | `"Oslo clinic"` | The resource that was booked. |

### sign_up and login

No fields. No customer details are sent.

### purchase

| Field | Example | Notes |
|---|---|---|
| `transaction_id` | `"booking-4711"` or `"order-321"` | GA4's standard transaction field. |
| `value` | `750` (number) | The amount paid, in main currency units: 750 means 750 kroner, not 750 øre. |
| `currency` | `"NOK"` | ISO 4217 code. |
| `items` | list | GA4's standard e-commerce items, one per order line, each with `item_id` (the service ID, a string), `item_name` (the service title), `price` (unit price, a number) and `quantity` (a number). A single reservation sends one item. A cart sends one per order line, including products and gift cards. |

Because `purchase` has `value`, `currency` and `items`, GA4's revenue and item reports work without further setup.

With Google Tag Manager, `purchase` is the one event pushed in GA4's nested e-commerce format. All other events are flat. See the example in [Google Tag Manager]({% link _integrations/google-tag-manager.md %}). With only Google Analytics, the same fields are sent as event parameters.

Always forward `transaction_id` unchanged. GA4 uses it to avoid counting a purchase twice, for example when a customer opens the payment page of a paid reservation again. This applies to revenue and purchase counts. Raw event counts, in Realtime and BigQuery, still show every firing.

Check that `purchase` is marked as a key event in GA4 under **Admin**, **Events**. It usually is, but not always.

## Recommended container setup

In your container you decide what each dataLayer event is called in GA4. We suggest this:

| dataLayer event | GA4 event | Parameters |
|---|---|---|
| `view_slots` | `availability_checked` | `availability_status`: `"available"`, `availability_count` from `slots_available`, `service_title`, `selected_resource_titles` |
| `view_available_dates` | `availability_checked` | `availability_status`: `"available"`, `availability_count` from `dates_available`, `service_title`, `selected_resource_titles` |
| `no_availability` | `availability_checked` | `availability_status`: `"unavailable"`, `days_to_next_available`, `service_title`, `selected_resource_titles` |
| `booking_completed` | `booking_completed` | `resource_title`, `booking_title`, `booking_count` |
| `sign_up`, `login`, `purchase` | Unchanged | All fields. These are already standard GA4 event names. For `purchase`, turn on **Send Ecommerce data** with the data layer as source. No parameters need mapping by hand. |

The only rename is merging the three availability events into one, `availability_checked`. With one event and an `availability_status` parameter, the share of checks that found nothing is a single number you can chart and use in funnels.

To do the merge with one trigger:

1. Create a Custom Event trigger with **Use regex matching** and the event name `^(view_slots|view_available_dates|no_availability)$`.
2. Create a Lookup Table variable on the built-in Event variable that sets `availability_status`.

Three separate triggers and tags work just as well, if you prefer something simpler.

Mark `booking_completed` as a key event in GA4. If you use Google Ads, import it as a conversion. The category **Book appointment** fits.

{% include alert.html type="warning" content="If you have entered both a Google Analytics ID and a Tag Manager ID in MakePlans, do not forward `booking_completed` from Tag Manager to Google Analytics. On the confirmation page MakePlans sends it to Google Analytics directly, so it would be counted twice. On the order confirmation page after a paid cart it is sent one way only, so this does not apply there." %}

## Tracking by page address

If you prefer triggers on page addresses, most steps can be recognised from the address alone:

| Step | Address |
|---|---|
| List of services | `/services`, and `/categories/<id>-<slug>/services` on accounts with categories. Cover both. |
| Times for a service | `/services/<id>-<slug>/slots?selected_resources=<id>&from=<date>` |

- Read `selected_resources` with Tag Manager's built-in URL variable, component type **Query**.
- Get the service ID from the path with the regular expression `^/services/(\d+)`.

Never match on the slug. It changes when a service is renamed. IDs also need a lookup table you maintain yourself to be readable in reports. The events carry titles to save you that work.

## Reports in GA4

- Custom parameters only show up in reports after you register them as event-scoped custom dimensions under **Admin**, **Custom definitions**. Register `service_title`, `selected_resource_titles` and `availability_status`.
- Do not register `booking_id`, `from_date` or other fields with a great many different values.
- Use closed funnels in Funnel explorations for completion rates. Open funnels make the rates look better than they are.
- Compare locations with rates, such as the share of views with no availability, and with unique users. Do not compare raw event counts. One visitor paging through empty weeks fires `no_availability` many times.

## Your own JavaScript

{% raw %}You can still add your own JavaScript to the booking site with the `{% script %}` tag.{% endraw %} See [Security]({% link _account/security.md %}).

{% include alert.html type="warning" content="If you earlier added your own `dataLayer.push` to the no-availability text to track empty days, remove it. Otherwise `no_availability` fires twice." %}

## Related

- [Google Analytics]({% link _integrations/google-analytics.md %})
- [Google Tag Manager]({% link _integrations/google-tag-manager.md %})
