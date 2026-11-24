---
title: "Google Tag Manager"
description: "Load your Google Tag Manager container on the booking site and use the booking events as triggers."
nav_order: 17
redirect_from:
  - /article/25-google-tag-manager
verified: 2026-11-23
review: needs-espen
---

# Google Tag Manager

MakePlans can load your Google Tag Manager container on the booking site and push events to the dataLayer as customers book. Use them as triggers for Google Ads, Meta Pixel or other tags.

## Set it up

1. Find your container ID in Google Tag Manager. See [Google's guide](https://support.google.com/tagmanager/answer/6103696).
2. In MakePlans, open setup and select **Booking site**, then **General**.
3. Paste it in **Google Tag Manager container ID** and select **Save**.

You enter the ID only, not the code snippet.

## Nothing reaches Google Analytics on its own

The dataLayer is a queue on the page. Events only go further if your container forwards them. Your container needs:

1. A Google tag with your GA4 measurement ID.
2. A Custom Event trigger for each event name.
3. A GA4 Event tag for each trigger, with the fields you want as parameters.

If no data shows up in Google Analytics, the container is almost always the missing piece. If an agency runs your container, send them this page.

## The events

| Event | When | Fields |
|---|---|---|
| `view_slots` | A visitor sees available times | `service_id`, `service_title`, `selected_resource_ids`, `selected_resource_titles`, `slots_available`, `from_date`, `to_date` |
| `view_available_dates` | A visitor sees the calendar of dates | As above, with `dates_available` instead of `slots_available` |
| `no_availability` | Nothing was free | As the view the visitor was on, plus `next_available_date` and `days_to_next_available` |
| `booking_completed` | A reservation was completed | `booking_id`, `booking_title`, `booking_count`, `resource_id`, `resource_title` |
| `sign_up` | A new customer registered | None |
| `login` | An existing customer logged in | None |
| `purchase` | A payment was made | `transaction_id`, `value`, `currency`, `items` |

The resource fields on the availability events are only filled in when the visitor has chosen a resource. `sign_up` is not sent for customers you create yourself, and `login` is not sent when a customer is logged in automatically by a cookie.

`purchase` is pushed in Google's e-commerce format:

```json
{
  "event": "purchase",
  "ecommerce": {
    "value": 750.0,
    "currency": "NOK",
    "transaction_id": "order-321",
    "items": [
      {"item_id": "1201", "item_name": "Eye exam", "price": 750.0, "quantity": 1}
    ]
  }
}
```

In the GA4 tag for `purchase`, turn on **Send Ecommerce data** with the data layer as source. Always forward `transaction_id` unchanged, since Google Analytics uses it to avoid counting a purchase twice.

## Recommended setup

- Use `booking_completed` as your conversion. Mark it as a key event in Google Analytics and import it as a conversion in Google Ads.
- Trigger on the events, not on page addresses. The address of a service changes if you rename it.
- Consider merging `view_slots`, `view_available_dates` and `no_availability` into one event in Google Analytics, with a parameter that says whether anything was available. Then the share of visitors who found nothing free is a single number.

{% include alert.html type="warning" content="If you have entered both a Google Analytics ID and a Tag Manager ID in MakePlans, do not forward `booking_completed` from Tag Manager to Google Analytics. MakePlans sends it to Google Analytics directly, so it would be counted twice." %}

## Limits

- You only see which resource a visitor was interested in if they chose one. For completed reservations per resource, use `resource_title` on `booking_completed`.
- The events record which day a visitor looked at, not which time of day they wanted.
- A payment that is confirmed without the customer returning to the booking site does not send `purchase`.

## Sensitive information

Names of services and resources, which are often names of people, become data in your Google account. If you work in health or therapy, consider sending IDs instead of titles, and whether analytics belongs on your booking site at all. Google does not allow personal information in Analytics.

## Related

- [Google Analytics](/integrations/google-analytics/)
