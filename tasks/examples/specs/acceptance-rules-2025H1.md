# Acceptance Rules - 2025 H1

> STATUS: ARCHIVED. Superseded by `specs/acceptance-rules-2026H2.md` as of
> 2026-07-01. Do not run an intake round with this document.

These rules were used for intake rounds before the 2026 revision.

## Required files

A job folder must contain `docs/task.md`, `docs/plan.md`, and
`evaluation/main.py`. A folder that misses any of the three counts as
implementing.

## Maturity tiers (retired scale)

Count the files under the job's `tests/` directory:

- Gold: 6 or more
- Silver: 3 to 5
- Bronze: fewer than 3

## Pool import (retired format)

Copy the entire job folder, including `tests/`, into the pool branch.
