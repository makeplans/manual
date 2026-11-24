---
title: "Make a test reservation"
description: "Try a reservation from the admin and from your booking site before you share it with customers."
nav_order: 6
verified: 2026-11-23
review: needs-espen
---

# Make a test reservation

Before you share your booking site, make one reservation yourself in the admin and one as a customer. You see what your customers see and can check that times, texts and emails look right.

## Add a reservation in the admin

This is how you add a reservation for someone who calls or drops by.

1. Open the **Calendar** and select **Add**. If you have event types, then select **New reservation**.
2. Under **Customer**, search for an existing customer, or type a new name to create one.
3. Select a **Service**.
4. Select a **Resource**, or leave **First available**.
5. Set the date and start time under **Booked from**. The end time follows the duration of the service. The times that are free that day are listed under **Available slots** on the left.
6. Select **Save appointment**.

{% include figure.html src="/assets/images/getting-started/test-reservation/01-new-reservation.webp" alt="The new reservation form filled in with a customer, a service, a resource and a time" %}

The reservation appears in the calendar in the colour of its resource.

## Book as a customer

1. Open your booking site. The address is shown in setup under **Promote**.
2. Select a service.
3. Select a date, then one of the **Available times**, then **Continue**.
4. Enter your email address and select **Continue**. Use a different address from the one you log in to the admin with, so you see what a new customer sees.
5. Enter the verification code you receive by email and select **Continue**.
6. The first time, enter your name and mobile phone number and select **Register**. The phone field is preset to your account's country, so a local number without country code works.
7. Check the details and select **Complete booking**.

{% include figure.html src="/assets/images/getting-started/test-reservation/02-choose-time.webp" alt="The booking site with a date and a time selected, and the Continue button" %}

The booking site confirms the reservation. From this page a customer can add it to their own calendar, reschedule or cancel.

{% include figure.html src="/assets/images/getting-started/test-reservation/03-confirmed.webp" alt="The booking site page confirming the reservation" %}

## Check the result

- Open the **Calendar** in the admin. The reservation from the booking site is there.
- Check both inboxes. The customer receives a confirmation email, and you receive an email about the new reservation.
- When you are done testing, open the reservation from the **Agenda** and select **Cancel reservation**.

{% include alert.html type="info" content="If no times are offered on a date, check that a resource offering the service is open that day. See [Set your opening hours](/getting-started/opening-hours/)." %}

## Related

- [Share your booking site]({% link _getting_started/share-booking-site.md %})
