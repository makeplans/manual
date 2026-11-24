---
title: "Zoom integration"
description: "Create a Zoom meeting automatically for each reservation and send the link to the customer."
nav_order: 10
redirect_from:
  - /article/37-zoom-integration
verified: 2026-11-23
review: needs-espen
---

# Zoom integration

With Zoom connected, MakePlans creates a Zoom meeting for each new reservation of the services you choose.

## Connect Zoom

1. Open setup and select **Integrations**, then **Zoom**.
2. Select **Connect to service** and log in to Zoom.
3. Back in MakePlans, choose the MakePlans account to connect.

## Set it up

1. **Connect each resource to a Zoom user.** Open setup, select **Resources**, edit the resource and choose the Zoom user. Save.
2. **Turn Zoom on for a service.** Edit the service, tick **Automatically create a Zoom meeting for this service** and save.
3. **Turn Zoom on for an event type** in the same way.

## Events

For events you can choose:

- whether group sessions are a Zoom webinar or a Zoom meeting. Webinars need a Zoom plan that includes them.
- whether each attendant gets their own link or all share one. This needs a paid Zoom account.

## Send the link to the customer

{% raw %}
Put `{{ booking.zoom_url }}` in a message. See [Merge fields](/notifications/merge-fields/).
{% endraw %}

{% include alert.html type="warning" content="Do not put the Zoom link in the confirmation message. The meeting may not have been created yet when the confirmation is sent. Use the reminder, or a message template sent more than 5 minutes after the reservation is made." %}

Good places for the link:

- **Text in SMS reminder** in setup under **Communication**.
- A [message template](/notifications/message-templates/) of the type reminder.

## Disconnect

Open the Zoom integration page and select **Delete**.
