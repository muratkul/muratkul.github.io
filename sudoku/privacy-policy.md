---
layout: default
title: Privacy Policy
---

> **Languages:** **English** · [Türkçe](./privacy-policy-tr) · [Español](./privacy-policy-es)

# Privacy Policy

**Effective date:** May 16, 2026
**Last updated:** May 16, 2026

This Privacy Policy explains how **Sudoku Arena Online** ("the App",
"we", "us") collects, uses, and protects information when you use our
mobile application. The App is operated by **Murat Kul** ("the
developer"), based in Istanbul, Türkiye.

By using the App you agree to the practices described below. If you do
not agree, please do not use the App.

---

## 1. Who we are

| | |
|---|---|
| App name | Sudoku Arena Online |
| Developer | Murat Kul |
| Country | Türkiye |
| Contact | nfvwzhbrbw@privaterelay.appleid.com |

This is an indie project. We have no employees, no third-party data
processors beyond the infrastructure providers listed below, and no
advertising or marketing partners.

---

## 2. What we collect

We collect only what is necessary to make the App work and to serve
non-personalised ads. We do **not** collect contacts, photos,
location, health data, or financial data.

### 2.1 Account data

When you sign in with **Google** or **Apple** we receive the following
from the identity provider:

- A unique user identifier (Firebase UID)
- Display name
- Email address (Apple may return a Private Relay address)
- Profile photo URL (a reference, not the image bytes)

If you choose **Continue as Guest**, we only generate an anonymous
Firebase UID. No name, email, or photo is collected.

### 2.2 Gameplay data

To run the multiplayer service we store the following on Firestore:

- Active matches you participate in: puzzle, status, players, mistakes,
  filled-cell counts, finish time, winner UID
- Matchmaking ticket while you are searching for an opponent: your UID,
  display name, photo URL, mode, difficulty, timestamp
- A reference to your active match (`currentMatchId`) on your user
  document

### 2.3 On-device data

The following stays on your device only and is never sent to our
servers:

- Your saved single-player session ("Continue") and game settings, in
  the local Hive database
- Your theme, language, haptics, and other preferences, in
  SharedPreferences

### 2.4 Advertising data

The App uses Google AdMob to serve ads. AdMob may collect or process
the following on our behalf:

- **Apple's Advertising Identifier (IDFA)** on iOS — used by AdMob to
  prevent ad fraud and to attribute installs via Apple's SKAdNetwork
  framework. We request only **non-personalised ads** (`npa=1`), which
  means AdMob does **not** use the IDFA to build an advertising
  profile of you. We do not show the App Tracking Transparency prompt
  because we do not enable cross-app tracking.
- **Google Advertising ID (AAID)** on Android — equivalent role to
  IDFA, with the same non-personalised configuration.
- **Coarse signals** that AdMob needs to comply with COPPA / GDPR /
  IAB TCF (e.g. country, device model, OS version, IP address used
  only to derive country). These are processed by Google and never
  surfaced to us as developers.
- **Reward signals** when you choose to watch a rewarded ad in
  exchange for an extra hint — limited to "did the user complete the
  watch?", never the contents of the ad.

You can turn off Limit Ad Tracking on iOS (Settings → Privacy &
Security → Apple Advertising) or reset your Advertising ID on Android
(Settings → Google → Ads). When Limit Ad Tracking is on, AdMob still
serves non-personalised ads but with reduced fraud detection signals.

---

## 3. Why we collect it

| Purpose | Data used |
|---|---|
| Sign you in and identify your matches | Account data |
| Pair you with another player | Matchmaking ticket, account data |
| Run a match and let your opponent see your progress | Gameplay data |
| Show your "Continue" card on the home screen | On-device data |
| Serve non-personalised ads + fraud-check the request | Advertising data |
| Attribute installs through Apple's SKAdNetwork | Advertising data |

We do **not** sell your data to third parties, build a marketing
profile from it, or share it with data brokers. The advertising
identifiers listed in section 2.4 are used **only for non-personalised
ads and fraud detection**; we have not enabled any tracking SDK,
attribution SDK, or audience-segmentation feature.

---

## 4. Third-party services

The App uses **Firebase**, operated by Google LLC, as its backend:

- **Firebase Authentication** — handles sign-in with Google, Apple, or
  anonymous mode.
- **Cloud Firestore** — stores match documents and user records.
- **Firebase Remote Config** — fetches runtime configuration
  (matchmaking timeouts, ad placement flags, etc.). No personal data
  is sent — only a generic install identifier so Google can deliver
  the right config payload.
- **Firebase Crashlytics** — records non-personalised crash
  diagnostics, sent only when the App crashes.
- **Google Sign-In** and **Sign in with Apple** — federated identity
  providers.

The App also embeds **Google AdMob** (operated by Google LLC) to
serve ads. See section 2.4 for what AdMob collects and how it's
configured.

These services act as **data processors** on our behalf. They do not
own your data. Their privacy practices are described at:

- [Google Privacy Policy](https://policies.google.com/privacy)
- [How Google uses information from sites or apps that use our services](https://policies.google.com/technologies/partner-sites)
- [Apple Privacy Policy](https://www.apple.com/legal/privacy/)

The list of third-party services may change in future versions;
section 11 covers how we communicate those updates.

---

## 5. Data location and security

Data is stored in Google Cloud regions used by Firebase (typically
`us-central1` or another region selected by Firebase). All traffic
between the App and Firebase uses TLS encryption. Firestore encrypts
data at rest by default.

---

## 6. Retention

We keep your data only as long as your account is active:

- **Account record** (`users/{uid}`) — until you delete your account.
- **Matchmaking ticket** — auto-deleted within 30 seconds (timeout) or
  immediately when a match is found / you cancel.
- **Match documents** — kept indefinitely so that both participants can
  see their history. They contain no information beyond UID,
  display name, and the metrics listed in section 2.2.
- **On-device data** — until you uninstall the App.

---

## 7. Your rights

If you are in the European Economic Area, the United Kingdom, or
Türkiye (KVKK), you have the right to:

- Access the personal data we hold about you
- Correct inaccurate data
- Delete your data ("right to erasure")
- Export your data in a portable format
- Object to or restrict processing
- Lodge a complaint with your local data protection authority

To exercise any of these rights, email
**nfvwzhbrbw@privaterelay.appleid.com**. We respond within 30 days.

---

## 8. Account deletion

You can delete your account at any time from inside the App:

> **Settings → Delete account**

This will:

1. Re-authenticate you with your sign-in provider (security check).
2. Permanently remove your user record and any pending matchmaking
   ticket from Firestore.
3. Permanently delete your Firebase Authentication user.
4. Sign you out.

After deletion, your UID may still appear inside historical match
documents you took part in, alongside the display name and photo URL
that were visible to your opponent during play. Those match documents
are not personally identifiable on their own.

If you cannot reach the in-app option for any reason, email us at
**nfvwzhbrbw@privaterelay.appleid.com** and we will delete your account
manually within 30 days.

---

## 9. Children

The App is **not directed to children under 13** (or the equivalent
minimum age in your jurisdiction). We do not knowingly collect data
from children. If you believe a child has provided us with personal
data, contact us and we will delete it.

---

## 10. International transfers

The App is built in Türkiye but the underlying infrastructure (Google
Firebase) may transfer data outside of Türkiye and the EEA. Google's
infrastructure uses standard contractual clauses approved by the
European Commission for these transfers.

---

## 11. Changes to this policy

We may update this Privacy Policy from time to time. The "Effective
date" at the top of this page reflects the most recent version. For
material changes we will post a notice in the App at least 7 days
before the new policy takes effect.

---

## 12. Contact

For any privacy question, request, or complaint:

> **Murat Kul**
> nfvwzhbrbw@privaterelay.appleid.com
> Istanbul, Türkiye
