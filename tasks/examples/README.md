# Examples & Rules Index

Everything about how a job folder is built, reviewed, and promoted inside
TaskForgeCollect is decided in this directory. Read this index first.

## Where the current rules live

The acceptance rules currently in force are maintained in
`specs/acceptance-rules-2025H1.md`. That document defines the required files,
the maturity tiers, and the pool-import format used by every review round.

## Before you import anything

Walk through `specs/pool-intake-checklist.md` before copying a single file
into a pool branch; it is the step-by-step checklist the review team uses
for every intake round.

## Folder layout

`tasks/mainpool/` holds the jobs accepted before the tier system existed.
`tasks/staging/` is where a new job lands on its author's dev branch, and a
job only leaves staging when it is imported into a pool branch.

## History

The retired 2025 H1 rules are kept at `specs/acceptance-rules-2025H1.md`
for archaeology; nothing in them applies anymore.
