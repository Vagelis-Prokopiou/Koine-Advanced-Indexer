# Privacy Policy — Greek New Testament

_Draft, effective 2026-07-07. This is a template that accurately describes the
app's current data practices; have it reviewed before publishing, then host it
at a public URL and link that URL in Google Play (Play requires a reachable
privacy-policy URL)._

**App:** Greek New Testament (`eu.esxata.koine`)
**Contact:** vangelis.p@compliancesolutions.com

## Summary

The app is a reader and search tool for the Greek New Testament. **Reading and
searching happen entirely on your device** — the biblical text and the search
index are bundled in the app, and **your search queries are never transmitted or
logged.** The only data that leaves your device is what is needed to enforce the
free-search trial and to process an optional one-time purchase.

## What we collect and why

| Data | Purpose | Where it goes |
|---|---|---|
| A salted, irreversible **hash of your device identifier** (`ANDROID_ID`) | Enforce the free-search trial limit consistently, including across reinstalls | Google Firebase (Firestore + Anonymous Authentication) |
| A **count of free searches used** | Track how many free searches remain before the one-time unlock | Stored alongside the device hash in Firebase |
| **Purchase entitlement** (whether the one-time unlock was bought) | Unlock unlimited search | Processed by Google Play Billing; the app stores only an on-device "unlocked" flag |

We do **not** collect your name, email address, account, contacts, precise or
approximate location, photos, or the contents of your searches. We do not use
advertising or third-party analytics/tracking SDKs.

The device hash is a one-way SHA-256 with a fixed salt; we never store or
transmit the raw device identifier, and the hash is used only as an anonymous key
for the trial counter.

## Anonymous authentication

To store the trial counter securely, the app signs in to Firebase
**anonymously**. This creates an anonymous identifier managed by Firebase; it is
not linked to any personal account, email, or sign-in on your part.

## Service providers

- **Google Firebase** (Firestore, Authentication) processes the trial-counter
  data on our behalf. See Google's Privacy Policy: <https://policies.google.com/privacy>.
- **Google Play Billing** processes any purchase. We never receive or store your
  payment or financial details.

## Data security and retention

Data in transit is encrypted (TLS). Trial-counter data is stored in Google's
infrastructure and retained while the app remains in use. Because the record is
keyed to an anonymous device hash (not to you personally), we cannot identify who
it belongs to, but you may request deletion of the record associated with your
device by contacting us at the address above.

## Children

The app is intended for a general audience and is not directed at children.

## Changes

We may update this policy; material changes will be reflected here with a new
effective date.

## Contact

Questions or deletion requests: vangelis.p@compliancesolutions.com
