---
title: "Accept payments with Stripe"
description: "Connect Stripe to take card payments when customers book, and require payment for a service or event."
nav_order: 1
redirect_from:
  - /article/17-accept-payments-with-stripe
verified: 2026-11-23
review: needs-espen
---

# Accept payments with Stripe

Stripe lets your customers pay by card when they book. You need your own Stripe account, which you can create while connecting. Stripe pays out to your bank account.

## Connect Stripe

1. Open setup and select **Integrations**, then **Stripe**.
2. Select **Connect to service**. This takes you to Stripe.
3. Log in to Stripe, or create an account, and allow MakePlans to access it.
4. You are sent back to MakePlans. Choose the MakePlans account to connect.

{% include figure.html src="/assets/images/payments/stripe/01-stripe-integration.webp" alt="The Stripe integration page with the Connect to service button and the platform fee" %}

## Require payment for a service or event

1. Edit the service, or the event.
2. Enter a price.
3. Tick **Pre-payment required**.
4. Save.

Customers must now pay by card to complete a reservation for it.

## What it costs

Stripe charges its own fee for each transaction. MakePlans charges a platform fee of 2% in addition. See [Fees, refunds and no-shows]({% link _payments/fees-and-refunds.md %}).

## Test it

Make a reservation yourself on the booking site and pay with a real card for a small amount. Then refund it from the reservation.

## Related

- [Fees, refunds and no-shows]({% link _payments/fees-and-refunds.md %})
