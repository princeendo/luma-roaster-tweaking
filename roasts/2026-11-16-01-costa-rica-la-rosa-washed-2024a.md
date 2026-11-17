---
roast_id: 2026-11-16-01
status: planned
date: 2026-11-16
bean_id: costa-rica-la-rosa-washed-2024a
baseline_roast: 2026-11-11-01
goal: "Test H3 (batch size vs. speed): see whether reducing load 90.0 -> 70.0 g on P01 (16 min) roasts faster and darker."
changed_variable: "green weight 90.0 → 70.0 g"

plan:
  mode: P01
  set_time_min: 16
  p03_set_temp_c: null
  green_weight_g: 70.0
  target_roast_level: city_plus
  expected_first_crack: null
  stop_rule: "Let the timer run out at 16:00. Press Power to cool early only on second-crack sounds (fast, quiet crackle), heavy smoke, or an oily sheen on the beans."

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
notes: "Planned 2026-11-16 as machine-calibration Batch 4 (H3) using the remaining Costa Rica La Rosa green coffee (183.6 g expected in bag; leaving ~113.6 g for a 90 g H1 test next). If roasted on another day, rename the file and roast_id."
---

# Roast 2026-11-16-01: Costa Rica La Rosa

## Plan rationale

Baseline is roast [2026-11-11-01](2026-11-11-01-costa-rica-la-rosa-washed-2024a.md) (`P01`, `90.0 g`, `16 min` → `12.0 %` weight loss, `city`, color change ~`07:30`). The one changed variable is batch weight: `90.0 → 70.0 g`.

- **Why test batch size (`H3`).** At `90.0 g` on `P01`, `14 min` gave `10.2 %` (`light`), `16 min` gave `12.0 %` (`city`), and the `18 min` maximum gave `15.3 %` (`city_plus`) (**observed**, `2026-11-10-01`, `2026-11-11-01`, `2026-11-11-02`). That is slower than the 7–12 min range typical of small air roasters (**external guidance**), likely because this unit is `120 V / 1,400 W` rather than `220–240 V / 1,500 W` (**observed** nameplate vs **manual**). Dropping to `70.0 g` tests whether a smaller load heats faster.
- **Why `70.0 g`.** Well below the `120 g` **manual** limit and `20 g` (`22 %`) lighter than the `90 g` baseline — large enough to show a clear difference in weight loss and movement without dropping to a tiny load that flies around (**external guidance**). Leaving ~`113.6 g` in the bag also preserves a full `90.0 g` batch for the `H1` `10 min` test next.
- **Why `16 min` instead of `18 min`.** Using `16 min` leaves room above the expected roast level: if `70 g` speeds up noticeably, `18 min` could overshoot into heavy smoke or scorching, whereas `16 min` gives a clean comparison against `2026-11-11-01`'s `12.0 %` loss (**observed**).
- **Same program (`P01`).** Washed coffee (**manual**), matching the baseline.
- **What to expect.** Likely `13.5–15.5 %` weight loss (`59.2–60.6 g` roasted) and earlier color change (around `05:30–06:30`) if less bean mass speeds heating; or lower weight loss if a sparser bed lets hot air bypass the beans. Also watch `bean_movement` closely for whether `70 g` circulates freely or bounces too high.

**Confidence: 60 %** that `70.0 g` at `16 min` finishes darker than `2026-11-11-01` (`>12.0 %` loss) without reaching second crack. The main uncertainty is `H3`: in a fluid-bed roaster, smaller batches have less thermal mass to heat (faster) but can also absorb less heat from the airstream (slower). Room temperature differences vs `2026-11-11` are a second uncertainty.

## Before the roast

1. Weigh the rest of the green bag first if convenient so we can verify `green_weight_remaining_g`.
2. Same place and same outlet as earlier roasts. Nothing else large on that circuit (`1,400 W` draws ~`11.7 A`).
3. Start with a cold roaster. Empty the chaff bin and clean the intake screen.
4. Weigh `70.0 g` of green beans and check they sit well below the MAX fill line (**manual**).
5. Note room temperature (`ambient_temp_c`).
6. Have a count-up stopwatch ready (or note countdown times: elapsed = `16:00 - display`).

## During the roast

1. Hold Power `3 s`, choose `P01`, press Power, turn to `16`, press Power, and start the stopwatch. Stay with the roaster the whole cycle (**manual**).
2. Watch `bean_movement` early and mid-roast (do the `70 g` beans circulate smoothly or bounce high/fly?).
3. Snap quick photos looking into the chamber at `06:00`, `08:00`, and `12:00`, and note approximate `color_change` and any `smoke_noticeable` or faint cracks.
4. Let the timer run out at `16:00`. Press Power early only on second-crack sounds, heavy smoke, or an oily sheen.
5. Wait until cooling finishes and the unit returns to standby before unloading (**manual**). Record `cooling_end`.

## After the roast

1. Weigh the cooled roasted beans without chaff (`roasted_weight_g`).
2. Take one photo of the cooled beans and note chaff amount, color evenness, and any scorching or tipping.
3. Empty the chaff bin (no brewing needed).

## During the roast (notes)

## Tasting

## Next time
