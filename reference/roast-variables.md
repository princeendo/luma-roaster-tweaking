# Roast variables

This is the dictionary for every field in a roast file (`roasts/_template.md`) and a bean file (`beans/_template.md`). The front-matter keys are the data contract that a future app will read and write. Change a key here and in the template in the same commit.

## Units and conventions

| Quantity | Unit | Format |
|---|---|---|
| Temperature | °C | number, for example `205` |
| Weight | grams | number, one decimal at most, for example `100.0` |
| Elapsed time | minutes and seconds from the press of Power that starts heating | string `"mm:ss"`, for example `"08:45"` |
| Roaster time setting | whole minutes, as set on the knob | number, for example `11` |
| Date | ISO 8601 | `2026-11-12` |
| Unknown or not observed | | `null` |

Elapsed time runs from the start of heating, not from power-on. The roaster's display counts down, so write down the countdown and convert, or (better) run a separate count-up timer. With a set time `T` minutes, a countdown reading `c` is elapsed time `T*60 - c` seconds.

## Identifiers

| Key | Meaning |
|---|---|
| `roast_id` | `YYYY-MM-DD-NN`, where `NN` is the roast number that day starting at `01`. The file name is `roasts/<roast_id>-<bean_id>.md`. |
| `bean_id` | Short kebab-case slug for one lot of green coffee, for example `ethiopia-guji-natural-2026a`. The file name is `beans/<bean_id>.md`. A new purchase of the same coffee is a new lot and gets a new ID. |
| `baseline_roast` | The `roast_id` this roast is compared against. `null` for the first roast of a bean when no useful baseline exists. |

## Roast file: header

| Key | Values | Meaning |
|---|---|---|
| `status` | `planned`, `roasted`, `tasted`, `abandoned` | Lifecycle. `abandoned` keeps a planned roast that never happened, with the reason in `notes`. |
| `date` | date | Roast date. |
| `goal` | text | What this roast is for, such as "first look at this bean" or "less sour than 2026-11-12-01". |
| `changed_variable` | text | The one setting changed from `baseline_roast`, such as "set time 11 → 12 min". |

## Roast file: `plan` and `actual`

`plan` is written before the roast. `actual` is what really happened. They have the same keys so they can be compared.

