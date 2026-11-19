---
roast_id: 2026-11-19-01
status: planned
date: 2026-11-19
bean_id: colombia-huila-santa-maria-washed-2026a
baseline_roast: 2026-11-11-02
goal: "First roast of a fresh Colombian. Get about 90 g of roasted coffee at the darkest this roaster reaches on P01, and test a 108 g load (H3, first test above 90 g)."
changed_variable: "green weight 90.0 → 108.0 g (the bean also changes, which cannot be avoided)"

plan:
  mode: P01
  set_time_min: 18
  p03_set_temp_c: null
  green_weight_g: 108.0
  target_roast_level: full_city_plus
  expected_first_crack: "12:00"
  stop_rule: "Let the timer run out at 18:00. If second crack starts first, press Power to cool after about 5 snaps (roughly 15–20 s after the first one). Press Power at once on heavy smoke or an oily sheen. If the beans are not moving at all at 02:00, press Power and report it."

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
notes: "Planned 2026-11-19. Colin asked for about 100 g green to get 90 g roasted; the plan uses 108.0 g to allow for 14–17 % weight loss. Must be a cold start. If roasted on another day, rename the file and roast_id. Roast 2026-11-16-02 (Costa Rica, H1 test) is still planned; if both run on the same day, roast this one first and wait at least 30 min before the other."
---

# Roast 2026-11-19-01: Colombia Huila Santa Maria

## Plan rationale

Baseline is roast [2026-11-11-02](2026-11-11-02-costa-rica-la-rosa-washed-2024a.md) (`P01`, `90.0 g`, `18 min` → `76.2 g`, `15.3 %` loss, about the color of a light-medium Colombian reference, no second crack). It is the darkest and best-tasting roast so far. Two things change: the bean (a fresh lot, so unavoidable) and the load, `90.0 → 108.0 g`.

- **Why 108 g and not 100 g.** Colin wants about 90 g roasted. Expected weight loss is `14–17 %` (see below), so 100 g would give only `83–86 g`. 108 g gives `89.6–92.9 g`. It stays 12 g under the 120 g limit (**manual**).
- **Why a bigger load may help.** Going from 70 g to 90 g at the same settings raised weight loss from `8.0 %` to `12.0 %` (**observed**, 2026-11-16-01, 2026-11-11-01). The bigger bed seems to hold more heat. Whether that keeps going above 90 g, or the beans start to move too slowly, is untested (H3). This roast is that test.
- **Why 18 min.** It is the longest P01 setting (**manual**), and at 90 g it still did not reach second crack (**observed**, 2026-11-11-02). The seller's sweet spot is "a few snaps into 2nd crack" (`full_city_plus`). Anything shorter would land lighter than the seller's target.
- **Why P01.** Washed coffee (**manual**).
- **Fresh beans behave differently.** Fresh green coffee holds more water than a 30-month-old lot, so it usually loses a little more weight for the same color and can crack louder (**external guidance**). That is why expected loss is `14–17 %`, slightly above the `15.3 %` baseline at the low end of development.
- **Expected events.** Color change about `07:30–08:30` (**observed** at 90 g on the old lot, 2026-11-11-01, 2026-11-11-02). First crack about `11:00–13:00`, usually 3–5 min after color change in air roasters (**external guidance**); it has never been heard on this machine, so any clear cracking is a useful record. Second crack, if any, would come in the last minute or two.
- **Cold start.** Run it on a cold roaster so it compares with the baseline (**external guidance**).

**Confidence: 65 %** that it lands at `89–94 g` roasted and a pleasant medium (`city_plus` to `full_city`). The main uncertainty is whether 108 g of fresh beans circulates well and roasts faster than 90 g did; it could also end lighter than the seller's target, because second crack has not happened on this machine yet.

**If it ends lighter than wanted:** the next roast keeps 108 g and moves to the manual's two-stage `P02 + P03` method or P03 alone (H5), since P01 has no longer setting. **If it hits second crack early** (before about 16:00): next time press Power sooner or drop to 16 min.

## Before the roast

1. Cold roaster. Same place and outlet as earlier roasts. Range hood on or window open, 30 cm clear all round (**manual**).
2. Empty the chaff bin and clean the intake screen.
3. Weigh `108.0 g` of green beans. Pick out stones and broken beans. Check the beans are below the MAX fill line (**manual**). If they are above it, remove beans until they are below and write down the weight.
4. Count-up stopwatch and phone camera ready.

## During the roast

1. Hold Power `3 s`, knob to `P01`, press Power, knob to `18`, press Power, start the stopwatch. Stay with the roaster the whole cycle (**manual**).
2. At `01:00–02:00` look at bean movement: the whole bed should churn, not only the top layer.
3. Write down color change, any first-crack cracking, smoke, and any second-crack snaps.
4. Follow the stop rule. Unload only after cooling ends and the unit returns to standby (**manual**).

## After the roast

1. Weigh the cooled beans without chaff (`roasted_weight_g`).
2. Note the chaff amount, and photograph the beans beside the Colombian reference and roast 2026-11-11-02 if any is left.
3. Store airtight. Rest at least 4 days before tasting.

## During the roast (notes)

## Tasting

Brew with Colin's daily recipe: Cosori Juni, `30 g`, Fellow Opus 2 at `3.5` (**observed**, 2026-11-11-02 tasting). Keep that recipe fixed across roasts of this bean so the roast is the only variable.

## Next time
