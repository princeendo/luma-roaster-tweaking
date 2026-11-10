# Project Decisions

This document records significant architectural and project decisions. It is authoritative for decisions that remain current. Do not record trivial implementation choices.

## Entry Template

### YYYY-MM-DD: Decision title

- **Decision:** What was decided.
- **Context:** The problem, constraint, or trigger.
- **Rationale:** Why this choice best fit the available evidence.
- **Consequences:** Important tradeoffs, follow-up work, or constraints.
- **Alternatives considered:** Material alternatives and why they were not selected.

## Decisions

### 2026-11-10: Roast and bean records are Markdown files with YAML front matter

- **Decision:** One file per roast in `roasts/` and one per green-coffee lot in `beans/`. Structured data lives in YAML front matter whose keys are defined in `reference/roast-variables.md`. Temperatures in °C, weights in grams, event times as `mm:ss` from the start of heating.
- **Context:** Roasts are planned and recorded in conversation with an agent now, and a phone app is planned later.
- **Rationale:** Agents read and edit Markdown easily, Git keeps history, and front matter is simple for an app to parse. °C matches the roaster's display.
- **Consequences:** The front-matter keys are a contract. Changing one means updating the template and the dictionary together, and later the app.
- **Alternatives considered:** A spreadsheet or CSV (hard to hold free-text tasting and plan notes); a database (too early, and hard for an agent to edit).

### 2026-11-10: Reference knowledge is labeled by source

- **Decision:** Every planning statement is labeled as **manual**, **observed** (with roast IDs) or **external guidance**. `reference/roaster-profile.md` holds machine knowledge in those categories plus open hypotheses.
- **Context:** The manual's roast table and chart disagree, and the roaster has no bean probe.
- **Rationale:** Keeps tested facts apart from assumptions, so the plan improves as roasts accumulate.
- **Consequences:** A hypothesis becomes "observed" only with roast evidence.
- **Alternatives considered:** One merged guide (loses track of what has been verified).

### 2026-11-10: Commit and push roast work to `main`; app work on branches

- **Decision:** The agent commits and pushes completed, validated roast logs and reference updates directly to `origin/main`. App code uses a branch and is pushed only when Colin asks.
- **Context:** Roast logging produces many small documentation changes. App code needs review.
- **Rationale:** Matches Colin's other documentation repositories (for example `tv-box-management`) and his app repositories (for example `prayer-reminder-app`).
- **Consequences:** Every finished roast plan or record lands on GitHub right away. The repository is public.
- **Alternatives considered:** Branch-and-ask for everything (too much friction for logging).
