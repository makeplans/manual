---
title: "Webhooks"
description: "Send a message to your own system when something happens in MakePlans."
nav_order: 15
verified: 2026-11-23
review: needs-espen
---

# Webhooks

A webhook sends a message to an address in your own system when something happens in MakePlans, such as a new reservation. It is meant for developers.

## Add a webhook

1. Open setup and select **Developer**, then **Webhooks**.
2. Select **New webhook**.
3. Enter the **Event** and the **Target URL**.
4. Keep **Active** ticked and select **Save webhook**.

{% include figure.html src="/assets/images/integrations/webhooks/01-new-webhook.webp" alt="The new webhook form with Event, Target URL and Active" %}

## Verify that a message comes from MakePlans

The **Account secret** on the Webhooks page is used to verify incoming messages. Treat it like a password.

The events you can use and how to verify messages are described at [developer.makeplans.com](https://developer.makeplans.com).
