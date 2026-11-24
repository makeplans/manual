---
title: "Resource form"
description: "Every field on the resource form and the resource page: availability, capacity, services, notifications, iCalendar feed and room display."
nav_order: 3
redirect_from:
  - /article/71-resource-form
verified: 2026-11-23
---

# Resource form

To add a resource, open setup, select **Resources**, then **New resource**. To change one, select the pencil next to it.

{% include figure.html src="/assets/images/availability/resource-form/02-resource-form.webp" alt="The resource form with all fields" %}

## Fields

| Field | What it does |
|---|---|
| **Title** | The name of the resource. Customers see it when they choose who or what to book. |
| **Default availability** | The normal opening hours for each weekday. See [Opening hours]({% link _availability/opening-hours.md %}). |
| **Max number of reservations at the same time** | The capacity of the resource. The default is 1. See [Resource capacity]({% link _availability/capacity.md %}). |
| **Max workload points per day** | An optional daily limit across all services. Leave empty for no limit. See [Daily workload points]({% link _availability/workload-points.md %}). |
| **Offers the following services on the booking site** | Tick the services this resource delivers. |
| **Email address(es) for notification** | Who is told about reservations for this resource. Leave empty to use the account's address. Separate several addresses with a semicolon. |
| **Phone number(s) for notification** | Who receives SMS about reservations for this resource. Separate several numbers with a semicolon. |

Select **Save resource** when you are done.

## The resource page

Select the name of a resource in the list to see a summary of its settings.

{% include figure.html src="/assets/images/availability/resource-form/01-resource-page.webp" alt="The resource page with booking settings, notifications and sharing" %}

From this page you can also:

- **Activate iCalendar-feed**: show this resource's reservations in another calendar application, such as Outlook, Google Calendar or the calendar on a phone. The feed is read-only. Changes are still made in MakePlans.
- **Enable room display**: a public display for the resource that shows its current status and upcoming reservations. It suits a tablet mounted outside a room.
- **Clone this resource**: open the new resource form with the same settings filled in.

## Delete a resource

Open the resource form and select **Delete**. If the resource has reservations you want to keep, first [move them to another resource]({% link _availability/move-reservations.md %}).
