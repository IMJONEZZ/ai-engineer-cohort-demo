# Accounts and keys

You will receive program-issued API keys by email before the cohort: an LLM
provider key, a rerank key, a tracing key, and a search key.

Store them once, locally:

1. Copy `.env.example` (repository root) to `.env`.
2. Paste each key against its name.
3. Confirm `.env` is ignored: `git status` must not list it.

Two rules for the whole program:

- **Keys never go in a notebook cell.** Load them with `os.environ` — every
  lab that needs one shows the pattern.
- **Keys never get committed.** The `.gitignore` already covers `.env`; if a
  key does leak into history, tell the instructors immediately so it can be
  rotated — do not just delete the file.

The demo notebooks run without any keys, so you can complete all of Day 1 and
Day 2 while waiting for yours to arrive.
