---
title: "Store values from incoming links"
description: "Pass values to the reservation form through the link customers arrive on, such as a campaign code or a note."
nav_order: 11
redirect_from:
  - /article/58-incoming-links
verified: 2026-11-23
review: needs-espen
---

# Store values from incoming links

A link to your booking site can carry values that are saved on the reservation the customer makes. Use it to record where a customer came from, or to fill in a field for them.

Add `remember_params` to the address of the booking site or of a service. The value is kept while the customer books and saved on the reservation.

| To set | Add |
|---|---|
| The notes on the reservation | `remember_params[booking][notes]=your text` |
| A custom field | `remember_params[booking][custom_data][field_name]=value` |

Example:

```
https://youraccount.makeplans.com?remember_params[booking][notes]=1337&remember_params[booking][custom_data][campaign]=spring
```

A custom field must also be in your custom reservation form. See [Custom fields]({% link _services/custom-fields.md %}).

The fields of a reservation that can be set are listed in the [API documentation](https://developer.makeplans.com).
