---
title: "Show reservations in other calendars"
description: "See your MakePlans reservations in Google Calendar, Outlook, Apple Calendar and other calendar apps with an iCalendar feed."
nav_order: 1
redirect_from:
  - /article/54-show-bookings-from-makeplans-in-other-calendars
verified: 2026-11-23
review: needs-espen
---

# Show reservations in other calendars

With an iCalendar feed, your reservations show up in the calendar app you already use, such as Google Calendar, Apple Calendar or Outlook.

The feed is one-way and read-only. You see your MakePlans reservations in the other calendar, but changes must be made in MakePlans, and appointments in the other calendar do not block times in MakePlans.

## A feed for one resource

1. Open setup, select **Resources** and select the name of the resource.
2. Under **iCalendar-feed**, select **Activate iCalendar-feed**.
3. Copy the address that is shown.

## A feed for the whole account

1. Open setup and select **Tools**, then **iCalendar-feeds**.
2. Select **Activate account iCalendar-feeds**.
3. Copy the address.

## Add the feed to your calendar

In your calendar app, add a new calendar from an address (often called "subscribe" or "from URL") and paste the address of the feed.

{% include alert.html type="warning" content="The address contains the key to the reservations. Anyone who has it can read them, so do not share it." %}

## Limits

- The feed contains upcoming reservations only, at most 200.
- The calendar app decides how often it fetches the feed. Some, such as Google Calendar, do it rarely, so new and changed reservations can take a long time to appear. Some apps let you refresh by hand.
