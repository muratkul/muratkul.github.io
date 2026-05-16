---
layout: default
title: Ads
---

> **Languages:** **English** · [Türkçe](./ads-tr) · [Español](./ads-es)

# Ads in Sudoku Arena Online

Sudoku Arena Online is free to play. The work behind the puzzle
generator, the multiplayer matchmaking, and the daily challenge is
supported by advertising. This page explains exactly what ads we show,
where they show up, and how we configure them — written in plain
language so you can decide what you're comfortable with before you
play.

For the full data-collection picture, see the
[Privacy Policy](./privacy-policy). For the contractual side, see the
[Terms of Service](./terms-of-service).

---

## Who serves the ads

We use **Google AdMob**, operated by Google LLC. Every ad you see
inside Sudoku Arena Online is delivered through AdMob's network. We
do not embed any other advertising SDK — no Meta Audience Network, no
Unity Ads, no IronSource, no in-app webview ads of any kind.

AdMob's policies and how Google uses the information it collects on
our behalf:

- [How Google uses information from sites or apps that use our services](https://policies.google.com/technologies/partner-sites)
- [Google AdMob & AdSense privacy practices](https://support.google.com/admob/answer/6128543)

---

## Where ads appear

There are four possible ad slots in the app. Whether each one is
active is controlled by a runtime configuration value (Firebase
Remote Config) that we can adjust without releasing a new build. At
launch we ship with the most conservative setup possible — only the
rewarded slot is on.

| Slot | When | Default at launch |
|---|---|---|
| **Rewarded — "Watch ad for an extra hint"** | After you spend your free hint, an optional play-icon appears on the hint button. Tapping it loads a short rewarded video; on completion you receive one extra hint. Declining or closing the ad does nothing. | **On** (user-initiated only) |
| **Banner — Home & match-result screens** | A small banner sits at the bottom of the home screen and the end-of-match modal. Never overlays the board or any tappable game UI. | **Off** at launch |
| **Banner — In-game** | A small banner sits below the number pad while you play. Same hands-off placement — never on the board. | **Off** at launch |
| **Interstitial — Match start** | A full-screen ad before a multiplayer match begins, with a clear Close button. Shown at most once per match. | **Off** at launch |

The Pro subscription (planned, not yet released) removes all four
slots. We do not currently sell a Pro upgrade in this version.

---

## What information AdMob receives

We have configured AdMob to request **non-personalised ads only**
(`npa=1`). In practice that means:

- AdMob is told **not** to use any identifier on your device to build
  or update a profile of you.
- The ads you see are chosen based on contextual signals — the type
  of app (puzzle game), the country derived from your IP address, and
  the device language. Not based on your past behaviour.
- We do **not** show Apple's App Tracking Transparency prompt because
  the app does not enable cross-app tracking. The ATT prompt is for
  apps that do.

AdMob still uses your platform's advertising identifier
(**Apple IDFA** on iOS or **Google AAID** on Android) for **fraud
detection** and for Apple's
[SKAdNetwork](https://developer.apple.com/documentation/storekit/skadnetwork)
attribution framework. This use is policy-bound — Google does not get
to use these identifiers to advertise to you elsewhere.

You can:

- **iOS**: Settings → Privacy & Security → Apple Advertising → toggle
  *Personalised Ads* off, or reset your IDFA from the same screen.
- **Android**: Settings → Google → Ads → toggle *Opt out of Ads
  Personalisation* and reset your Advertising ID.

When ad tracking is limited, AdMob still serves non-personalised ads
in the app — you don't lose any functionality.

---

## What information we (the developer) see

The only ad-related data we receive from AdMob is the **aggregate
revenue and impression count** in the AdMob console — totals like
"X impressions yesterday, Y CPM, Z USD revenue", per ad unit, per
country. We never see anything about you as an individual: not the
ads you saw, not whether you clicked them, not what time of day you
played.

---

## How to reach us

If anything on this page is unclear, or you spotted an ad that looked
inappropriate for our 4+ rating, please write to
**nfvwzhbrbw@privaterelay.appleid.com** with a screenshot. AdMob lets
us block specific advertisers per category, and we use this regularly
to keep the experience clean.

---

## Changes to this page

Material changes to the ad setup (for example, adding a new ad SDK or
turning on a placement that was previously off) will be reflected here
first. The
[Privacy Policy](./privacy-policy) will be updated at the same time,
with the "Last updated" date bumped at the top so you can tell when
something changed.

Last updated: May 16, 2026
