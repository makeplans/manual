---
title: "Link straight to the reservation form"
description: "Send customers directly to the reservation form for a chosen service and time, from your own date picker, an email or a website."
nav_order: 12
redirect_from:
  - /article/68-link-to-booking-form-from-external-datepicker
verified: 2026-11-23
---

# Link straight to the reservation form

If you show available times yourself, for example with the API on your own website, you can link the customer straight to the reservation form with the service and time already chosen.

Use this address on your booking site:

```
/bookings/new?booking[service_id]=X&booking[booked_from]=TIME
```

| Part | Value |
|---|---|
| `booking[service_id]` | The number of the service, as shown in its address in setup. |
| `booking[booked_from]` | The start time in ISO 8601 format without time zone, such as `2026-12-01T10:00:00`. The time is read in the time zone of your account. |

Example:

```
https://youraccount.makeplans.com/bookings/new?booking[service_id]=12&booking[booked_from]=2026-12-01T10:00:00
```

The link uses the normal booking site, so the customer can only do what they could do there. A time that is not available cannot be booked this way.

More about the fields of a reservation is in the [API documentation](https://developer.makeplans.com).
