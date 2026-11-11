---
roast_id: 2026-11-10-01
status: roasted
date: 2026-11-10
bean_id: costa-rica-la-rosa-washed-2024a
baseline_roast: null
goal: "First roast on this machine. Find when first crack happens and get a drinkable city_plus roast."
changed_variable: null

plan:
  mode: P01
  set_time_min: 14
  p03_set_temp_c: null
  green_weight_g: 90.0
  target_roast_level: city_plus
  expected_first_crack: "08:30"
  stop_rule: "Press Power to cool 0:30 after first crack ends. If the end is unclear, press at 2:00 after first crack starts. Press at once on any second-crack sound, and no later than 13:00 elapsed (display 1:00)."

environment:
  ambient_temp_c: null
  ambient_humidity_pct: null
  location: null
  outlet: null
  warm_start: false
  minutes_since_last_roast: null

actual:
  mode: P01
  set_time_min: 14
  p03_set_temp_c: null
  green_weight_g: 90.0
  roasted_weight_g: 80.8
  heating_end: "14:00"
  heating_end_reason: timer
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
  weight_loss_pct: 10.2
  development_time: null
  development_ratio_pct: null
  roast_level: light
  color_whole: null
  color_ground: null
  color_method: null
  evenness: slightly_uneven
  defects: []
  chaff_amount: null
  bean_movement: null

tasting: []

next_time: "Set time 14 → 16 min, same program and weight, to add development. Planned as 2026-11-11-01."
notes: "Roasted 2026-11-10. Colin reported that the timer ran out, so heating ended at 14:00, past the planned 13:00 limit. Program P01 and set time 14 are taken from the plan he followed, not stated separately. Event times, room temperature and cooling end were not reported and stay null. roast_level and evenness were judged by the agent from Colin's photos of 2026-11-11, not in person."
---

# Roast 2026-11-10-01: Costa Rica La Rosa

## Plan rationale

This is the first roast on the machine, so there is no baseline and no observed data. Its main job is to measure when first crack starts (H2 in the [roaster profile](../reference/roaster-profile.md)). A good cup is the second goal.

- **P01.** The bean is washed, and the manual assigns washed, low-chaff beans to P01. (**manual**)
- **90 g.** The limit is 120 g (**manual**). A load somewhat below the maximum keeps the beans moving in an air roaster (**external guidance**). 90 g also divides the 1 lb bag into five roasts.
- **Set time 14 min, cool by hand.** Pressing Power during heating starts cooling, and it is the only way to end a roast early (**manual**). A long set time leaves room to stop by ear. Whether the set time changes the heating curve is untested (H1, **hypothesis**). Roast 2 tests it.
- **Expected first crack about 08:30, likely range 07:00–10:00.** The manual's chart puts first crack near 8.5–9 min (**manual**, read by eye from a blurred chart). Old, dry beans tend to crack sooner (**external guidance**).
- **Stop 0:30 after first crack ends.** This is the seller's advice for this coffee, and the seller warns that it goes flat if roasted too long or too hot. (**external guidance**, from the bag label)
- **Hard limit 13:00.** The manual's chart puts second crack near 15 min (**manual**). Stopping at 13:00 keeps the roast short of it and avoids heavy smoke.
- **Expected weight loss 12–15 %.** City to city_plus is typically 13–15 % (**external guidance**). A 30-month-old bean has less water to lose, so the figure may be lower.

**Confidence: 55 %** that first crack starts between 07:00 and 10:00 and the roast ends at city to city_plus. The main uncertainty is the supply voltage of this unit (H7). The manual describes a 220–240 V machine. A 120 V version may heat on a different schedule. Bean age is the second uncertainty.

## Before the roast

1. Read the rating label on the base and note the voltage, frequency and power (task SETUP-01).
2. Put the roaster under a range hood or by an open window, on a flat surface, with 30 cm clear around it. Do not run a kettle or microwave on the same circuit.
3. Check that the chaff bin is empty and the intake screen is clean.
4. Weigh 90.0 g of green beans. Remove stones and broken or black beans. Weigh the whole bag first if possible, to correct the bean record.
5. Note the room temperature.
6. Load the beans, check they are below the MAX line, and lock the lid, chaff bin and chamber.
7. Have a count-up timer ready. A phone stopwatch with a lap button works well: one lap per event.

## During the roast

1. Hold Power for 3 s. Select P01 and press Power. Turn the knob to 14 and press Power. Start the count-up timer at that press.
2. Stay with the roaster for the whole cycle. Record the elapsed time of each event:
   - **Color change**: beans go from green to yellow or tan, and the smell changes from grass to hay or bread.
   - **First crack start**: the first of several popcorn-like cracks within a few seconds. One stray pop does not count.
   - **First crack rolling**: cracks are continuous.
   - **First crack end**: cracks taper off to none for about 10 s.
3. Watch how the beans move (good, sluggish or stalled) and when smoke appears.
4. Press Power once to start cooling according to the stop rule. Record that time. It is `heating_end`.
5. If first crack has not started by 12:00, keep going and still press Power at 13:00. That result is useful: it means this unit runs slower than the manual's chart.
6. If the display shows E1, E2 or E3, write the code down and follow the manual.

If the count-up timer fails, elapsed time is 14:00 minus the display.

## After the roast

1. Wait until cooling ends and the unit returns to standby. Record that time. Then unload.
2. Weigh the roasted beans without chaff.
3. Note the chaff amount, how even the color is, and any dark patches or dark tips.
4. Empty the chaff bin.
5. Store the beans in an airtight container. Taste after 3–5 days of rest, and use the same brew recipe for every roast of this bean.

## What happened

Colin's first report, 2026-11-10:

- No first crack was heard at any point. He suspects the fan noise covered it.
- No visible smoke. Heat came through the outlet.
- 90.0 g green gave 80.8 g roasted: 10.2 % weight loss.
- "The color looks pretty good." No roast level judged yet.
- Stored in a mason jar with the lid slightly loose.

Reading of the result (**external guidance**, not yet confirmed): 10.2 % is below the 11–13 % typical for a light roast. Old green coffee holds less water, so the same roast level loses less weight. The roast is therefore somewhere between just short of first crack and a light roast. Bean size, surface and smell will narrow it down, and the cup will settle it.

Second report, 2026-11-11 (photos beside green beans and beside a Colombian coffee roasted between light and medium):

- The roasted beans are clearly larger than the green ones and the center creases have opened.
- Color is light to medium-light brown, lighter than the Colombian reference. A few beans are paler tan. Many surfaces are still matte and slightly wrinkled.
- A bean broke between the teeth with minimal to moderate effort.
- Rating label: 120 V, 60 Hz, 1400 W.

Conclusion: the beans expanded and turned brittle, so first crack very probably happened and was not heard. The roast is `light`, with little development after first crack. This agrees with the 10.2 % weight loss for an old, dry bean.

## Tasting

## Next time

Set time 14 → 16 min with everything else the same. The full 14 minutes gave only a light roast with little development, so this unit runs slower than the manual's chart. See roast 2026-11-11-01.
