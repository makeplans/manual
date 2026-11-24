---
title: "Accept payments with Vipps"
description: "Connect Vipps so customers in Scandinavia can pay for a reservation in the Vipps app."
nav_order: 2
redirect_from:
  - /article/84-accept-payments-with-vipps
verified: 2026-11-23
---

# Accept payments with Vipps

With Vipps, customers pay for a reservation in the Vipps app. The payment goes straight to your Vipps business account.

## What you need from Vipps

You need an agreement with Vipps for online payments, called "Ta betalt på nett". A Vipps number for payments between people is not enough.

Order it from [Vipps](https://vippsmobilepay.com/nb-NO/panett) and name MakePlans as your partner when you register. MakePlans has a partner agreement with Vipps, so there is no extra fee from us. You pay Vipps' own price per transaction.

## Connect Vipps

When your agreement is approved:

1. Open setup and select **Integrations**, then **Vipps**.
2. Enter your **Merchant serial nr**. If your Vipps sales unit was set up through MakePlans, this is all you need.
3. If you have your own Vipps agreement, also tick **Use my own Vipps agreement keys instead of MakePlans partner keys** and enter **Client ID**, **Client secret** and **Vipps Subscription Key**. You find these in the Vipps business portal under API keys, not in the Vipps app.
4. Select **Save integration**.

{% include alert.html type="warning" content="Do not add the Vipps integration before your agreement for online payments is ready. With missing or wrong values, customers get an error when they try to pay." %}

## Require payment for a service or event

Connecting Vipps is not enough on its own. For each service or event type that should be paid in advance, enter a price and tick **Pre-payment required**.

## Test it

MakePlans cannot check your Vipps details for you, so make a test reservation. Set a low price on a service for a moment, book it on the booking site and pay with Vipps. Then refund the payment from the reservation or in the Vipps portal.

## How it works for the customer

1. The customer chooses a time and verifies themselves on the booking site.
2. They are sent to Vipps and approve the payment in the app.
3. The amount is charged at once. Vipps tells MakePlans, and the reservation is confirmed.

The payment shows your company name. Payouts and transaction reports are in the Vipps portal. MakePlans does not send the customer a receipt.

## If the payment is not completed

While the payment is waiting, the time is held for about 20 minutes and the reservation has the state "Awaiting payment". The customer can go back and try again within that time. After that the time is released, and the customer has to book again.

A reservation that is not paid is never confirmed.

## Payment requests

You can send a Vipps payment request from a reservation, for example to charge after the appointment. The customer must have a phone number and the service must have a price. Tick **Send payment requests** on the Vipps integration page, and a link for sending the request appears on the reservation.

## Troubleshooting

| Problem | Check |
|---|---|
| The customer gets an error when paying | The values under **Integrations**, **Vipps**. A wrong merchant serial number is the usual cause. |
| Reservations go through without payment | That the service has a price, that **Pre-payment required** is ticked and saved, and that the integration is active. |
| The customer has paid but there is no reservation | Look up the transaction in the Vipps portal. Some customers pay manually to your Vipps number instead of through the booking site. The money is in your Vipps account, but no reservation was made, so you must add it yourself. |

## Related

- [Fees, refunds and no-shows]({% link _payments/fees-and-refunds.md %})
