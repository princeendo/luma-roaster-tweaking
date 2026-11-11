---
roast_id: 2026-11-11-02
status: roasted
date: 2026-11-11
bean_id: costa-rica-la-rosa-washed-2024a
baseline_roast: 2026-11-11-01
goal: "Top of the 14/16/18 min series: see how dark the maximum set time roasts, about 13.5-14.5 % weight loss."
changed_variable: "set time 16 → 18 min"

plan:
  mode: P01
  set_time_min: 18
  p03_set_temp_c: null
  green_weight_g: 90.0
  target_roast_level: city_plus
  expected_first_crack: null
  stop_rule: "Let the timer run out at 18:00. Press Power to cool early only on second-crack sounds (fast, quiet crackle), heavy smoke, or an oily sheen on the beans."

environment:
  ambient_temp_c: null
  ambient_humidity_pct: null
  location: null
  outlet: null
  warm_start: null
  minutes_since_last_roast: null

actual:
  mode: P01
  set_time_min: 18
  p03_set_temp_c: null
  green_weight_g: 90.0
  roasted_weight_g: 76.2
  heating_end: "18:00"
  heating_end_reason: timer
  cooling_end: null
  error_codes: []

events:
  color_change: "08:00"
  first_crack_start: null
  first_crack_rolling: null
  first_crack_end: null
  second_crack_start: null
  smoke_noticeable: null

results:
  weight_loss_pct: 15.3
  development_time: null
  development_ratio_pct: null
  roast_level: city_plus
  color_whole: null
  color_ground: null
  color_method: null
  evenness: null
  defects: []
  chaff_amount: null
  bean_movement: null

tasting: []

next_time: "No further time step: 18 min is the P01 maximum. Taste the 14, 16 and 18 min roasts side by side, then choose the direction."
notes: "Planned for 2026-11-11 as the second roast of the day. If it happens on another day, rename the file and roast_id. expected_first_crack is null because first crack is not audible on this machine. Colin reported that he ran P01 for 18 minutes, recorded as the timer running out. color_change is his estimate (approximately 08:00). roast_level was judged by the agent from his photo. He did not say whether the roaster started cold, so warm_start stays null. Room temperature, sounds, smoke and cooling end were not reported."
---

# Roast 2026-11-11-02: Costa Rica La Rosa

## Plan rationale

Baseline is roast 2026-11-11-01. The one change is the set time, 16 → 18 min.

- **What the series shows so far.** P01 with 90.0 g: 14 min gave 10.2 % weight loss and a `light` roast; 16 min gave 12.0 % and `city`. That is about 0.9 points of weight loss for each added minute. (**observed**, 2026-11-10-01 and 2026-11-11-01)
- **Expected result.** About 13.5–14.5 % weight loss (77.0–77.9 g roasted), at or slightly darker than the Colombian light-medium reference, `city_plus` and possibly `full_city`. This extends the observed trend by two minutes; the trend may not stay straight. (**observed** trend, extrapolated)
- **Why 18.** It is the longest time P01 allows. (**manual**) It shows the darkest roast this program can give at 90 g, and it completes three evenly spaced roasts of one bean to taste side by side.
- **Risk to the cup.** The seller says this coffee goes flat if roasted too long. (**external guidance**, bag label) This roast may taste flatter than the 16 min roast. That is an acceptable cost on a practice lot, and the comparison is the point.
- **Why the timer.** First crack was not heard in either earlier roast. (**observed**, 2026-11-10-01 and 2026-11-11-01)
- **H1.** Color change came at about 07:30 with a 16 min set time. (**observed**, 2026-11-11-01) If it comes at about 07:30 again, the set time only cuts off one fixed curve. If it comes clearly later, the machine stretches the curve.
- **Cold start.** The earlier roasts started cold. A warm roaster usually roasts faster (**external guidance**), which would be a second change. Wait until the roaster is fully cool, at least 30 minutes after the last roast, and record the gap.

**Confidence: 65 %** that the weight loss lands between 13.5 and 14.5 % without reaching second crack. The main uncertainty is whether roast level keeps rising at the same rate late in the cycle. No roast on this machine has gone past 16 minutes.

## Before the roast

1. Same place and outlet. Nothing else large on that circuit.
2. Roaster fully cool. Note how long since the last roast ended.
3. Empty the chaff bin and check the intake screen.
4. Weigh 90.0 g of green beans. Note the room temperature.
5. Good ventilation. Smoke is more likely than in the earlier roasts.

## During the roast

1. Hold Power 3 s. Select P01, press Power. Turn to 18, press Power, and start the stopwatch on that press.
2. Record the elapsed time of the color change. This is the most useful number in this roast.
3. Record any cracking heard and the time smoke first shows.
4. Let the timer run out. Press Power early only on second-crack sounds, heavy smoke or an oily sheen, and record the time.
5. Record when cooling ends and the unit returns to standby.

Elapsed time is 18:00 minus the display.

## After the roast

1. Unload after standby. Weigh the roasted beans without chaff.
2. Photograph them beside both earlier roasts and the Colombian reference.
3. Empty the chaff bin. Store airtight with the lid closed, labeled with the roast time.

## What happened

Colin's report, 2026-11-11, with a photo of green beans, the 14, 16 and 18 min roasts and the Colombian light-medium reference in a row:

- P01 ran for 18 minutes.
- 90.0 g green gave 76.2 g roasted: 15.3 % weight loss. The plan expected 13.5–14.5 %.
- Color change at approximately 08:00.
- In the photo the beans are an even medium brown, darker than the 16 min roast and close to the Colombian reference, perhaps slightly lighter. No oil on the surface.

Reading:

- Recorded as `city_plus` from the color. The 15.3 % weight loss points darker, toward `full_city`, and more so for an old, dry bean. Color in a phone photo is the weaker evidence, so the true level may be `full_city`.
- Weight loss rose 1.8 points from 14 to 16 min and 3.3 points from 16 to 18 min. The roast speeds up late in the cycle. A warm start would also raise the figure, and it is not known whether this roast started cold.
- H1: color change came at about 07:30 with a 16 min setting and about 08:00 with 18 min. A fully stretched curve would predict about 08:25, and a fixed curve 07:30. Both times are estimates, so the half-minute difference does not settle the question.

## Tasting

## Next time

The time series is complete at 14, 16 and 18 min. Taste all three with one recipe before using the last two batches. The best-tasting time sets the next roast.
