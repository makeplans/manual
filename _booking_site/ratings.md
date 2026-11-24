---
title: "Ratings"
description: "Ask customers to rate their reservation with a link in a follow-up email, choose the rating scale and see the results."
nav_order: 14
verified: 2026-11-23
review: needs-espen
---

# Ratings

You can ask customers to rate their visit. They get a link in a follow-up email after the reservation, select a score, and the rating is saved on that reservation.

## Ask for a rating

Ratings are collected through a message template of the type follow up.

1. Open setup and select **Message templates**, then **New message template**.
2. Set **Message type** to **Follow up** and **Delivery type** to **Email**.
3. In **Deliver at**, write when to send it, counted from the end of the reservation. For example, `08:00 tomorrow` sends it at 8 AM the day after.
4. Enter a **Subject**.
5. Write the message in **Template** and include the rating link:

{% raw %}
```liquid
Hi {{ booking.person.name }},

Thank you for visiting us. How was your {{ booking.service.title }}?

Rate your visit: {{ booking.rating_link }}
```
{% endraw %}

6. To ask only after certain services, select them under **Services**. Otherwise the message is sent for all services.
7. Select **Save message template**.

Message templates are available when your account is activated. See [Notifications]({% link _notifications/overview.md %}).

## Choose the scale

1. Open setup and select **Booking site**, then **Rules**.
2. Choose a **Rating scale**, for example **1-5**. The default is 1 to 3.
3. Select **Save**.

{% include alert.html type="warning" content="Choose the scale before you start collecting ratings. Each rating is stored as the number the customer chose, so if you change the scale later, older ratings mean something else." %}

## See the ratings

Open **Reports** and select **Ratings**. The report shows the average rating per day, per resource and per service, how the scores are spread, how many customers responded, and the lowest rated reservations. See [Reports]({% link _bookings/reports.md %}).

## Related

- [Notifications]({% link _notifications/overview.md %})
