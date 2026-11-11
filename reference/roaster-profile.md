# Roaster profile: CBR-120POT

This is the agent's working model of Colin's roaster. It separates three kinds of knowledge:

- **Manual:** what the manufacturer's manual says ([transcription](manual/cbr-120pot-user-manual.md)).
- **Observed:** what Colin's roasts have shown. Each entry cites roast IDs.
- **Hypothesis:** a reasonable reading that has not been tested on this machine.

Update this file whenever a roast confirms or contradicts an entry.

## The machine

A countertop hot-air (fluid-bed) roaster. A fan blows heated air up through the bean chamber, which keeps the beans moving and roasts them. Chaff blows up into a bin under the lid. There is no bean-temperature probe and no live temperature readout. The only controls are a program choice, one number (time or temperature), and the Power button.

| Item | Value | Source |
|---|---|---|
| Model | CBR-120POT. "Luma" is the seller's name; it does not appear in the manual. | Manual |
| Capacity | 120 g maximum, below the MAX fill line | Manual |
| Rated power | 1,500 W | Manual |
| Rated supply | AC 220–240 V, 50/60 Hz | Manual |
| Nameplate on Colin's unit | **120 V, 60 Hz, 1,400 W** | Observed (label read 2026-11-11) |
| Maximum temperature | 240 °C | Manual |
| Display units | °C | Manual |

**Supply voltage:** the manual is written for a 220–240 V, 1,500 W unit. Colin's unit is a 120 V, 1,400 W version, so it has slightly less heating power and the manual's times and chart may not apply to it. Treat them as a rough guide until roasts confirm them. 1,400 W at 120 V draws about 11.7 A, most of a 15 A circuit, so nothing else large should run on that circuit during a roast.

## Controls

| Action | How | Source |
|---|---|---|
| Power on | Hold Power for 3 s. Display shows P01. | Manual |
| Choose program | Turn knob to P01, P02 or P03, press Power once. | Manual |
| Set value | Turn knob to time (P01/P02) or temperature (P03), press Power once to start. | Manual |
| During heating | Display counts down. Heating indicator is lit. | Manual |
| End of heating | At zero, cooling starts on its own. Cooling indicator is lit. | Manual |
| Stop early | Press Power once during heating. It goes straight to cooling. This is the only way to end a roast early. | Manual |
| Change settings mid-roast | Not possible. Time cannot be reset and the unit cannot be turned off during heating. | Manual |
| Unload | Only after cooling ends and the unit returns to standby. | Manual |

