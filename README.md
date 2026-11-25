# Robot RSI Research Hub

Public archive: https://icgrey.github.io/-Robot-RSI-Research-Hub/

Independent research index for **Robot Harness / Embodied Recursive Self-Improvement**. It is separate from the robot experiment website and the World Model research feed.

## Data format and immutability

- `data/papers.json`: canonical paper index keyed by **arXiv ID**; maintain `versions[]` append-only to retain old revisions.
- `data/daily-index.json`: newest-first list of report dates.
- `daily/YYYY-MM-DD.json`: each dated report; **do not overwrite historical days**.
- A same-paper v2/v3 update gets appended under its existing arXiv record, while its updated publication is noted in the *new* daily report.

## Screening

Prioritize robot feedback → failure attribution → code/skill/harness/memory revision → paired/held-out validation → retained improvement, with emphasis on frozen VLA + atomic skills + MLLM/VLM agents and executable runtime contracts.

Do **not** mistake task-internal retry, standard VLA post-training, generic coding-agent RSI, or world-model/video generation for robot harness RSI.

Historical research reports dated 2026-11-14 through 2026-11-21 and 2026-11-25 have been restored from the accessible original chat reports. Interactive figures are converted to equivalent text or tables; chat-internal citation IDs are not external links. Reports dated 2026-11-10 through 2026-11-13 remain explicitly labeled summary-only because original bodies were unavailable. No new verification of historic research claims is implied.

## New daily issue workflow

1. Write a new `daily/YYYY-MM-DD.json` report with `body_markdown` containing the complete Chinese report (headings, tables, data, source URLs, conclusions), `archive_status: "full"`, `date`, `title`, `conclusion`, `items`, and `notes`. Do not omit analysis or numerical data.
2. Prepend the date to `data/daily-index.json`.
3. `data/papers.json` is a manually curated library. Never add new entries automatically. Only append verified new versions to already selected paper IDs; preserve prior versions.
4. Commit to `main`. GitHub Pages publishes the static site.

The site does not run searches itself. Automatic publication requires the existing ChatGPT scheduled research task with access to the GitHub connector.
