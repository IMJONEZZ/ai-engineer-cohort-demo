# AI Engineer Program — Demo Cohort

Course materials for the AI Aspire **AI Engineer Program** demo cohort.
This repository is read by the AI Aspire platform: link it to a cohort as a
curriculum source and the platform ingests it — units, sessions, slide decks,
and pre-work — versioned per sync, published per cohort.

## How this repository is organized

```
00_Prework/            What every learner completes before Day 1
Day_1_Foundations/     Context engineering, retrieval, RAG, agents, MCP
Day_2_Orchestration/   Workflow orchestration, state machines, multi-agent
```

Each day holds:

- `sessions/` — Jupyter notebooks, in teaching order (`S1_…`, `S2_…`).
  Committed outputs come from a real run; every notebook executes offline
  with no paid API keys.
- `slides/` — the day's deck as ordered images, exported once and committed.

## Conventions the platform understands

- Directory names carry the ordering (`Day_1_…`, `S1_…`). No manifest is
  required — a `curriculum.json` can override titles or ordering, but this
  branch deliberately ships without one.
- A session's display title is the notebook's first `# Heading`, not its
  filename.
- Pre-work steps are the numbered folders under `00_Prework/`; `## Windows`,
  `## macOS`, and `## Linux` headings become per-OS instructions.

## Running the notebooks yourself

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install jupyter
jupyter lab
```

Every notebook is self-contained and deterministic: model calls go through a
small `DemoLLM` stand-in so the material teaches the *patterns* — retrieval,
agent loops, orchestration — without network access or credentials. Swapping
`DemoLLM` for a real client is a one-cell change and is left as an exercise
in each lab.
