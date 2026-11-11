---
roast_id: 2026-11-11-01
status: roasted
date: 2026-11-11
bean_id: costa-rica-la-rosa-washed-2024a
baseline_roast: 2026-11-10-01
goal: "More development than 2026-11-10-01: reach city to city_plus, 12-13.5 % weight loss."
changed_variable: "set time 14 → 16 min"

plan:
  mode: P01
  set_time_min: 16
  p03_set_temp_c: null
  green_weight_g: 90.0
  target_roast_level: city_plus
  expected_first_crack: null
  stop_rule: "Let the timer run out at 16:00. Press Power to cool early only on second-crack sounds (fast, quiet crackle) or heavy smoke."

environment:
  ambient_temp_c: null
  ambient_humidity_pct: null
  location: null
  outlet: null
  warm_start: null
  minutes_since_last_roast: null

actual:
  mode: P01
  set_time_min: 16
  p03_set_temp_c: null
  green_weight_g: null
  roasted_weight_g: null
  heating_end: "16:00"
  heating_end_reason: timer
  cooling_end: null
  error_codes: []

events:
  color_change: "07:30"
  first_crack_start: null
  first_crack_rolling: null
  first_crack_end: null
  second_crack_start: null
  smoke_noticeable: null

results:
  weight_loss_pct: null
  development_time: null
  development_ratio_pct: null
  roast_level: city
  color_whole: null
  color_ground: null
  color_method: null
  evenness: null
  defects: []
  chaff_amount: null
  bean_movement: null

tasting: []

next_time: null
notes: "Roasted 2026-11-11. expected_first_crack is null because first crack was not heard in the baseline. color_change is Colin's estimate (around 7.5 minutes). roast_level was judged by the agent from Colin's photo and his description, not in person. Program P01 is taken from the plan he followed. Green and roasted weights, room temperature and cooling end were not reported and stay null."
---

# Roast 2026-11-11-01: Costa Rica La Rosa

## Plan rationale

Baseline is roast 2026-11-10-01. The one change is the set time, 14 → 16 min.

- **Why longer.** P01 with 90 g ran the full 14 minutes and gave a `light` roast with 10.2 % weight loss, matte and slightly wrinkled beans, and no visible smoke. (**observed**, 2026-11-10-01) The seller's target for this coffee is light to medium, 30 s past the end of first crack. (**external guidance**, bag label)
- **Why 16 and not 15 or 18.** The unit is rated 120 V and 1,400 W, less than the manual's 1,500 W machine, and it reached only `light` in 14 minutes, so it gains roast level slowly. (**observed**, 2026-11-10-01) The manual's table moves one roast label for each 2–3 minutes. (**manual**) Two minutes should give a clear, measurable step without going dark. 18 is the maximum (**manual**) and leaves no room for a later step.
- **Why the timer and not the ear.** First crack was not heard over the fan. (**observed**, 2026-11-10-01) The set time is the control, and weight loss is the check.
- **Same program and weight.** P01 and 90.0 g, so the set time is the only difference. (**manual** for the program choice)
- **Expected result.** 12–13.5 % weight loss (77.9–79.2 g roasted), color close to the Colombian reference beans, smoother surfaces. City to city_plus is typically 13–15 % on fresh coffee (**external guidance**); this old, dry lot runs lower (**observed**, 2026-11-10-01).
- **What it tells us about H1.** If the set time only cuts off one fixed curve, this roast is the baseline plus two minutes and will be clearly darker. If the machine stretches its curve to fit the set time, the result will be close to the baseline. Compare the color-change time and the weight loss.

**Confidence: 60 %** that the roast lands at city to city_plus with 12–13.5 % loss. The main uncertainty is H1: nobody yet knows how this machine uses the set time. The second is that a different room temperature would shift the result.

## Before the roast

1. Same place and same outlet as the baseline. Nothing else large on that circuit: the roaster draws about 11.7 A.
2. Start with a cold roaster. Empty the chaff bin and check the intake screen.
3. Weigh 90.0 g of green beans. Note the room temperature.
4. Close the kitchen up as far as is safe and stand close: listen for first crack between about 10:00 and 14:00.

## During the roast

1. Hold Power 3 s. Select P01, press Power. Turn to 16, press Power, and start the stopwatch on that press.
2. Record the elapsed time of the color change (green to yellow or tan), any cracking heard, and any visible smoke.
3. Let the timer run out. Press Power early only on second-crack sounds or heavy smoke, and record the time.
4. Record when cooling ends and the unit returns to standby.

Elapsed time is 16:00 minus the display.

## After the roast

1. Unload after standby. Weigh the roasted beans without chaff.
2. Photograph them beside the baseline roast and the Colombian reference.
3. Empty the chaff bin. Store airtight with the lid closed.

## What happened

Colin's report, 2026-11-11, with a photo of green beans, roast 2026-11-10-01, this roast and the Colombian light-medium reference side by side:

- The timer ran the full 16 minutes. No early stop.
- Color change at about 7.5 minutes.
- No cracks heard. Colin thinks the fan is too loud to hear them.
- The beans are definitely darker than roast 2026-11-10-01, but not quite as dark as the Colombian reference. In the photo they are a more even medium-light brown, with fewer pale beans.

Reading: one step darker than the baseline, recorded as `city`. The weight loss will confirm or correct that.

## Tasting

## Next time
