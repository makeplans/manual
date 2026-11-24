---
title: "Create a reservation"
description: "Add a reservation for a customer in the admin, block time with a busy reservation, and repeat a reservation."
nav_order: 3
verified: 2026-11-23
---

# Create a reservation

Customers make most reservations themselves on the booking site. You add one in the admin when a customer calls, emails or books at the counter.

1. Open the **Calendar** or the **Agenda** and select **Add**, then **New reservation**.
2. Under **Customer**, search for an existing customer, or type a new name to create one.
3. Select a **Service**.
4. Select a **Resource**, or leave **First available**.
5. Set the date and start time under **Booked from**. **Booked to** follows the duration of the service.
6. Select **Save appointment**.

{% include figure.html src="/assets/images/getting-started/test-reservation/01-new-reservation.webp" alt="The new reservation form filled in with a customer, a service, a resource and a time" %}

## Find a free time

When you have chosen a service, the times that are free on the chosen date are listed under **Available slots** on the left. The same panel lists the reservations already made that day.

## Messages to the customer and the resource

When you have chosen a customer, tick what to send:

- **Confirmation**: **Email** or **SMS** to the customer.
- **Reminder**: **SMS** to the customer before the reservation.
- **Notification**: **Email** or **SMS** to the resource.

Which boxes are ticked from the start follows your [notification settings]({% link _notifications/overview.md %}).

## Other fields

| Field | What it does |
|---|---|
| **Save even if occupied** | Saves the reservation even if the resource is already booked at that time. |
| **All day** | The reservation covers whole days. |
| **Repeat with a pattern** | Creates a series, for example every week for ten weeks. Choose how often and when it ends. |
| **Notes** | Your own notes on the reservation. Select the megaphone to dictate. |

## Types of reservation

At the top of the form you choose the type.

| Type | Use it for |
|---|---|
| **Customer reservation** | A normal reservation for a customer. |
| **Drop-in** | A customer who walks in when you do not want to, or cannot, record their details. The reservation is saved with the service and the time, but without a customer. |
| **Busy** | Time when the resource cannot be booked, such as a meeting or a vacation. Give it a **Title** instead of a customer. See [Vacations, holidays and blocking dates]({% link _availability/time-off.md %}). |

## From a customer's page

You can also open a customer from **Customers** and select **New reservation**. The customer is then already filled in.

## Related

- [Change, move or cancel a reservation]({% link _bookings/change-reservation.md %})
