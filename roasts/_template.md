---
roast_id: YYYY-MM-DD-NN
status: planned
date: YYYY-MM-DD
bean_id: null
baseline_roast: null
goal: null
changed_variable: null

plan:
  mode: null
  set_time_min: null
  p03_set_temp_c: null
  green_weight_g: null
  target_roast_level: null
  expected_first_crack: null
  stop_rule: null

environment:
  ambient_temp_c: null
  ambient_humidity_pct: null
  location: null
  outlet: null
  warm_start: null
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
notes: null
---

# Roast YYYY-MM-DD-NN: <bean name>

## Plan rationale

Why these settings. Label each point **manual**, **observed** (with roast IDs), or **external guidance**. Give a confidence percentage and the main uncertainty.

## During the roast

Running notes: sounds, smells, smoke, bean movement, anything odd.

## Tasting

Free-text impressions that do not fit the `tasting` entries.

## Next time

The one change to try next, and why.
