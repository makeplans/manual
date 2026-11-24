---
title: "Overview"
seo:
  title: "Payments and sales"
description: "Take payment when customers book, and handle refunds, coupon codes and gift cards."
nav_order: 0
redirect_from:
  - /article/23-accept-payments-with-quickpay
verified: 2026-11-23
---

# Payments and sales

Customers can pay when they book. The money goes straight from the customer to your own account with a payment provider. MakePlans never holds it.

## How it fits together

To take payment you need three things:

1. **An agreement with a payment provider**, connected to MakePlans under setup, **Integrations**.
2. **A price** on the service or event.
3. **Pre-payment required** ticked on the service or event. The reservation is then confirmed only when the customer has paid.

{% include alert.html type="warning" content="If a service requires pre-payment and no payment provider is connected, customers cannot complete a reservation for it." %}

## Payment providers

| Provider | For |
|---|---|
| [Stripe]({% link _payments/stripe.md %}) | Card payments. Recommended, and quick to get started with. |
| [Vipps]({% link _payments/vipps.md %}) | Mobile payment in Scandinavia. |
| [Braintree]({% link _payments/braintree.md %}) | Card payments through Braintree. |
| [Front Go]({% link _payments/front-go.md %}) | Payments in Norway. |

If more than one provider is connected, for example Stripe and Vipps, the customer chooses how to pay. The **Default payment provider** is set in setup under **Account**.

## In this section

- [Fees, refunds and no-shows]({% link _payments/fees-and-refunds.md %})
- [Coupon codes]({% link _payments/coupons.md %})
- [Gift cards]({% link _payments/gift-cards.md %})
- [Products and add-ons]({% link _payments/products.md %})
- [Passes]({% link _payments/passes.md %})
- [Subscriptions]({% link _payments/subscriptions.md %})
- [Orders]({% link _payments/orders.md %})

How the price of a reservation is calculated is covered in [Prices]({% link _services/prices.md %}).
