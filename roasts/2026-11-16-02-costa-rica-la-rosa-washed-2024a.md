---
roast_id: 2026-11-16-02
status: planned
date: 2026-11-16
bean_id: costa-rica-la-rosa-washed-2024a
baseline_roast: 2026-11-11-02
goal: "Test H1 (fixed curve vs. stretched curve): compare color change and 10:00 weight loss on P01 90.0 g set to 10 min against the 18 min baseline."
changed_variable: "set time 18 → 10 min"

plan:
  mode: P01
  set_time_min: 10
  p03_set_temp_c: null
  green_weight_g: 90.0
  target_roast_level: cinnamon
  expected_first_crack: null
  stop_rule: "Let the timer run out at 10:00. Press Power early only on heavy smoke or an error."

environment:
  ambient_temp_c: null
  ambient_humidity_pct: null
  location: null
  outlet: null
  warm_start: false
  minutes_since_last_roast: null

actual:
  mode: null
  set_time_min: null
  p03_set_temp_c: null
  green_weight_g: null
  roasted_weight_g: null
  heating_end: null
  heating_end_reason: null
  cooling_end: null
  error_codes: []

events:
  color_change: null
  first_crack_start: null
  first_crack_rolling: null
  first_crack_end: null
  second_crack_start: null
  smoke_noticeable: null

results:
  weight_loss_pct: null
  development_time: null
  development_ratio_pct: null
  roast_level: null
  color_whole: null
  color_ground: null
  color_method: null
  evenness: null
  defects: []
  chaff_amount: null
  bean_movement: null

tasting: []

next_time: null
notes: "Planned 2026-11-16 as machine-calibration Batch 5 (H1) using the remaining Costa Rica La Rosa green coffee (after the 70 g Batch 4 roast). Must be a cold start (>= 30 min after Batch 4 ends). If roasted on another day, rename the file and roast_id."
---

# Roast 2026-11-16-02: Costa Rica La Rosa

## Plan rationale

Baseline is roast [2026-11-11-02](2026-11-11-02-costa-rica-la-rosa-washed-2024a.md) (`P01`, `90.0 g`, `18 min` → `15.3 %` weight loss, `city_plus`, color change ~`08:00`). The one changed variable is the timer setting: `18 → 10 min`.

- **Why test `H1` (`10 min` vs `18 min`).** Earlier `14`, `16`, and `18 min` roasts showed darker roasts with longer set times (**observed**, `2026-11-10-01`, `2026-11-11-01`, `2026-11-11-02`), and `color_change` estimates were ~`07:30` at `16 min` and ~`08:00` at `18 min`. That half-minute gap is too rough to tell whether `P01` uses one fixed heating curve or stretches its curve proportionally to the timer setting.
- **How `10 min` settles it without stopwatch-second timing.**
  - **If stretched curve:** `color_change` shifts ~`3.5 min` earlier to around `04:30`, and the beans finish brown near `10:00` with ~`10–15 %` weight loss.
  - **If fixed curve:** beans stay green past `05:00`, change color around `07:30–08:00`, and finish `10:00` pale/underdeveloped with low weight loss.
- **Same program (`P01`) and weight (`90.0 g`).** Matches the `14`/`16`/`18 min` baseline series (**manual** for washed coffee on `P01`).
- **Cold start.** Wait at least `30 minutes` after Batch 4 (`2026-11-16-01`) cools before starting so a warm roaster does not speed up heating (**external guidance**).

**Confidence: 85 %** that the combined evidence of `04:30` / `06:00` / `08:00` photos plus `10:00` weight loss cleanly settles `H1`. The main uncertainty is `ambient_temp_c` or residual heat if started less than 30 minutes after Batch 4.

## Before the roast

1. Confirm the roaster is fully cool (`>= 30 min` since Batch 4 ended) and record `minutes_since_last_roast`.
2. Same place and outlet as Batch 4. Empty the chaff bin and clean the intake screen.
3. Weigh `90.0 g` of green beans (record any remainder in the bag). Check below MAX fill line (**manual**).
4. Have phone camera and count-up stopwatch ready.

## During the roast

1. Hold Power `3 s`, choose `P01`, press Power, turn to `10`, press Power, and start the stopwatch. Stay with the roaster the whole cycle (**manual**).
2. Snap a quick photo looking into the chamber at **`04:30`**, **`06:00`**, and **`08:00`** (with the roaster's countdown visible in frame if possible).
3. Let the `10:00` timer run out.
4. Wait until cooling returns to standby before unloading (**manual**). Record `cooling_end`.

## After the roast

1. Weigh the cooled roasted beans without chaff (`roasted_weight_g`).
2. Take one photo of the cooled beans (no brewing needed).
3. Empty the chaff bin.

## During the roast (notes)

## Tasting

## Next time
