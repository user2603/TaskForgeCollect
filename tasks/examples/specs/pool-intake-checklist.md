# Pool Intake Checklist

The checklist the review team walks through for every intake round. The
authoritative thresholds live in `specs/acceptance-rules-2026H2.md`; this
checklist is a summary, not a replacement.

1. Inventory every dev branch and the jobs waiting in `tasks/staging/`.
2. For each job not yet in the tracker: check the required files
   (`docs/task.md` and `evaluation/main.py`) and decide `implemented` /
   `implementing`.
3. Count the `.py` files directly under the job's `tests/` folder and assign
   the tier: `gold` at 8 or more, `silver` from 4 to 7, `bronze` below 4.
4. Add one tracker row per new job (name, status, tier, author handle).
   Leave every pre-existing row untouched, including its empty tier cell.
5. Import only implemented + gold jobs into `tasks/releasepool/`, using the
   lean two-file format.
6. Read everything back and compare before calling the round done.

If the wording here ever disagrees with `specs/acceptance-rules-2026H2.md`,
fix the pointer in the index (`tasks/examples/README.md`) and follow the
operative rules document.
