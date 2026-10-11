# Privacy Policy — Koine Advanced Indexer

_Last updated: 11 October 2026_

_Published at https://github.com/Vagelis-Prokopiou/Koine-Advanced-Indexer/blob/master/PRIVACY.md — the copy both app stores link to. This file is the source; publishing is a copy, so
`./scripts/check-privacy-policy.sh` checks the two have not drifted._

This policy explains what information the **Koine Advanced Indexer** mobile app
(“the app”, “we”, “us”) collects, why, and how it is handled. The app is a reader
and search tool for four Greek corpora — the Septuagint, the New Testament, the
Apostolic Fathers, and the second-century Apologists — published by Evangelos
Prokopiou.

> **In short:** reading the text happens entirely on your device. The only
> information that ever leaves your device is a *non-reversible, hashed device
> key* and a *count of free searches used* — used only to run the free-search
> allowance and to apply your one-time purchase. We do not collect your name,
> email, or location; we show no ads and use no cross-app or cross-site
> tracking; and we never sell your data.

## Android and iOS differ, and this is where

The two versions of the app are not the same in what they collect, so the sections
below say which applies:

- **Android** keeps the free-search count on a server, so that the free allowance
  survives a reinstall. That is the collection described below.
- **iOS collects nothing.** The count is kept on the device, in the device
  keychain — which is how it survives a reinstall without a server — and the
  unlock is your App Store purchase; there is no Firebase, no anonymous sign-in, and nothing about
  your reading, your searches, or your device leaves the phone. The app's App Store
  privacy manifest declares exactly that. Purchases are handled by Apple, as
  described under *Purchase status*.

Everything under *Information the app does not collect* applies to both.

## Information the app collects (Android)

- **A hashed device identifier.** To keep the free-search allowance working
  across reinstalls without requiring you to create an account or log in, the
  app derives a one-way, salted cryptographic hash (SHA-256) of your device’s
  Android ID. **The original Android ID is never transmitted or stored** — only
  the hash is sent, and it cannot be reversed to identify you or your device. It
  serves purely as an anonymous key for your trial counter.
- **Free-search usage count.** A single number recording how many free searches
  have been used, so the allowance can be enforced consistently.
- **An anonymous authentication identifier.** The app signs in to our backend
  using Firebase Anonymous Authentication. This creates a random, identity-less
  token — it contains no personal information and is used only to read and write
  your trial counter securely.
- **App integrity tokens.** Firebase App Check may generate attestation tokens
  confirming that requests come from a genuine, untampered copy of the app.
  These protect the backend from abuse and are not linked to your identity.
- **Purchase status.** If you buy the one-time “unlimited search” unlock, the
  store processes the payment — Google Play on Android, the App Store on iOS — and
  reports back whether your account owns the unlock. The app stores only whether
  search is unlocked; it never sees or stores your payment details. This is the one
  item that applies to both platforms.

## Information the app does *not* collect

- No name, email address, phone number, or account credentials.
- No precise or approximate location.
- No contacts, photos, files, or messages.
- No advertising identifiers, and no advertising of any kind.
- No analytics profiling and no tracking across other apps or websites.
- Your reading activity — which passages you open or how you navigate — stays
  entirely on your device and is never transmitted.

## How we use this information

- To count free searches and enforce the free-search allowance.
- For security and fraud prevention — the server-side, hashed counter stops the
  free trial from being reset simply by clearing app data or reinstalling.
- To apply and restore your one-time purchase on your Google account.

## Where the data goes (service providers)

On Android, the hashed key and search count are stored in **Google Cloud
Firestore**, accessed through **Firebase Authentication** and **Firebase App
Check**. Purchases are handled by **Google Play Billing** on Android and by the
**App Store** on iOS. The iOS build sends nothing to Firebase, because it holds its
counter locally. These Google services act as
our data processors, handling the data on our behalf. All data is transmitted
over encrypted connections (HTTPS/TLS). Google’s handling of data is governed by
the [Google Privacy Policy](https://policies.google.com/privacy).

## Data sharing

We do not sell your data and do not share it with third parties for their own
purposes or for advertising. The information described above is processed only
by Google as our service provider, solely to provide the functionality above.

## Data retention

The hashed device key and free-search count are retained so that the free
allowance remains consistent across reinstalls; this is by design, to prevent
trial resetting. Because the key is a non-reversible hash and we hold no
personal information, this data cannot be used to identify you.

## Deleting your data

You can ask us to delete the hashed device key and free-search count held for your
device: write to the address under *Contact* and say that you are requesting
deletion. Because the key is a non-reversible hash, we cannot look you up from your
name or email — include the request from the device you used, or ask us how to
supply the key, and we will confirm what was removed. On iOS there is nothing to
request: we hold nothing. The count stays in your device's keychain, which keeps it
across a reinstall; erasing the device removes it.

## Children

The app is not directed to children under 13 and does not knowingly collect
personal information from children.

## Changes to this policy

We may update this policy from time to time. Material changes will be reflected
here with a revised “Last updated” date.

## Contact

For any questions about this policy or the data described here, contact:

Evangelos Prokopiou — <vagelis.prokopiou@gmail.com>

---

© 2026 Evangelos Prokopiou. Koine Advanced Indexer privacy policy.