| Key | Values | Meaning |
|---|---|---|
| `mode` | `P01`, `P02`, `P03`, `P02+P03` | Roaster program. `P02+P03` is the manual's two-stage method. |
| `set_time_min` | 2–18 | Time setting for P01 or P02. For `P02+P03`, the P02 stage time. `null` for P03 alone. |
| `p03_set_temp_c` | 140–240 | Temperature setting for P03. P03 always heats for 10 minutes. |
| `green_weight_g` | ≤ 120 | Green coffee weighed before loading. |
| `target_roast_level` | see [roast levels](#roast-levels) | Plan only. |
| `expected_first_crack` | mm:ss | Plan only. Predicted first-crack start. |
| `stop_rule` | text | Plan only. When to press Power to start cooling early, if at all. |
| `roasted_weight_g` | number | Actual only. Weight after cooling and chaff removal. |
| `heating_end` | mm:ss | Actual only. When heating stopped. |
| `heating_end_reason` | `timer`, `manual_cool` | Actual only. Whether the countdown ran out or Power was pressed. |
| `cooling_end` | mm:ss | Actual only. When the unit returned to standby. |
| `error_codes` | list, such as `[E2]` | Actual only. Any E1, E2 or E3 shown. |

## Roast file: `environment`

These explain why the same settings can roast differently on different days. Small air roasters are sensitive to room temperature and supply voltage.

| Key | Values | Meaning |
|---|---|---|
| `ambient_temp_c` | number | Room temperature where the roaster sits. |
| `ambient_humidity_pct` | number | Relative humidity, if known. |
| `location` | text | For example "kitchen counter under range hood". |
| `outlet` | text | Which outlet or circuit. Keep it the same between roasts if possible. |
| `warm_start` | `true`, `false` | `true` if the roaster had run in the previous 30 minutes. |
| `minutes_since_last_roast` | number | Gap after the previous roast on the same session. `null` for a cold start. |

## Roast file: `events`

Elapsed times (mm:ss). Record what was observed. Leave the rest `null`.

| Key | How to recognize it |
|---|---|
| `color_change` | Beans turn from green to yellow or tan, and the smell changes from grassy to bread or hay. |
| `first_crack_start` | First clear, popcorn-like crack. Not a single stray pop: the first of several within a few seconds. |
| `first_crack_rolling` | Cracks come continuously. |
| `first_crack_end` | Cracks taper off. |
| `second_crack_start` | Quieter, faster crackle like rice cereal in milk. Smoke rises sharply. |
| `smoke_noticeable` | Visible smoke from the outlet. |

## Roast file: `results`

| Key | Values | Meaning |
|---|---|---|
| `weight_loss_pct` | number | `(green_weight_g - roasted_weight_g) / green_weight_g * 100`, to one decimal. |
| `development_time` | mm:ss | `heating_end - first_crack_start`. `null` if first crack was not heard. |
| `development_ratio_pct` | number | `development_time / heating_end * 100`, to one decimal. Often called DTR. |
| `roast_level` | see [roast levels](#roast-levels) | Judged by eye on the whole beans after cooling, in daylight if possible. |
| `color_whole` | number or text | Optional color reading on whole beans. |
| `color_ground` | number or text | Optional color reading on ground coffee. |
| `color_method` | text | Device or method for the color readings, such as a phone app or reference card. |
| `evenness` | `even`, `slightly_uneven`, `uneven` | Spread of color between beans. |
| `defects` | list | Any of `scorching` (dark patches on flat faces), `tipping` (dark bean ends), `chipping`, `underdeveloped` (wrinkled, pale crease), `oily_surface`. |
| `chaff_amount` | `light`, `moderate`, `heavy` | Chaff collected in the bin. |
| `bean_movement` | `good`, `sluggish`, `stalled` | How freely the beans circulated in the chamber. |

## Roast file: `tasting`

A list with one entry for each time the coffee is brewed and assessed. Add an entry rather than overwrite one.

| Key | Values | Meaning |
|---|---|---|
| `date` | date | Tasting date. |
| `rest_days` | number | Days since the roast. |
| `brew_method` | text | For example `v60`, `aeropress`, `espresso`, `french_press`. |
| `dose_g`, `water_g` | numbers | Recipe. Use the same recipe across roasts of a bean so the roast is the variable. |
| `grind` | text | Grinder and setting. |
| `water_temp_c` | number | Brew water temperature. |
| `acidity`, `sweetness`, `body`, `bitterness` | 1–5 | Intensity, not quality. 3 is moderate. |
| `flavor_notes` | list | Words such as `blueberry`, `cocoa`, `grassy`, `ashy`. |
| `overall` | 1–10 | Colin's overall enjoyment. |
| `notes` | text | Anything else. |

## Roast file: free text

`next_time` holds the one recommended change for the next roast of this bean. `notes` holds corrections and anything that does not fit a field.

## Bean file keys

| Key | Values | Meaning |
|---|---|---|
| `name` | text | The seller's product name. |
| `status` | `in_stock`, `finished` | Whether any green coffee is left. |
| `supplier`, `supplier_url` | text | Where it was bought. |
| `purchase_date` | date | |
| `green_weight_purchased_g` | number | |
| `green_weight_remaining_g` | number | Reduce by `green_weight_g` each time a roast is recorded. |
| `cost_total` | number | Price paid, in the purchase currency. |
| `origin_country`, `region`, `producer` | text | |
| `variety` | list | For example `[Heirloom]`, `[Caturra, Catuai]`. |
| `process` | `washed`, `natural`, `honey`, `wet_hulled`, `anaerobic`, `decaf`, `other` | Processing method. It drives the P01/P02 choice. |
| `altitude_m` | number or range text | Higher grown coffee is usually denser. |
| `harvest` | text | Crop year, for example `2025/26`. |
| `screen_size` | text | Bean size grade, if published. |
| `density_g_l` | number | Free-flow density, if measured. |
| `moisture_pct` | number | If published. |
| `chaff_level` | `low`, `medium`, `high` | Observed after the first roast. |
| `suggested_mode` | `P01`, `P02` | Manual rule: P01 for peeled or low-chaff beans (washed, polished), P02 for unpeeled or high-chaff beans (natural, honey). |
| `supplier_roast_notes` | text | The seller's roasting advice. |
| `supplier_flavor_notes` | list | The seller's tasting notes. |

## Roast levels

Use these values for `target_roast_level` and `roast_level`. They follow common specialty-coffee usage (external guidance), from lightest to darkest. The manual uses different and inconsistent names (it ranks "City" darker than "Dark"), so do not mix its labels into this field. Put a manual label in `notes` if it matters.

| Value | Typical marker (external guidance) |
|---|---|
| `cinnamon` | Just into first crack. Very light tan, often sour and grassy. |
| `light` | Late first crack. |
| `city` | Just after first crack ends. |
| `city_plus` | A short time after first crack ends. Common target for bright single origins. |
| `full_city` | Just before second crack. |
| `full_city_plus` | First few snaps of second crack. |
| `vienna` | Early second crack. Oil starts to show. |
| `french` | Well into second crack. Oily, dark. |
| `italian` | End of second crack. Very dark, burnt notes. |
