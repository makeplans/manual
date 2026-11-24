---
title: "Room display"
description: "Show the status and upcoming reservations of a room on a tablet or screen outside it."
nav_order: 13
redirect_from:
  - /article/69-room-display
verified: 2026-11-23
review: needs-espen
---

# Room display

A room display is a public page for one resource. It shows whether the room is in use and which reservations are coming up. It suits a tablet mounted outside a meeting room.

## Set it up

1. Open setup, select **Resources** and select the name of the resource.
2. Under **Room display**, select **Enable room display**.
3. Open the **Room display link** in a browser on the screen outside the room.
4. Back in the admin, select **Generate setup code**.
5. Enter the code on the screen.

{% include figure.html src="/assets/images/booking-site/room-display/01-enable-room-display.webp" alt="The resource page with the Enable room display button under Sharing and display" %}

The screen now shows the calendar and the reservations for the room.

{% include alert.html type="warning" content="The setup saves an access key in the browser on the screen. Anyone who can get at that device could copy the key and read the reservations for the room, including personal data about customers. Place the screen where it cannot be tampered with." %}

## Related

- [Resource form]({% link _availability/resource-form.md %})
