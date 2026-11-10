# Luma roaster tweaking

Notes, roast logs and reference material for getting good coffee out of a CBR-120POT ("Luma") hot-air home roaster.

The workflow is a conversation with an agent:

1. Ask the agent to plan the next roast of a bean. It reads the reference files and every earlier roast, then writes a planned roast file with settings, expected crack times and when to press Power to cool.
2. Roast, and note the times, weights and what you saw and heard.
3. Tell the agent what happened. It fills in the roast file, works out weight loss and development, and updates what it knows about the roaster.
4. After resting and brewing, report how it tasted. The agent records it and proposes the next change.

Later, an Android app will run the timers and capture the same data at the roaster. See `TASKS.md`.

## Layout

```text
AGENTS.md                      Rules for agents (CLAUDE.md points here)
TASKS.md                       Open work, including the app
reference/
  roaster-profile.md           What this roaster does: manual facts, observations, open questions
  roast-variables.md           Every tracked field, its units and how it is calculated
  roasting-fundamentals.md     General roasting knowledge (external guidance)
  manual/                      The manufacturer's manual: original scan, transcription, quick reference
beans/
  _template.md                 One file per lot of green coffee
roasts/
  _template.md                 One file per roast
print/                         Printable one-page roast sheets (HTML source and PDF)
docs/agent/                    Agent preferences, decisions and learnings
```

## What to note during a roast

Have a scale and a count-up timer ready (the roaster's display counts down). The minimum useful record is:

- green weight before, roasted weight after
- program and setting
- time of first crack start, and of second crack if it happens
- time you pressed Power to cool, if you did
- room temperature

Everything else in `reference/roast-variables.md` is optional and helps when available.

## Naming

- Beans: `beans/<bean_id>.md`, for example `beans/ethiopia-guji-natural-2026a.md`.
- Roasts: `roasts/<YYYY-MM-DD-NN>-<bean_id>.md`, for example `roasts/2026-11-12-01-ethiopia-guji-natural-2026a.md`.

## Safety

Read the manual's limits in `AGENTS.md` and `reference/manual/`. In short: 120 g at most, stay with the roaster, keep the vents clear, and unload only after cooling finishes.
