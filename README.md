# Commercial Readiness Weekly Status Report

A fillable, sign-off-ready version of the Commercial Readiness Weekly Status Report — the same report that's been circulating as a Word doc, now a single HTML page. This is a separate repo/site from the CLH Weekly Status report.

Pre-filled for **Week of 8/26 – 9/2**, with project statuses and cumulative stats carried forward from the 8/19–8/26 report.

## Using it

Open `index.html` in a browser (or the published GitHub Pages link). No install, no login.

- **Week of** — the two date fields at the top control which draft is loaded/saved. Changing them switches to that week's draft.
- **Summary** — the one mandatory highlight bullet for the week.
- **Sign Off** — each of the six names (Kelly, Barry, Tessa, Laura, Andrew, Jan) has a checkbox. Checking it records that person's sign-off with a timestamp, shown next to their name. The counter above shows how many of 6 have signed.
- **Projects & Status** — the standing project list, grouped the same way as the doc, with a status dropdown (Active / Closed / Cancelled / Paused) per project.
- **Workstream Updates** — collapsible sections (Gong, CLH/EPM/TTP, ClinicalKey, PSS Products, CS Standup, MISC) with a text field per topic, matching the doc's structure. Migration lists and the ADA file-conversion counters are pre-filled from the last report; percentages recalculate automatically as counts change.
- **People** — Recruiting & People, Recognition, and the OfficeVibe metric.

### Saving your work

The page autosaves to your browser's local storage as you type (per week), so refreshing or closing the tab won't lose progress. **Save Draft** saves immediately and shows a timestamp; **Clear Draft** wipes the current week's saved data.

Autosave is per-browser, not shared — it's meant to protect your own in-progress edits, not to sync between teammates. Whoever is the primary editor each week should be the one filling this in and exporting it.

### Publishing the finished report

Once everyone has signed off:

1. Click **Download Markdown** to generate a `.md` file of the completed report (sign-offs, project statuses, and all workstream updates).
2. Commit it to a `/reports` folder in this repo (e.g. `reports/2026-08-26_to_2026-09-02.md`) so the team has a running, version-controlled archive — replacing the separate Word docs.
3. Alternatively, use **Print / Export PDF** to generate a clean, form-free printable version for anyone who wants a PDF/paper copy.

## Publishing with GitHub Pages

1. Push this folder to GitHub.
2. **Settings → Pages** → set **Source** to "Deploy from a branch," branch `main`, folder `/ (root)` (or wherever this folder lives in the repo).
3. GitHub publishes it at `https://<your-username>.github.io/<repo-name>/`.

## Files

- `index.html` — the fillable report.
- `README.md` — this file.
