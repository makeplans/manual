---
title: "FAQ: Features and integrations"
description: "Answers about booking several services, gift cards and passes, Vipps, calendar sync, mobile apps, languages, the API, tracking and data processing."
nav_order: 2
redirect_from:
  - /article/96-faq-features-and-integrations
verified: 2026-11-23
---

# FAQ: Features and integrations

## Can a customer book several services in one reservation?

Each service is a reservation of its own. Two ways to handle it:

- Create a combined service, such as "Cut + colour", with the total duration.
- Let the customer book twice. After the first booking they are already verified, so the second is quick.

If a customer needs a longer appointment, a service can allow several slots in one reservation. See [Service form]({% link _services/service-form.md %}).

## Do you have gift cards, passes and subscriptions?

Yes. See [Gift cards]({% link _payments/gift-cards.md %}), [Passes]({% link _payments/passes.md %}) and [Subscriptions]({% link _payments/subscriptions.md %}).

## Do you support Vipps, and is the 2% fee on top of Stripe's?

Yes to both. With Stripe, MakePlans charges a platform fee of 2% in addition to Stripe's own fee. With Vipps there is no fee from MakePlans, only Vipps' own price. See [Fees, refunds and no-shows]({% link _payments/fees-and-refunds.md %}).

## Does MakePlans sync both ways with Google Calendar or Outlook?

No. You can show your MakePlans reservations in other calendars with an iCalendar feed, but it is one-way and read-only. Appointments in your other calendar do not block times in MakePlans. See [Show reservations in other calendars]({% link _integrations/calendars.md %}).

## Is there a mobile app?

No, and you do not need one. Both the admin and the booking site work in the browser on your phone. To get an icon on your home screen, open MakePlans in the browser and choose "Add to Home Screen" from the browser's menu.

## Which languages can the booking site use?

See [Languages]({% link _booking_site/languages.md %}).

## Where do I find my API key?

Open setup and select **Developer**, then **API**. See [Enable the API]({% link _integrations/api.md %}).

## How do I track reservations in Google Ads or Tag Manager?

Enter your Google Tag Manager or Google Analytics ID in setup under **Booking site**, then **General**. MakePlans sends a `booking_completed` event when a reservation is completed. Use it as your conversion. See [Google Tag Manager]({% link _integrations/google-tag-manager.md %}).

## Do you sign a data processing agreement, and where is the data stored?

The data processing agreement is part of the terms of service. Data is stored in Norway. See [GDPR and privacy]({% link _account/gdpr.md %}).
