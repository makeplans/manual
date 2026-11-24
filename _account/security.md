---
title: "Security"
description: "How to keep your account safe, and technical details for IT departments: IP addresses, webhooks, embedding and senders."
nav_order: 12
redirect_from:
  - /article/62-security-considerations
verified: 2026-11-23
---

# Security

## Keep your account safe

- Give each person their own user. See [Users and access levels]({% link _account/users.md %}).
- Use a password you do not use anywhere else.
- Turn on 2-step verification in your profile. See [Your profile, password and login]({% link _account/login.md %}).
- Remove users when people leave.
- Treat your API key, webhook secret and iCalendar feed addresses like passwords.

## For IT departments

### IP addresses

MakePlans sends from these ranges:

- `185.116.4.0/22`
- `2001:820:2::/48`

### Webhooks

Webhooks are signed with a secret from your account and sent from the IP ranges above. See the [API documentation](https://developer.makeplans.com/#security).

### API from the browser and embedding

To use the public API from JavaScript, or to show the booking site in an iframe, your domain must be approved on the account. Requests from other domains are blocked. See [Embed in your website]({% link _booking_site/embed.md %}).

### Code on the booking site

The booking site has a strict content security policy.

- Your own JavaScript must be added with the `script` tag described in the [custom messages documentation](https://github.com/makeplans/makeplans-custom-messages#javascript).
- Requests to other sites are blocked. Contact support if you need more than the script tag allows.
- Your JavaScript does not run on sensitive pages, such as payment forms.

### Senders

- Emails are sent from `robot@booking.makeplans.com`, unless you have the add-on for your own sender.
- SMS are sent from "MakePlans". In some countries they come from a phone number instead, because of local rules.

## Related

- [GDPR and privacy]({% link _account/gdpr.md %})
