---
title: "Different opening hours for one service"
description: "Give a service its own opening hours per resource with the Provider setting, for example a service offered Monday to Wednesday only."
nav_order: 4
verified: 2026-11-23
review: needs-espen
---

# Different opening hours for one service

By default, opening hours are set on the resource and are the same for every service that resource offers. If one service should only be bookable at certain times, give that service its own hours.

Example: Sam Taylor works Monday to Friday and offers both sports massage and physiotherapy. Physiotherapy should only be bookable Monday to Wednesday. Sports massage keeps following Sam's normal opening hours.

In this setting, each resource that offers the service is called a provider.

## Set it up

1. Open setup, select **Services** and edit the service.
2. Set **Availability is defined by** to **Provider**.
3. Select **Save service**.
4. On the service page, under **Availability is defined by**, select **Availability pr provider**.
5. For each resource, tick **Open** on the days the service can be booked and enter **From** and **To**. Select **+ add** for a second period on the same day.
6. Select **Save**.

{% include figure.html src="/assets/images/services/provider-availability/01-availability-per-provider.png" alt="The availability grid for Physiotherapy consultation, with both resources open Monday to Wednesday from 09:00 to 17:00" %}

{% include alert.html type="warning" content="All days start as closed for every provider. Set the hours right after you switch to **Provider**, or the service cannot be booked." %}

The other services the resource offers are not affected. They keep using the [opening hours of the resource]({% link _availability/opening-hours.md %}).

## Go back to the resource's hours

Edit the service and set **Availability is defined by** back to **Resource (default)**.

## Related

- [Opening hours]({% link _availability/opening-hours.md %})
- [Service form]({% link _services/service-form.md %})
