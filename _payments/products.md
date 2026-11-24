---
title: "Products and add-ons"
description: "Sell products on your booking site, and offer add-ons customers can choose together with a reservation."
nav_order: 8
verified: 2026-11-23
review: needs-espen
---

# Products and add-ons

Besides reservations, you can sell other things on your booking site. Everything of this kind is created in setup under **Products**. Select **Add** and choose what to create.

| Type | What it is |
|---|---|
| **Product** | Something you sell on its own, at a fixed price. |
| **Add-on** | An extra the customer can add when reserving a service. |
| **Gift card** | See [Gift cards]({% link _payments/gift-cards.md %}). |
| **Pass** | A number of reservations paid for in advance. See [Passes]({% link _payments/passes.md %}). |
| **Subscription** | Reservations included for a recurring price. See [Subscriptions]({% link _payments/subscriptions.md %}). |

## Create a product

1. Open setup and select **Products**, then **Add**, then **New product**.
2. Enter a **Title** and the **Price including taxes**.
3. Add a **Description** for customers.
4. Save.

## Create an add-on

1. Open setup and select **Products**, then **Add**, then **New addon**.
2. Enter a **Title** and the **Price including taxes**.
3. Under **Available when reserving the following services**, tick the services the add-on belongs to. If you tick none, it is offered with all services.
4. Save.

## Settings they share

| Field | What it does |
|---|---|
| **Show on the booking site** | Clear this to stop offering it without deleting it. |
| **Description** | Text shown to customers. |
| **Show custom reservation form** | Your own form for this product. See [Custom fields]({% link _services/custom-fields.md %}). |
| **Show content for outgoing communication** | Your own email and SMS texts for this product. |

## How customers buy

Customers add a product to a cart on the booking site and confirm the order. They must be logged in and pay online, so you need a [payment provider]({% link _payments/overview.md %}). See [Orders]({% link _payments/orders.md %}).

{% include alert.html type="warning" content="If you use categories on the booking site, put each product in a category. A product outside every category is not shown there. The product's page in the admin warns you when this is the case." %}

## Your own names

If you call these something else, such as "Membership" instead of "Subscription", change the word under setup, **UX**, **Custom titles**. See [Calendar and display settings]({% link _bookings/display-settings.md %}).
