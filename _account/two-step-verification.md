---
title: "2-step verification (2FA)"
description: "Turn on two-factor authentication (2FA) for your login with an authenticator app, and see which standard MakePlans uses."
nav_order: 4
---

# 2-step verification (2FA)

With 2-step verification, your password alone is not enough to log in. You also enter a six-digit code from an authenticator app on your phone, so someone who gets hold of your password still cannot get in. This is often called two-factor authentication (2FA or MFA).

The codes are time-based one-time passwords (TOTP). TOTP is an open internet standard, published by the IETF as [RFC 6238](https://datatracker.ietf.org/doc/html/rfc6238). It is the standard used by FreeOTP, Google Authenticator, Microsoft Authenticator, 1Password, Authy and other authenticator apps. Codes by SMS, passkeys and security keys are not supported.

## Before you start

Install an authenticator app on your phone. Any app that supports TOTP works, for example:

- FreeOTP (open source)
- Google Authenticator
- Microsoft Authenticator
- 1Password
- Authy

Each user turns on 2-step verification for their own login.

## Turn on 2-step verification

1. Select your initials in the top right corner, then **Profile**.
2. Select **Activate 2-step verification**.
3. Scan the QR code with your authenticator app. The app starts showing a six-digit code that changes every 30 seconds.
4. Enter your password and the code from the app, and confirm.

Finish within 10 minutes. After that the QR code expires, and you start again from your profile.

Turning on 2-step verification logs you out on your other devices and browsers. Log in there again with your password and a code.

## Log in with a code

1. Enter your email and password as usual.
2. Open your authenticator app and enter the six-digit code it shows.

## The code is not accepted

- **Use the code on screen now.** A code works only while the app shows it. If it is about to change, wait for the next one.
- **Check the clock on your phone.** The codes are based on the time. Set date and time to automatic in your phone settings.
- **Check that you read the right entry**, if your app has several.

## Turn off 2-step verification

Open your **Profile** and turn it off there. You need your password and a current code from the app. This also logs you out on your other devices and browsers.

## You are getting a new phone

Do this while you still have the old phone:

1. Turn off 2-step verification with a code from the old phone.
2. Turn it on again and scan the new QR code with the new phone.

Many authenticator apps can also move or sync their codes to a new phone. Then you do not need to change anything in MakePlans.

## You have lost your phone

There are no backup codes, and MakePlans cannot send the code by SMS or email.

- If your authenticator app has a backup or syncs between devices, restore it on another device and log in as usual.
- Otherwise, contact support.

To avoid this, use an authenticator app with backup or sync.

## Technical details

For IT departments and security reviews.

| | |
|---|---|
| **Method** | Time-based one-time password (TOTP) from an authenticator app |
| **Standard** | [RFC 6238](https://datatracker.ietf.org/doc/html/rfc6238) (TOTP), built on [RFC 4226](https://datatracker.ietf.org/doc/html/rfc4226) (HOTP) |
| **Code** | 6 digits, new code every 30 seconds, HMAC-SHA1 |
| **Setup** | QR code with an `otpauth://` address, the format authenticator apps read |
| **Applies to** | Users who log in to the MakePlans admin |
| **Not supported** | Codes by SMS or email, passkeys and security keys (WebAuthn), backup codes |

Customers on the booking site do not use 2-step verification. They confirm who they are with a code sent by email or SMS. See [Verification]({% link _booking_site/verification.md %}).

## Related

- [Your profile, password and login]({% link _account/login.md %})
- [Users and access levels]({% link _account/users.md %})
- [Security]({% link _account/security.md %})
