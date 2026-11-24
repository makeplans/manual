---
title: "Reservation form and registration form"
description: "Add a text above the reservation form and change which fields customers fill in."
nav_order: 8
verified: 2026-11-23
review: needs-espen
---

# Reservation form and registration form

Open setup and select **Booking site**, then **Forms**.

{% include figure.html src="/assets/images/booking-site/forms/01-forms.webp" alt="The Booking site forms page with the three text fields" %}

| Field | What it does |
|---|---|
| **Text displayed before reservation form** | A message shown above the form, such as what to bring. |
| **Custom reservation form** | Replaces the standard reservation form with your own fields. |
| **Custom person registration form** | Changes the form new customers fill in with their name and contact details. For the Timisoara and Lviv themes. |

The two forms are written as short lines of code, one per field. See [Custom fields]({% link _services/custom-fields.md %}) for how to write them, or contact support for help.

A service can have its own reservation form. Edit the service and fill in **Show custom reservation form**.

{% include alert.html type="info" content="A field you add to the reservation form must also be added in setup under **Custom fields**, so that you can see the answers in the admin." %}
