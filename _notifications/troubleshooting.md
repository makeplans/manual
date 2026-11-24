---
title: "Troubleshooting SMS and email delivery"
description: "What to check when a customer says they did not receive a verification code, a confirmation or a reminder."
nav_order: 8
redirect_from:
  - /article/79-troubleshooting-sms-and-email-delivery
verified: 2026-11-23
---

# Troubleshooting SMS and email delivery

When a customer says a message never arrived, the cause is almost always one of the following. Go through them in order.

## 1. Look at the reservation

Open the reservation in the admin. The **Log** shows what has happened to it and when.

- If the reservation is there and confirmed, the message was most likely sent, and the problem is on the customer's side.
- If there is no reservation, the customer probably never completed the verification.

## 2. The verification was never completed

A reservation is not confirmed until the customer has entered the code. A reservation that is not completed is released after 20 minutes. Customers sometimes close the page believing they are done.

Ask the customer to book again and complete the verification. A new booking sends a new code.

## 3. The email is in spam

Ask the customer to:

1. Check the spam or junk folder, and tabs such as Promotions in Gmail.
2. Search their mailbox for "makeplans".
3. Add the sender to their contacts or safe senders.

If many customers struggle with email, consider SMS verification. A code on the phone is easier for most people. See [Verification]({% link _booking_site/verification.md %}).

## 4. The customer's details are out of date

For security, codes and messages go to the phone number or email stored on the customer's profile, not to what they type when booking. A returning customer with a new number gets the code on the old one.

Open the customer under **Customers** and correct the phone number or email. Check for duplicate profiles at the same time. See [Customers]({% link _bookings/customers.md %}).

If you have changed verification method, for example from SMS to email, existing customers may lack the detail that is now needed. They get an error saying it is not saved on their profile. Add it on the profile. For this reason, think twice before changing verification method when you already have many customers.

## 5. Foreign phone numbers

A number from another country must be written with its country code, such as +4512345678. A number without country code is read as a number in your account's country and may be saved wrongly or rejected.

SMS cannot be delivered to a few countries. If a customer abroad cannot receive SMS, contact support, add the reservation for them in the admin, or use email verification.

## 6. No phone number on the reservation

With email verification, the phone number is optional. Customers who leave it out cannot get SMS confirmations or reminders. To require it, use SMS verification, or make the phone field required in a [custom reservation form]({% link _services/custom-fields.md %}).

## 7. Reminders

- SMS reminders must be turned on under **Notifications - customer**, and only apply to reservations made after that.
- The reminder is sent at the set time, by default noon the day before. For a reservation made later than that, it is sent shortly after confirmation.
- If another system is connected to MakePlans and sends its own reminders, check there too. Double or missing reminders often come from the other system.

## 8. No SMS credits

Every SMS uses a credit. Check your balance in setup under **SMS credits**.

## Still not solved

No SMS service can promise that every message arrives. Now and then an operator fails to deliver, or the phone is off or abroad. If you have checked everything above, contact support with a link to the reservation, or the customer's phone number or email, and we will check the delivery logs.