**Practical consequence (hypothesis):** Power is the "drop" button. The set time is an upper limit, and the real end of the roast is when Colin presses Power to cool. This only works if a longer set time does not change the heating curve before that point. See [H1](#open-questions).

## Programs

| Program | For | Setting | Source |
|---|---|---|---|
| P01 | Peeled or low-chaff beans: washed, polished | Time 2–18 min on the built-in curve | Manual |
| P02 | Unpeeled or high-chaff beans: natural, honey | Time 2–18 min on the built-in curve | Manual |
| P03 | "DIY professional" roasting of peeled beans, or re-roasting and drying roasted beans | Temperature 140–240 °C, fixed 10 min | Manual |
| P02 + P03 | Two stages: P02 for 10 min to dry and remove chaff, empty the chaff bin, then P03 at a chosen temperature | Manual gives no P03 temperature | Manual |

The manual does not say how P01 and P02 differ inside the machine (fan speed, heat or both).

## Manual reference timings (P01/P02)

The manual's table, "based on the roaster's test results" and "for reference only":

| Manual label | Set time | Listed maximum temperature |
|---|---|---|
| Light Roast | 6–8 min | 180 °C |
| Medium Roast | 9–11 min | 195 °C |
| Dark Roast | 12–14 min | 215 °C |
| City Roast | 14–16 min | 225 °C |
| Italian Roast | 17–18 min | 240 °C |

The manual's reference chart ([original scan](manual/assets/temperature-profile-original-highres.png), [redraw](manual/assets/temperature-profile.png)) gives a different picture. Reading the scan by eye (approximate, the labels are blurred):

| Chart label | Approx. time | Approx. chart temperature |
|---|---|---|
| Cinnamon Roast | ~7 min | ~190 °C |
| Light Roast | ~8.5 min | ~195–200 °C |
| First crack | ~8.5–9 min | ~195–200 °C |
| Medium Roast | ~11 min | ~210 °C |
| Second crack | ~15 min | ~225 °C |
| Dark Roast | ~16.5 min | ~235 °C |
| City Roast | ~17 min | ~240 °C |
| Top label (illegible, possibly "Espresso Roast") | ~19 min | ~250 °C |

The chart curve rises fast to about 130 °C in 1 minute, reaches about 180 °C at 5 minutes, then climbs slowly in steps. Cooling falls to about 55 °C within roughly 1.5 minutes.

**What this means for planning (hypothesis):**

- The table and chart disagree. The table's "Light Roast" at 6–8 minutes ends before the chart's first crack at about 9 minutes. Coffee stopped before first crack is usually not drinkable (external guidance). Treat the table's short times with suspicion until a roast shows where first crack really happens.
- The chart's temperatures are probably air or heater temperatures, not bean temperatures. Do not compare them with bean-temperature figures from other roasters.
- The chart is the manufacturer's illustration, not measured data from Colin's machine.

## Observed behavior

Add entries here as `- <finding> (roasts: <IDs>)`.

- First crack was not heard over the fan with 90 g of a 30-month-old washed coffee. The beans had expanded, opened at the crease and turned brittle, so first crack very probably happened unheard. Do not rely on sound alone to end a roast. Use elapsed time and weight loss as well. (roasts: 2026-11-10-01)
- P01 with 90 g and a 14 min set time, run to the end of the timer, gave only a `light` roast with 10.2 % weight loss on a 30-month-old washed coffee. This unit is slower than the manual's chart, which shows medium at about 11 min. (roasts: 2026-11-10-01)
- A longer set time gives a darker roast: P01 at 16 min was clearly darker than P01 at 14 min, same bean and 90.0 g, timer run out both times. Weight loss rose from 10.2 % to 12.0 %, about 0.9 points per added minute. (roasts: 2026-11-10-01, 2026-11-11-01)
- Color change (green to yellow or tan) came at about 07:30 on P01 with a 16 min set time. (roasts: 2026-11-11-01)
- First crack was not heard in either roast. The fan is probably too loud for sound to be a usable signal on this machine. (roasts: 2026-11-10-01, 2026-11-11-01)
- No visible smoke at 10.2 % weight loss. (roasts: 2026-11-10-01)

## Open questions

Each question lists a cheap test. Run the tests early, because the answers change how every later roast is planned.

| ID | Question | Test | Status |
|---|---|---|---|
| H1 | Does the P01/P02 time setting cut off one fixed curve (so 10 min and 14 min settings heat the same way until 10:00)? Or does it stretch the curve to fit the time? | Roast the same bean, same weight, at two set times (for example 10 and 14 min). Compare color change and first-crack times. Same times → one fixed curve. | Open. 16 min roasted darker than 14 min, which fits either answer. The color-change time is known only for the 16 min roast (about 07:30), so log it on every roast. |
| H2 | When does first crack start on this machine at 100 g? | Every roast: log `first_crack_start`. | Open. Not heard in 2026-11-10-01 or 2026-11-11-01. |
| H3 | How does batch size change timing? In fluid-bed roasters a larger batch often moves less and roasts slower, but it can also retain more heat. | After H1, roast one bean at 80 g and 110 g with the same settings. | Open |
| H4 | How do P01 and P02 differ in speed? | Roast the same bean, same weight and time in each. | Open |
| H5 | Does P03 hold a steady temperature or ramp? At what setting does it reach first crack within its 10 minutes? | After a P02 drying stage, run P03 at 220 °C and log crack times. Adjust by 10 °C steps. | Open |
| H6 | How much does a warm start (second batch soon after the first) speed up the roast? | Roast two identical batches back to back and compare event times. | Open |
| H7 | What supply voltage is the unit rated for? | Read the nameplate. | Answered: 120 V, 60 Hz, 1,400 W. |
