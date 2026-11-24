---
title: "Custom fields"
description: "Add your own fields to the reservation form on the booking site and to the forms in the admin."
nav_order: 9
redirect_from:
  - /article/51-using-custom-fields
verified: 2026-11-23
review: needs-espen
---

# Custom fields

Custom fields let you collect and store information MakePlans does not have a field for, such as a car registration number on a reservation or a membership number on a customer.

{% include alert.html type="info" content="Custom fields are written as short lines of code. If you are not comfortable with that, contact support and we will help you set them up." %}

You can add custom fields to reservations, customers, services, events, resources, categories and the account. A field can be for your own use in the admin only, or also be shown to customers on the booking site.

## Where the forms are

| Form | Where to edit it |
|---|---|
| The reservation form on the booking site | Setup, **Booking site**, **Forms**, **Custom reservation form** |
| The customer registration form on the booking site | Setup, **Booking site**, **Forms**, **Custom person registration form** |
| A reservation form for one service | The service form, **Show custom reservation form** |
| Extra fields in the admin forms | Setup, **Custom fields** |

A field shown on the booking site must also be added to the matching admin form under **Custom fields**, with the same field name. The label can be different.

## The reservation form on the booking site

Each line is one field. This is the default form:

{% raw %}
```liquid
{% name %}
{% phone %}
{% email %}
{% count %}
{% note %}
```
{% endraw %}

`count` is only shown when the service allows more than one person per reservation.

The standard fields you can use are:

{% raw %}
```liquid
{% name %}
{% phone %}
{% email %}
{% date_of_birth %}
{% national_id_no %}
{% street %}
{% postal_code %}
{% city %}
{% state %}
{% country_code %}
{% count %}
{% coupon_code %}
{% terms_accepted %}
{% opt_in_marketing %}
{% note %}
```
{% endraw %}

Use each standard field only once in a form. Standard fields are saved on the customer, except `count` and `note`, which are saved on the reservation.

### Change a label

Add your own label in quotes:

{% raw %}
```liquid
{% phone 'Mobile phone number' %}
```
{% endraw %}

### Make a field required

Name is always required. Phone is required with SMS verification, and email with email verification. To require another field, add `data-required="true"`. Use `nil` to keep the standard label:

{% raw %}
```liquid
{% email nil, 'data-required="true"' %}
{% street 'Your street', 'data-required="true"' %}
```
{% endraw %}

This check runs in the customer's browser only.

## Your own fields

A custom field has a label and a field name. The field name identifies the field in exports and in the API, so keep it short, in lowercase and without spaces.

| Type | Example |
|---|---|
| Text | {% raw %}`{% text 'Car registration number', 'car_reg' %}`{% endraw %} |
| Textarea | {% raw %}`{% textarea 'Information from supplier', 'supplier_info' %}`{% endraw %} |
| Checkbox | {% raw %}`{% checkbox 'Do you want lunch?', 'lunch' %}`{% endraw %} |
| Select | {% raw %}`{% select 'Level', 'level', ['Beginner','Average','Expert'] %}`{% endraw %} |
| Number | {% raw %}`{% number 'How old are you?', 'age' %}`{% endraw %} |
| Date | {% raw %}`{% date 'Membership date', 'became_member_at' %}`{% endraw %} |
| URL | {% raw %}`{% url 'Website', 'website_link' %}`{% endraw %} |
| Hidden | {% raw %}`{% hidden 'secret' %}`{% endraw %} |

Notes:

- End the field name of a date with `_at`, so the value is always treated as a date.
- A select starts with an empty choice so customers do not pick a value by mistake.
- All values are stored as text.

### Example

A reservation form that asks for a mobile number, requires email and adds a lunch question:

{% raw %}
```liquid
{% name %}
{% phone 'Mobile phone number' %}
{% email nil, 'data-required="true"' %}
{% checkbox 'Do you want lunch when you arrive?', 'lunch' %}
{% note %}
```
{% endraw %}

To see and edit the answer in the admin, add the same field under setup, **Custom fields**, in **Custom reservation fields**:

{% raw %}
```liquid
{% checkbox 'Lunch', 'lunch' %}
```
{% endraw %}

### Save a field on the customer

Fields in the reservation form are saved on the reservation. To save one on the customer instead, add the option at the end:

{% raw %}
```liquid
{% text 'Membership number', 'member_no', '', '{"object":"person"}' %}
```
{% endraw %}

## Full reference

The complete syntax, including default values for selects, validation and showing different text per language, is in the [custom forms documentation](https://github.com/makeplans/makeplans-custom-forms).
