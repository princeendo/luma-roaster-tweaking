# Luma roaster tweaking: notes for agents

This file is authoritative for every agent tool (Claude Code, opencode, Codex, and so on). `CLAUDE.md` only points here.

This repository helps Colin get the most out of a small hot-air home coffee roaster (model **CBR-120POT**, sold as "Luma"). The agent and Colin work back and forth: the agent plans the next roast from the reference material and the roast history, Colin roasts and reports what happened, and the agent records the result and proposes the next adjustment. Later, an Android app (maybe iOS too) will run timers and capture the same data at the roaster.

## Read first

1. `README.md` for the layout.
2. `reference/roaster-profile.md` for what this machine can and cannot do. It is the agent's working model of the roaster.
3. `reference/roast-variables.md` for every tracked field and its meaning.
4. `reference/roasting-fundamentals.md` for general roasting knowledge.
5. The roast logs for the bean in question (`roasts/`), newest first, and its record in `beans/`.
6. `TASKS.md` for open work. It is the only status tracker; update it in the same change that completes, adds or blocks a task.

The manual is in `reference/manual/`. Use `cbr-120pot-user-manual.md` (transcription) for lookups. Open the original scan PDF only to settle a transcription question.

## Planning a roast

When Colin asks for the next roast:

1. Identify the bean. If it has no record in `beans/`, create one from `beans/_template.md` and ask only for the details that change the plan (process, origin, and how much green coffee is left).
2. Read every earlier roast of that bean, then the most recent roasts of any bean, because the roaster's behavior carries across beans.
3. Write a new roast file from `roasts/_template.md` with `status: planned`. Fill the plan section: goal, the one variable being changed, the settings, the expected event times, and a stop rule (for example, "press Power to cool at 1:30 after first crack starts, or at 11:00, whichever comes first").
4. Change one variable per roast against a previous roast unless Colin asks for a bigger jump. Say which roast is the baseline.
5. Give a confidence percentage and name the main uncertainty.
6. Label every recommendation by its source: **manual**, **observed** (cite roast IDs), or **external guidance** (general roasting knowledge, not yet tested on this machine). Never present external guidance as a manual claim or a measured fact.

## Recording a roast

When Colin reports a roast, fill the `actual`, `events`, `results` and `observations` sections of the planned file and set `status: roasted`. Compute weight loss and the development figures as `reference/roast-variables.md` defines them. Leave unknown fields as `null`. Do not invent times or weights. Add tasting notes later in the same file and set `status: tasted`.

When a roast confirms or contradicts something in `reference/roaster-profile.md`, update that file in the same change and cite the roast ID. Machine facts move from "hypothesis" to "observed" only with roast evidence.

## Safety limits

These come from the manual. Plans must never exceed them.

- Green bean load is **120 g or less** and below the MAX fill line.
- P01/P02 time is 2–18 minutes. P03 is 140–240 °C for a fixed 10 minutes.
- The roaster is attended for the whole cycle, with the air inlet and outlet clear and at least 30 cm from anything flammable.
- Beans come out only after cooling ends and the unit returns to standby.

## Data rules

- Temperatures are in °C, because the roaster displays °C. Weights are in grams. Times are `mm:ss` from the moment Power is pressed to start heating.
- Roast and bean files are Markdown with YAML front matter. The front matter is the machine-readable record that a future app will import, so keep its keys exactly as the template defines them. Add a new key to the template and to `reference/roast-variables.md` in the same change, never to one file alone.
- Do not delete or rewrite a past roast's recorded data. Correct a mistake in place and say so in the file's `notes`.

## Git

- Colin is the author, with a `Co-Authored-By` trailer for the agent.
- Short imperative subject. A plain-language body says what changed and why.
- Before staging, inspect `git status` and the complete diff. Stage only files that belong to the task. Do not use `git add .` or `git add -A`.
- This repository authorizes the agent to commit and push completed, validated changes directly to `origin/main`. Commit and push at the end of each completed task, such as a planned roast, a recorded roast, or a reference update. Do not leave finished work uncommitted.
- Push with `git push origin main`, then confirm that `main` and `origin/main` point to the same commit.
- Never force-push or rewrite history. If validation, commit or push fails, leave the worktree intact and report the failure; the task is not complete.
- App code, when it starts, works on a branch and does not push until Colin asks. See `TASKS.md`.
- The repository is public. Never commit secrets, signing keys, `local.properties`, or personal details beyond what is already here.

## Validation

Documentation and roast-log changes need `git diff --check`, a check that every relative Markdown link resolves, and `agent-profile check .`. A roast file must also keep the template's front-matter keys.

<!-- BEGIN AGENT PROFILE BOOTSTRAP -->
<!-- SOURCE SHA256: d5a06d5c885fcd56aa5e3fed2e790cbb82b0e67ccdbb8f47e2c470763e7c8825 -->
## Agent Profile

Before substantial planning or implementation:

1. Read `README.md`.
2. Read `docs/agent/PREFERENCES.md`.
3. Read relevant architecture or subsystem documentation.
4. Read `docs/agent/DECISIONS.md` before reconsidering established design choices.
5. Consult `docs/agent/LEARNINGS.md` when useful, but treat it as non-authoritative.

Small and obvious tasks do not require exhaustive repository reading. Explicit current-task instructions override standing preferences. Repository requirements, contracts, documented decisions, and repository-specific preferences override global defaults.

If documented preferences reasonably answer an ordinary engineering question, use them instead of asking again. Ask about ambiguity that is materially consequential, destructive, expensive to reverse, architecturally significant, or genuinely unresolved.

### Preference Learning

- Apply the maintainer's answer to the current task first.
- If a clarification is likely to recur, check whether it is already documented.
- Record an apparently reusable but unconfirmed preference in `docs/agent/LEARNINGS.md` with scope, confidence, context, and likely future value.
- Do not promote weak or one-off evidence into authoritative preferences.
- Record significant project decisions in `docs/agent/DECISIONS.md`, not in the learnings queue.
- Promote repeated or explicitly confirmed repository preferences into the local section of `docs/agent/PREFERENCES.md`.
- Propose cross-repository preferences for conservative review in the canonical agent-profile repository; do not silently mutate global preferences.

When the `agent-profile` command is available, `agent-profile check .` is safe during read-only work. Run `agent-profile sync .` only when repository edits are authorized. The committed snapshot remains authoritative for this repository when the command is unavailable.
<!-- END AGENT PROFILE BOOTSTRAP -->
