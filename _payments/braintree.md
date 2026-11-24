---
title: "Accept payments with Braintree"
description: "Connect Braintree to take card payments when customers book."
nav_order: 3
redirect_from:
  - /article/22-accept-payments-with-braintree
verified: 2026-11-23
review: needs-espen
---

# Accept payments with Braintree

Braintree is a card payment provider. You need your own [Braintree](https://www.braintreepayments.com) account.

## Connect Braintree

1. Open setup and select **Integrations**, then **Braintree**.
2. Choose the **Environment**: **Production** for real payments, **Sandbox** for testing.
3. Enter **Merchant**, **Public key**, **Private key** and **Cse key** from your Braintree account.
4. Select **Save integration**.

## Require payment for a service or event

Edit the service or event, enter a price and tick **Pre-payment required**. Customers must then pay by card to complete a reservation for it.

## Related

- [Payments and sales]({% link _payments/overview.md %})
