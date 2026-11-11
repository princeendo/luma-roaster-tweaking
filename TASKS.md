# Tasks

The only status tracker. Update it in the same change that completes, adds or blocks a task.

Status values: `pending`, `in-progress`, `blocked`, `deferred`, `completed`.

## Roasting

### SETUP-01: Record the roaster's nameplate

- **Status:** completed
- **Done:** 120 V, 60 Hz, 1,400 W, recorded 2026-11-11.
- **What:** Read the rating label on the base. Record voltage, frequency and power in `reference/roaster-profile.md` and close H7.
- **Why:** The manual is written for 220–240 V. A 120 V unit may heat differently, which would make the manual's times unreliable.

### SETUP-02: Add the first green coffee

- **Status:** completed
- **What:** Create `beans/<bean_id>.md` for each coffee on hand.
- **Done:** `beans/costa-rica-la-rosa-washed-2024a.md`. Add a file for any other coffee when it is first roasted.

### ROAST-01: Baseline roast

- **Status:** completed
- **Result:** `roasts/2026-11-10-01-costa-rica-la-rosa-washed-2024a.md` (P01, 90 g, set 14 min). Roasted 2026-11-10: weights recorded (10.2 % loss), no first crack heard, judged `light` from photos, timer ran out at 14:00. Tasting still to come.
- **Depends on:** SETUP-02
- **What:** Plan and record the first roast at about 100 g. Set the timer longer than needed and press Power to cool based on first crack. Log first-crack time and weight loss.

### ROAST-02: Test whether the time setting changes the curve (H1)

- **Status:** completed
- **Result:** inconclusive for H1. 14, 16 and 18 min roasts gave 10.2 %, 12.0 % and 15.3 % weight loss, so the set time reliably controls roast level. Color change at about 07:30 (16 min) and 08:00 (18 min) is too rough to tell a fixed curve from a stretched one. H1 stays open in `reference/roaster-profile.md` with a sharper test.
- **Third roast:** `roasts/2026-11-11-02-costa-rica-la-rosa-washed-2024a.md` (P01, 90 g, set 18 min).
- **First pair:** `roasts/2026-11-11-01-costa-rica-la-rosa-washed-2024a.md` (P01, set 16 min against the 14 min baseline). Roasted 2026-11-11: darker than the baseline, color change about 07:30. 12.0 % loss against 10.2 %. H1 is still open because the baseline has no color-change time.
- **Depends on:** ROAST-01
- **What:** Two roasts of the same bean and weight at different set times. See H1 in `reference/roaster-profile.md`.
- **Why:** The answer decides whether "long timer, manual cool" is a valid way to control the roast.

### TASTE-01: Taste the 14/16/18 min series

- **Status:** pending
- **What:** Brew roasts 2026-11-10-01, 2026-11-11-01 and 2026-11-11-02 side by side with one recipe, about 2026-11-15 to 2026-11-17. Record a `tasting` entry in each roast file. The result decides the last two batches of the Costa Rica La Rosa (183.6 g left).

## App

### APP-01: Design the roast companion app

- **Status:** deferred
- **Unblock when:** about five roasts are recorded and the roast-file fields have stopped changing.
- **What:** Write a design for an Android app (iOS later, possibly) that runs a count-up timer synced to the roaster's countdown, logs events with one tap (first crack, second crack, cool pressed), records weights and room conditions, and imports and exports the roast files in this repository's front-matter format. Decide whether the app lives in this repository or its own.
- **Constraint:** App work happens on a branch and is not pushed until Colin asks.
