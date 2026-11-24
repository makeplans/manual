---
title: "Subscriptions"
description: "Sell a subscription that renews at a set interval and includes a number of reservations, such as a monthly membership."
nav_order: 10
verified: 2026-11-23
---

# Subscriptions

A subscription gives the customer a number of reservations for a price that recurs, such as a monthly membership.

## Create a subscription

1. Open setup and select **Products**, then **Add**, then **New subscription**.
2. Enter a **Title** and the **Price including taxes**.
3. Fill in the terms in the table below.
4. Save.

| Field | What it does |
|---|---|
| **Renewal price** | The price at each renewal. Leave empty to use the same price as the first period. |
| **Renewal period** | How often it renews: a number of days, weeks, months or years. |
| **Days before renewal to send the renewal notice** | When the customer is told that the subscription is about to renew. |
| **Number of reservations included** | How many reservations each period includes. Tick **Unlimited** for no limit. |
| **Valid for the following services** | The services and event types it can be used for. If you tick none, it is valid for all. |

## Renewal notice for all subscriptions

The default for the renewal notice is set under **Booking site**, then **Rules**, in **Days before a subscription renewal to send the renewal notice**. A subscription with its own value overrides it.

## Keep track

Open **Orders** in the main menu and select **Subscriptions** to see your customers' subscriptions.

## Related

- [Passes]({% link _payments/passes.md %})
- [Orders]({% link _payments/orders.md %})
