---
title: "Send an SMS to customers"
description: "Send one SMS to all your customers, to customers with certain reservations, to one customer, or to everyone signed up for an event."
nav_order: 7
verified: 2026-11-23
---

# Send an SMS to customers

You need enough SMS credits for every recipient before you send. A message longer than 160 characters uses two or more credits per recipient, but arrives as one message.

## To all customers

1. Open setup and select **Tools**, then **Send SMS to all customers**.
2. Check the number of recipients at the top.
3. Write the **Message**.
4. Select **Send**.

{% include alert.html type="warning" content="This sends to every customer on your account. It cannot be undone." %}

## To customers with certain reservations

1. Open setup and select **Tools**, then **Send SMS to filtered customers**.
2. Choose at least one filter: **Bookings on or after**, **Bookings on or before**, **Services** or **Resources**.
3. Select **Find recipients**, then write and send the message.

Use this to reach, for example, everyone booked with one employee next week.

## To one customer

Open **Customers** and select **Send SMS** next to a customer who has a phone number.

## To everyone signed up for an event

Open the event and select **Send SMS to all participants**. See [Manage the attendants of an event]({% link _services/attendants.md %}).

## Make it personal

{% raw %}
Use tags in the message, such as `{{ person.name }}`, `{{ person.first_name }}` or `{{ person.email }}`.
{% endraw %}

## Email to all customers

There is no function for sending one email to all customers. Export your customers in setup under **Export** and use a newsletter service. With the Mailchimp or MailerLite integration, new customers are added to your list automatically. See [Integrations]({% link _integrations/overview.md %}).
