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

- **Status:** completed
- **Done:** Tasted 2026-11-15 on the Cosori Juni (`cone`, Barista Mode `Roast Test 1`, 15 g / 240 g, Opus 2 `6`). All three cups were weak with `bitterness: 1`, `acidity: 2`, `sweetness: 3`, and light grassy notes. Body and overall score rose steadily with roast time: 14 min (`2/10`, `body: 1`), 16 min (`3/10`, `body: 2`), 18 min (`5/10`, `body: 3`).
- **What:** Brew roasts 2026-11-10-01, 2026-11-11-01 and 2026-11-11-02 side by side with one recipe, about 2026-11-15 to 2026-11-17. Record a `tasting` entry in each roast file. The result decides the last two batches of the Costa Rica La Rosa (183.6 g left).

### TASTE-02: Re-taste 18 min with Colin's daily 30 g / Opus 3.5 recipe

- **Status:** completed
- **Done:** Brewed 2026-11-15 (`30 g` of 2026-11-11-02 at Opus 2 `3.5` after an intermediate `15 g : 240 g` test at `4.5` was also weak). Better, but still weak/flat — confirming the 30-month-old green coffee is past its prime for flavor evaluation.
- **Depends on:** TASTE-01
- **What:** Brew 30 g of 2026-11-11-02 (18 min; ~46.2 g remains) using Fellow Opus 2 at `3.5` and Colin's normal daily Cosori Juni recipe. Log the `tasting` entry and recipe parameters before planning Batch 4 (183.6 g green left).
- **Why:** Moving from `6` to `4.5` at `15 g : 240 g` was still "super weak." Testing Colin's proven daily `30 g` / `3.5` setup compares directly against his daily Colombian reference and separates Juni bed depth / grind calibration from the 30-month green-bean age.

### ROAST-03: Test smaller batch size (H3) and curve shape (H1)

- **Status:** in-progress
- **Depends on:** TASTE-02
- **Batch 4 (`2026-11-16-01`, recorded):** `P01`, `70.0 g`, `16 min` → `64.4 g` roasted (`8.0 %` loss vs `12.0 %` at `90.0 g` in `2026-11-11-01`). Smaller load roasted slower/lighter.
- **Next (`2026-11-16-02`, planned):** `P01`, `90.0 g`, `10 min` vs `2026-11-11-02` for H1 (cold start >= 30 min after Batch 4). Combined checklist: `print/2026-11-16-test-roasts-sheet.pdf`.
- **What:** Run both machine-calibration tests with the remaining Costa Rica La Rosa green coffee (photos at the checkpoint times + cooled weights; no brewing needed).
- **Why:** Tasting showed the 30-month-old lot is too flat for cup tuning, so use the remaining green coffee to settle H3 and H1 in `reference/roaster-profile.md`.

### ROAST-04: First roast of the Colombia Huila Santa Maria (fresh lot)

- **Status:** in-progress
- **Planned:** `roasts/2026-11-19-01-colombia-huila-santa-maria-washed-2026a.md` (`P01`, `108.0 g`, `18 min`, target about 90 g roasted). Printable sheet: `print/2026-11-19-01-roast-sheet.pdf`.
- **What:** Roast, record, rest at least 4 days, then taste with Colin's daily Juni recipe (`30 g`, Opus 2 `3.5`).
- **Why:** First fresh coffee on this machine, so the first cup results worth tuning against. Also the first load above 90 g (H3).
- **Order:** Cold start. If 2026-11-16-02 (ROAST-03) runs the same day, roast this one first and wait at least 30 min.

## App

### APP-01: Design the roast companion app

- **Status:** deferred
- **Unblock when:** about five roasts are recorded and the roast-file fields have stopped changing.
- **What:** Write a design for an Android app (iOS later, possibly) that runs a count-up timer synced to the roaster's countdown, logs events with one tap (first crack, second crack, cool pressed), records weights and room conditions, and imports and exports the roast files in this repository's front-matter format. Decide whether the app lives in this repository or its own.
- **Constraint:** App work happens on a branch and is not pushed until Colin asks.
