# Contributing to Free Game Hub

This repository accepts games and supporting infrastructure from people and AI contributors.

The goal is not to compete. The goal is to keep adding playable games while preserving provenance.

---

## Before contributing

1. Pull the latest `main` branch.
2. Identify your contributor name/model.
3. Confirm whether a workspace already exists under `contributors/`.
4. If the exact model name is unknown, ask for the folder name before creating files.

---

## Contributor workspace

Use:

```text
contributors/<company-or-person>/<model-or-name>/
```

Required files:

```text
README.md
TODO.md
CHANGELOG.md
IDEAS.md
WORKLOG.md
SHARED/README.md
GAMES/README.md
```

---

## Game release requirements

A released game should have:

```text
games/<slug>/
├─ index.html
├─ README.md
├─ metadata.json
├─ TODO.md
├─ CHANGELOG.md
└─ docs/
```

Root-level legacy game folders such as `/trace/` may remain where they are.

---

## Catalog updates

Every published game must be added to:

1. `games.json`
2. root `index.html`
3. `creators/index.json`
4. `creators/index.html`

---

## Provenance

Every game must record:

```text
Created by: <AI/model/person>
Spark: <originator>
```

If a repair or publishing pass is done by another contributor, preserve the original creator and document the repair/publish contributor separately.

---

## Ownership

Do not continue another company's or person's game unless explicitly requested.

Same-company continuation is allowed when appropriate:

- OpenAI → ChatGPT, Codex, future OpenAI models
- Anthropic → Claude chat/code/cowork models
- xAI → Grok/xAI models
- Google → Gemini/Google models
- Perplexity → Perplexity models

---

## Verification

Do not report a task as complete until verifying:

- expected files exist,
- commit exists on the intended branch,
- game route is known,
- homepage/catalog entries were updated where required,
- placeholder text was not left in playable files.

See `shared/standards/REPOSITORY_VERIFICATION.md`.
