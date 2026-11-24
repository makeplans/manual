---
title: "Prices"
description: "How the price of a reservation is calculated, and how to set different prices for certain days and times."
nav_order: 3
redirect_from:
  - /article/60-pricing-and-payment
verified: 2026-11-23
review: needs-espen
---

# Prices

You set the price on the service, in **Price including taxes**. That is the price for one person and one slot. Leave the field empty for a service without a price.

## How the total is calculated

| Reservation | Calculation | Total at a price of 10 |
|---|---|---|
| One person, one slot | price | 10 |
| 5 people | price × people | 50 |
| 3 slots (3 hours of a 60-minute service) | price × slots | 30 |
| 3 people for 2 slots | price × slots × people | 60 |

Whether customers can book for several people or several slots is decided by **Max number of people allowed per reservation** and **Max number of slots per reservation** on the [service form]({% link _services/service-form.md %}).

## Different prices at certain times

Use **Prices at given times** to charge more or less on certain days or at certain hours, such as evenings or weekends.

1. Open setup, select **Services** and edit the service.
2. Under **Prices at given times**, select **Add price**.
3. Tick the days the price applies to.
4. Enter the period in **From** and **To**, and the **Price**.
5. Select **Add price** again for more periods, or **Remove** to delete one.
6. Select **Save service**.

{% include figure.html src="/assets/images/services/prices/01-prices-at-given-times.webp" alt="The service form with one price rule: Fridays from 15:00 to 17:00 at a price of 65" caption="The standard price is 55. Reservations that start on a Friday between 15:00 and 17:00 cost 65." %}

A reservation that starts inside one of the periods gets that price. All other times use the standard price.

## Taking payment

Showing a price does not mean the customer pays online. To take payment when the customer books, connect a payment provider and tick **Pre-payment required** on the service. See [Payments]({% link _payments/overview.md %}).

## Prices for events

Events have their own price on each event. See [Event types and events]({% link _services/events.md %}).
