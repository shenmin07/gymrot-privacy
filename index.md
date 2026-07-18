# Privacy Policy — GymRot

**Effective date:** July 17, 2026
**Provided by:** the developer of GymRot
**Contact:** gymrotsupport@gmail.com


GymRot ("the app", "we") helps you earn screen time by completing workouts. This
policy explains what data the app handles and why. We designed GymRot to keep as
much data as possible **on your device**.

## Data we store on our backend

GymRot uses [Supabase](https://supabase.com) (a hosted Postgres database) to power
accounts, social features, and backup. When you sign in and use these features, we
store:

- **Account:** an identifier and email address from **Sign in with Apple** (often a
  private-relay address), and the **username** and **display name** you choose.
- **Profile photo:** if you set one, the photo you pick (downscaled) is stored so
  friends can see it on the leaderboard and requests.
- **Progress shown to friends:** your current **streak**, **avatar stage**, and
  **avatar customization** (the skin tone, outfit color, and hairstyle you pick
  for your character).
- **Friends:** friend requests and accepted friendships (the two user IDs and
  status).
- **Shared plans:** when you share a workout plan, a snapshot of that plan is stored
  so the recipient can import it.
- **Workout event log:** dates on which you completed a workout or took a rest day
  (used to compute your streak on the server). This does **not** include your
  location.
- **Schedule backup:** so a reinstall + sign-in restores your setup, we store your
  weekly schedule (days, times, lengths, intensities), your **workout plans**
  (exercises, sets/reps/weights), your **saved gym locations** (the names,
  coordinates, and radius of the gyms you added — not your movements), your home-gym
  choice, your **bodyweight** (if set), and your unit preference.
- **Crash diagnostics:** if the app crashes or misbehaves, Apple's MetricKit
  produces a diagnostic report (stack traces, app/OS version, device model) that we
  upload to a write-only table to fix the problem. These reports never contain your
  location, health data, or content.

Access to this data is restricted by row-level security: users can only read their
own data plus the limited friend data (name, photo, streak, avatar stage and
style) needed
for the leaderboard. Crash reports are write-only — not even you can read them back
through the app.

## Data that stays on your device (never sent to us)

- **Your live location.** Checking whether you're at one of your saved gyms
  (geofencing) happens entirely on-device. No location fix, movement, or visit
  history is ever transmitted. (Only the gym *places* you deliberately save are
  included in the schedule backup, as described above.)
- **Blocked-app selection.** The apps you choose to block are handled by Apple's
  Screen Time / Family Controls framework as opaque tokens on your device and
  **cannot** be read or transmitted by us.
- **Workout logs.** The set-by-set history of your finished sessions stays in the
  on-device database.
- **AI prompts and plans.** The optional "Generate with AI" feature uses **Apple
  Foundation Models**, which run entirely on your device. Prompts and generated
  plans are not sent to us or any third party.

## Apple Health (optional)

If you turn on **"Save workouts to Health"** (Profile → You), the app **writes**
your finished workouts (type, duration, calories) into Apple Health on your device.
This is one-way: GymRot requests **no read access** and never receives any data
from Health. You can revoke access anytime in the Health app.

## How we use data

We use the data above only to provide the app's features: authentication, the
friends leaderboard, plan sharing, restoring your setup after a reinstall, and
fixing crashes. We do **not** sell your data, use it for advertising, or include
third-party tracking or analytics.

## Third parties

- **Apple** — Sign in with Apple (authentication), on-device Foundation Models, and
  Apple Health (only if you enable the export; data flows from us to Health, never
  back).
- **Supabase** — database, storage, and authentication hosting (data processor for
  the data listed above).

## Data retention & deletion

You can **delete your account at any time** in the app: **Home → profile icon →
Profile → Delete account.** This permanently deletes your profile, photo,
friendships, shared plans, workout-event history, schedule backup, and crash
reports from our backend. On-device data is removed when you delete the app;
workouts you exported to Apple Health belong to your Health database and can be
deleted there.

## Children

GymRot is not directed at children under 13, and we do not knowingly collect data
from them.

## Changes

We may update this policy; material changes will be reflected by a new effective
date at the top.

## Contact

Questions about this policy or your data: **gymrotsupport@gmail.com**.
