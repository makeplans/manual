---
title: "Orders"
description: "What an order is, how customers place one on the booking site, and where to find orders, passes, subscriptions, gift cards and coupons."
nav_order: 11
verified: 2026-11-23
review: needs-espen
---

# Orders

When a customer buys something on the booking site, such as a product, a pass or a gift card, it becomes an order.

## How a customer places an order

1. The customer opens the product on the booking site and selects **Add to cart**. They are asked to log in first.
2. The **Shopping Cart** lists what they have added, with the total. They can **Remove** an item or select **Empty cart**.
3. They select **Confirm order** and pay at the checkout.

{% include figure.html src="/assets/images/payments/orders/01-cart.png" alt="The shopping cart on the booking site with one pass, the total and the Confirm order button" %}

{% include alert.html type="warning" content="The checkout needs a payment provider. Without one, customers see \"No payment methods available\" and cannot complete the order." %}

Logged-in customers find their earlier orders under **My orders** on the booking site.

## Find orders in the admin

Open **Orders** in the main menu.

| Tab | Shows |
|---|---|
| **Orders** | All orders. Filter on **Pending**, **Confirmed** or **Cancelled**. |
| **Passes** | Passes held by customers. See [Passes]({% link _payments/passes.md %}). |
| **Subscriptions** | Customers' subscriptions. See [Subscriptions]({% link _payments/subscriptions.md %}). |
| **Gift cards** | Gift cards and their value. See [Gift cards]({% link _payments/gift-cards.md %}). |
| **Coupons** | Your coupon codes. See [Coupon codes]({% link _payments/coupons.md %}). |

## Export

To export orders, open setup and select **Export**, then **Orders**.

## Related

- [Products and add-ons]({% link _payments/products.md %})
