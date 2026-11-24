---
title: "Merge fields"
description: "Insert the customer's name, the time, the service and other details into messages and texts."
nav_order: 4
verified: 2026-11-23
---

# Merge fields

A merge field is a placeholder that MakePlans replaces with the real value when the message is sent. You can use merge fields in message texts, message templates and several texts on the booking site.

{% raw %}
```liquid
Hi {{ booking.person.name }},
you have booked {{ booking.resource.title }}
on {{ booking.booked_from }}.
```
{% endraw %}

When the message is sent, each placeholder is replaced: the customer's name, the name of the resource, and the date and time of the reservation.

## The reservation

{% raw %}

| Merge field | Gives |
|---|---|
| `{{ booking.booked_from }}` | Start time, written in your account's language |
| `{{ booking.booked_to }}` | End time |
| `{{ booking.time_range }}` | Start and end time together |
| `{{ booking.title }}` | The title of the reservation |
| `{{ booking.count }}` | Number of people |
| `{{ booking.notes }}` | Notes |
| `{{ booking.price }}` | Price |
| `{{ booking.link }}` | A link to a page with information about the reservation |
| `{{ booking.verification_code }}` | The verification code, for SMS |
| `{{ booking.verification_link }}` | The verification link, for email |
| `{{ booking.terms }}` | The terms for the service, or your general terms |
| `{{ booking.zoom_url }}` | The Zoom link, when the Zoom integration is on |
| `{{ booking.whereby_url }}` | The Whereby link, when the Whereby integration is on |

{% endraw %}

## The customer

{% raw %}

| Merge field | Gives |
|---|---|
| `{{ booking.person.name }}` | Name |
| `{{ booking.person.email }}` | Email |
| `{{ booking.person.phone_number }}` | Phone number |
| `{{ booking.person.street }}`, `postal_code`, `city`, `state`, `country` | Address |
| `{{ booking.person.date_of_birth }}` | Date of birth |

{% endraw %}

## The service, event and resource

{% raw %}

| Merge field | Gives |
|---|---|
| `{{ booking.service.title }}` | Name of the service |
| `{{ booking.service.description }}` | Description of the service |
| `{{ booking.service.price }}` | Price of the service |
| `{{ booking.event.title }}` | Full title of the event, including the event type |
| `{{ booking.event.event_title }}` | Title of this event only |
| `{{ booking.event.description }}` | Description of the event |
| `{{ booking.resource.title }}` | Name of the resource |

{% endraw %}

## Your business

{% raw %}

| Merge field | Gives |
|---|---|
| `{{ booking.client.name }}` | Company name |
| `{{ booking.client.address }}` | Address |
| `{{ booking.client.email }}` | Email |
| `{{ booking.client.phone_number }}` | Phone number |

{% endraw %}

In texts that are not about a reservation, such as the footer of the booking site, write `client` without `booking`:

{% raw %}
```liquid
This is the booking site for {{ client.name }}.
```
{% endraw %}

## Your own fields

Values from [custom fields]({% link _services/custom-fields.md %}) are under `custom_data`, followed by the field name:

{% raw %}
```liquid
{{ booking.custom_data.car_reg }}
{{ booking.person.custom_data.member_no }}
```
{% endraw %}

## Format dates and times

To write the date your own way, use the raw time with the `i18n_date` filter. It follows the language and time zone of your account.

{% raw %}
```liquid
{{ booking.booked_from_iso8601 | i18n_date: '%A, %B %-d, %Y' }}
```
{% endraw %}

gives "Thursday, January 4, 2018", and

{% raw %}
```liquid
{{ booking.booked_from_iso8601 | i18n_date: '%H:%M' }}
```
{% endraw %}

gives "13:25".

## Different text per language

{% raw %}
```liquid
{% if locale == 'nb' %}
Velkommen!
{% else %}
Welcome!
{% endif %}
```
{% endraw %}

## Full reference

Messages are written in Liquid, so you can also use HTML and Liquid's own functions. The complete list of merge fields is in the [custom messages documentation](https://github.com/makeplans/makeplans-custom-messages).
