---
roast_id: 2026-11-19-04
status: roasted
date: 2026-11-19
bean_id: colombia-huila-santa-maria-washed-2026a
baseline_roast: 2026-11-19-01
goal: "Get darker than P01 alone reaches: P01 18 min to about city, then a P03 stage at the maximum, 240 °C (464 °F), toward the seller's 'a few snaps into 2nd crack'."
changed_variable: "added a second stage: P01 18 min → P01 18 min, then P03 240 °C (464 °F)"

plan:
  mode: P01+P03
  set_time_min: 18
  p03_set_temp_c: 240
  green_weight_g: 108.0
  target_roast_level: full_city_plus
  expected_first_crack: null
  stop_rule: "Stage 1: let P01 run the full 18:00. Stage 2 (P03, 464 °F, always 10:00): press Power to cool after about 5 snaps of second crack (roughly 15–20 s after the first one). Press Power at once on heavy smoke or an oily sheen. If the beans are not moving at all 2:00 into either stage, press Power and report it."

environment:
  ambient_temp_c: null
  ambient_humidity_pct: null
  location: garage
  outlet: null
  warm_start: false
  minutes_since_last_roast: null

actual:
  mode: P01+P03
  set_time_min: 18
  p03_set_temp_c: 240
  green_weight_g: 108.0
  roasted_weight_g: 89.6
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
  roast_level: city_plus
  color_whole: "medium brown, darker than 2026-11-19-01 and 2026-11-19-03; some mottling; no oil"
  color_ground: null
  color_method: "by eye from one indoor phone photo beside 2026-11-19-01 and 2026-11-19-03"
  evenness: slightly_uneven
  defects: []
  chaff_amount: null
  bean_movement: null

tasting: []

next_time: "Taste beside 2026-11-19-01 and 2026-11-19-03 before the next roast. If darker is wanted, record the garage temperature first; P03 at its maximum added only 3.1 % after a hot P01 stage."
notes: "Roasted 2026-11-19. Stage 1: 108.0 g to 96.0 g (11.1 %), catcher beans included. 3.5 g spilled on the floor while moving hot beans quickly between stages, so stage 2 started with 92.5 g and ended at 89.6 g (3.1 %), with a negligible amount in the chaff catcher. weight_loss_pct is null because the spill breaks the formula; the spill-adjusted total is about 13.9 % (89.6 x 96.0 / 92.5 = 93.0 g from 108.0 g). Stage 1 cooling was skipped (hot beans into P03). Cracks were not heard; Colin cannot hear them over the fan. p03_set_temp_c is taken from the plan (464 °F) and was not separately confirmed; heating_end_reason and event times were not reported. Planned 2026-11-19. Two-stage roast in one file. Event times: color change from the start of stage 1; first crack, second crack, smoke, heating_end and cooling_end from the start of stage 2 (P03). Record the weight between stages here if taken. Confirm the P03 knob reads 464 before pressing Power, and photograph it. No printable sheet. If roasted on another day, rename the file and roast_id."
---

# Roast 2026-11-19-04: Colombia Huila Santa Maria

## Plan rationale

Baseline is roast [2026-11-19-01](2026-11-19-01-colombia-huila-santa-maria-washed-2026a.md) (`P01`, `18 min`, `107.9 g` → `92.8 g`, `14.0 %` loss, `city`, mottled). The change is a second stage after it: P03 at its maximum, 240 °C (464 °F). Colin chose this over first repeating [2026-11-19-03](2026-11-19-03-colombia-huila-santa-maria-washed-2026a.md) with a confirmed 464 °F knob.

- **Why P01 first.** P01 18 min takes this bean to `city` on its own (**observed**, 2026-11-19-01). P02 18 min only dried it and lifted beans into the chaff catcher (**observed**, 2026-11-19-02). Starting from `city` leaves P03 only the last part of the roast to do.
- **Why P03 at 240 °C (464 °F).** It is the maximum (**manual**). After a P02 stage, P03 at 230 or 240 °C (the setting is not certain) added `6.9 %` loss and ended `light` (**observed**, 2026-11-19-03). Starting from `city` instead, the same heat should carry the beans into second crack.
- **Two-stage method.** The manual's version is P02 then P03 (**manual**). Using P01 as the first stage is not in the manual, but it uses the same programs within their limits. Beans cooled between stages and reheated can taste flatter than a single roast (**external guidance**).
- **Expected weight.** `full_city_plus` is usually about 16–18 % total loss on fresh coffee (**external guidance**): about `88.6–90.7 g` from 108.0 g. Below about 88 g, or any oil on the beans, means it went past the target.
- **Expected events (stage 2).** The beans start the stage cool, at `city`. Second crack, if it comes, probably in the second half of the 10 minutes. This is a guess.
- **Evenness.** P01 alone gave a mottled roast (**observed**, 2026-11-19-01). The P03 stage may even it out, or the mottling may stay.

