---
title: "Fees, refunds and no-shows"
description: "What it costs to take payments, how to refund a payment, and how to handle deposits and customers who do not turn up."
nav_order: 5
redirect_from:
  - /article/85-payment-fees-refunds-and-discount-codes
verified: 2026-11-23
---

# Fees, refunds and no-shows

## Fees

Payments are processed by your payment provider, which pays out directly to your bank account.

| Provider | Fees |
|---|---|
| Stripe | Stripe's own fee per transaction, plus a platform fee of 2% to MakePlans. The 2% comes on top of Stripe's fee. |
| Vipps | Vipps' own price only. MakePlans charges nothing extra. |

All fees are taken from the payment before it is paid out to you. If a customer pays 1000, both Stripe's fee and the 2% are deducted from that amount. You see the total fees per transaction in your Stripe dashboard.

There is no setup fee or monthly fee for taking payments, and no fee on free reservations. If you have a high volume or are a non-profit, contact us about a lower platform fee.

## Refunds

A refund is never made automatically. Cancelling a reservation, whether you or the customer does it, does not pay the money back.

To refund, open a reservation that has a completed payment and select the refund link. MakePlans tells the provider to refund the full amount to the customer.

You do not get the transaction fees back. With Stripe, the fees for the original payment, including the MakePlans platform fee, are kept, and the refunded amount is taken from your next payout. See [Stripe's explanation](https://support.stripe.com/questions/understanding-fees-for-refunded-payments). For Vipps, see Vipps' own rules.

## Payment in advance and deposits

| | Supported |
|---|---|
| Full payment in advance | Yes. The customer pays the whole price before the reservation is confirmed. |
| A deposit, with the rest paid later | Not yet. |
| Reserving an amount on the card without charging it | No. A reservation on a card only lasts about a week, which is too short for most bookings. |

## No-shows and late cancellations

There is no automatic fee for a no-show or a late cancellation. You have two options:

- Tick **Pre-payment required** on the service.
- Let customers save their card with Stripe on their profile. When a reservation has a saved card and the service has a price, you can charge the card from the reservation after it is completed.

A charge you make yourself cannot use BankID or 3-D Secure, so it can fail if the customer's bank demands that.

## Reports

MakePlans stores the amount paid on each reservation, but it is not an accounting system. For complete transaction reports, use Stripe and Vipps.

## Related

- [Coupon codes]({% link _payments/coupons.md %})
