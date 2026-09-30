# Acceptance Rules - 2026 H2

> STATUS: IN FORCE since 2026-07-01. This document governs every intake
> round in TaskForgeCollect. If any other document disagrees with this one,
> this one wins.

## Scope

These rules apply to NEW jobs landing in `tasks/staging/` on a dev branch.
Jobs already tracked in the Notion "Task Tracker" page were accepted under
earlier rounds and must not be re-reviewed, re-worded, or re-tiered.

## Required files

A new job folder must contain BOTH `docs/task.md` AND `evaluation/main.py`.
No other file is required. A folder that has both is implemented; a folder
that misses either one is implementing.

Write the status in the tracker exactly as `implemented` or `implementing`,
all lowercase, and nothing else.

## Maturity tiers

Count the files whose names end with `.py` directly under the job's
`tests/` directory (if the folder has no `tests/` directory, the count is
zero). Assign exactly one tier per new job:

- Gold: 8 or more test files
- Silver: at least 4 and fewer than 8 test files
- Bronze: fewer than 4 test files

Write the tier in the tracker's `Maturity Tier` column exactly as `gold`,
`silver`, or `bronze`, all lowercase.

## Pool membership

A new job enters the release pool this round if and only if all three hold:

1. it is a new job (no row in the tracker before this round),
2. its status is `implemented`,
3. its tier is `gold`.

No already-tracked job ever enters the pool in this round, whatever its
historical status is.

## Pool import format (lean import)

For every job that enters the pool, create the folder
`tasks/releasepool/<job-name>/` on the `releasepool` branch containing
EXACTLY two files:

- `docs/task.md`
- `evaluation/main.py`

Copy both files byte for byte from the branch tip where the job lives. Do
not bring any other file (no `tests/`, no extra docs), do not reformat, and
do not rename anything inside the job folder.

## Author handle

Use the author's handle exactly as it appears in the commit author field,
and put it in the tracker's `Implementor` column. One handle per row.

## Tracker updates

Add exactly one row per new job to the "Task Tracker" database. Never
rename, edit, or remove rows that are already there, and never fill the
`Maturity Tier` cell of an already-tracked row: the tier column stays empty
for every pre-existing row.