**Confidence: 50 %** that this ends at `full_city` to `full_city_plus`, 88–91 g. The main risks are overshooting into `vienna` if second crack comes fast, and finding that P03 still adds too little heat.

## Stage 1: P01

1. Cold roaster, chaff bin empty. Range hood on or window open, 30 cm clear all round (**manual**).
2. Weigh `108.0 g`. Check below the MAX fill line (**manual**).
3. Hold Power `3 s`, knob to `P01`, press Power, knob to `18`, press Power, start the stopwatch.
4. Let it run the full 18:00 and the automatic cooling. Note color change.

## Between stages

1. Once it is back in standby, empty the chaff bin (**manual**, two-stage method).
2. Optional: weigh all the beans, including any in the chaff catcher. This gives a check against roast 1's `92.8 g`.
3. Put all the beans back. Move on soon, without a long wait.

## Stage 2: P03

1. Hold Power `3 s`, knob to `P03`, press Power, knob to **`464`** (°F, 240 °C). **Check it reads 464, take a photo**, press Power, restart the stopwatch from zero.
2. Watch the first minute for beans blowing into the chaff catcher.
3. Listen for cracking. Second crack is a quieter, faster crackle like rice cereal in milk, often with a jump in smoke.
4. Follow the stop rule. Unload only after cooling ends and the unit returns to standby (**manual**).

## After the roast

1. Weigh all the beans, including any in the chaff catcher.
2. Photograph them beside roasts 2026-11-19-01 and 2026-11-19-03.
3. Store airtight and rest at least 4 days.

## During the roast (notes)

Colin's mid-roast report, 2026-11-19:

- **After stage 1 (P01, 18 min):** `108.0 g` → `96.0 g`, `11.1 %` loss ([photo](assets/2026-11-19-04-after-p01.jpg)). Light to light-medium and mottled, like roast 2026-11-19-01, but that roast lost `14.0 %` (`92.8 g`) at the same settings. Colin confirmed a cold start (at least 30 min after the previous roast), P01 for the full 18 min, and about the same garage temperature as roast 1. He then found the likely reason: in roast 1 he discarded the less-roasted beans from the chaff catcher before weighing, and here he put them back. So roast 1's `14.0 %` was overstated, and the two P01 stages probably roasted about the same.
- **Cracks cannot be heard.** Colin said he has never been able to hear cracks over the fan. The stop rule was changed mid-roast to: press Power when smoke turns from wisps to a steady stream, when the beans turn clearly darker than 2026-11-19-01, or on any oily sheen; otherwise let 10:00 run.
- **No cooling between stages.** Colin did not wait for stage 1's cooling cycle to finish. He went to P03 as quickly as he could, so stage 2 started with hot beans, unlike the plan (wait for standby, then empty the chaff bin). Expect stage 2 to run faster than the P03 stage of 2026-11-19-03, which started from cool beans. The manual says to unload only after cooling ends and the unit is back in standby (**manual**); the stage 1 weight (`96.0 g`) was taken hot.
- **Spill between stages:** `3.5 g` fell on the floor while Colin was moving the hot beans quickly, so stage 2 (P03) started with `92.5 g`. Total loss from green can only be estimated: scale the final weight by `96.0 / 92.5`. Target for `full_city_plus` (16–18 % total) is now about `85–87.5 g` at the end.

![Beans after stage 1 (P01 18 min)](assets/2026-11-19-04-after-p01.jpg)

- **Final (after stage 2):** `92.5 g` → `89.6 g`, `3.1 %` in this stage, with a negligible amount in the chaff catcher. Spill-adjusted, about `93.0 g` from `108.0 g`: **`13.9 %` total**. That is lighter than the planned `85–87.5 g`.
- **Color** ([photo](assets/2026-11-19-01-03-04-comparison.jpg); left to right: 2026-11-19-01, 2026-11-19-03, this roast). Medium brown, the darkest of the three, with a little mottling left and no oil. Judged `city_plus`, short of the `full_city_plus` target.
- **What it says about P03.** Even starting from hot beans already at about `city`, 10 minutes at P03's maximum added only `3.1 %`. P03 holds the roast rather than driving it hard. P01's last minutes seem to be the hottest heat this roaster gives, and an 18 min P01 run already ends close to `city`. So, on this unit at 108 g in this garage, about `city_plus` may be as dark as the programs reach.

![Roasts 2026-11-19-01, 2026-11-19-03 and 2026-11-19-04, left to right](assets/2026-11-19-01-03-04-comparison.jpg)

## Tasting

## Next time

Taste all three before roasting again. If the cup wants more roast, check the garage temperature first: cold intake air lowers the heat a small air roaster can reach (**external guidance**).
