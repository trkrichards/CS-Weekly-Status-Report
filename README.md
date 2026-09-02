# Commercial Readiness Weekly Status Report

Repo: [trkrichards/CS-Weekly-Status-Report](https://github.com/trkrichards/CS-Weekly-Status-Report)

## Week of 8/26 – 9/2

### Summary
_Not yet entered — fill in via `index.html`._

### Active Projects

**Physician and Pharmacist Initiatives**
- ClinicalKey Unified Vision (CK+?): No updates
- ClinicalKey for Nursing Unified Vision (CKN+?): No updates
- ClinicalKey (CK) Physician BAU: No updates
- CK AI BAU: No updates
- CPCK BAU: No updates
- CK for Medical Schools BAU: No updates
- CK Test Prep BAU: No updates
- NEOID LMS Access CK Student: No updates

**Nursing and Patient Education Initiatives**
- Clinical Learning Hub: No updates
- CK Student NOAM/Clinical Cases BAU: No updates
- CK Nursing BAU: No updates
- Patient Pass/PE Products BAU: No updates
- Clinical eLearning BAU: No updates

**Specialist Solution Initiatives**
- ClinicalPath BAU: No updates
- ClinicalPath Provider Reports: No updates
- PSS BAU: No updates

**Strategic/Corporate Initiatives**
- eLearning Localization: No updates

**Miscellaneous**
- Project Phoenix Admin Console: No updates

**Other / Miscellaneous:** _Not yet entered._

### Out of Office
- Kelly: None
- Barry: None
- Tessa: None
- Laura: None
- Andrew: None
- Jan: None

### Recognition
_Not yet entered._

### Sign Off
- [ ] Kelly — not yet signed
- [ ] Barry — not yet signed
- [ ] Tessa — not yet signed
- [ ] Laura — not yet signed
- [ ] Andrew — not yet signed
- [ ] Jan — not yet signed

---

> The section above reflects the current, unfilled draft state of `index.html`. Fill out the form there, and once everyone has signed off, replace this block with the output of **Download Markdown** so this README always shows the latest completed report.

## About this repo

A fillable version of the Commercial Readiness Weekly Status Report, organized around the team's active projects. This is a separate repo/site from the CLH Weekly Status report.

Closed, cancelled, and paused initiatives from the source report aren't listed individually — anything outside the active project list (e.g. Gong, CS Customer Centric Standup, ADA file conversion) goes in the **Other / Miscellaneous** field.

## Pages in this repo

- **`index.html`** — the fillable form. Where you enter updates.
- **`report.html`** — a read-only view of the report you just saved, for one specific week.
- **`view-reports.html`** — browses every report that's been committed to `reports/`, pulled live from GitHub. Click a report to expand a rendered preview, or open it raw / on GitHub.
- **`reports/`** — the archive folder for finished, signed-off weekly reports as Markdown files (see `reports/README.md`).

Clicking **Save & View Report** on `index.html` saves your entries, then navigates to `report.html?week=<the selected week>`, which reads that saved data and renders it as a clean report — no form controls, just the content. Use **← Back to Edit** on `report.html` to return to the form, or **View Reports** to see the archive.

**Print / Export PDF** on `index.html` does the same save-and-navigate, but opens `report.html` in a new tab with printing triggered automatically, so you get a clean printout without ever seeing the form.

### View Reports configuration

`view-reports.html` lists files by calling the public GitHub Contents API for this repo — already configured for this repo:

```js
const GITHUB_OWNER = "trkrichards";
const GITHUB_REPO = "CS-Weekly-Status-Report";
```

A few things worth knowing about this approach:
- It calls `https://api.github.com/repos/trkrichards/CS-Weekly-Status-Report/contents/reports`, which works with no login as long as the repo is public. If the repo is private, the browser can't authenticate to this API, so the page will show an error with a link to browse `reports/` on GitHub directly instead.
- Unauthenticated GitHub API calls are limited to 60/hour per visitor's IP — plenty for normal use, but worth knowing if it stops working temporarily after heavy testing.
- Nothing needs to be regenerated when a new report is added — the page reflects whatever is currently committed to `reports/`.
- If this repo is ever renamed or transferred to a different account, update `GITHUB_OWNER`/`GITHUB_REPO` at the top of `view-reports.html` to match.

### A note on where the draft data lives

There's no backend or database for the *in-progress* form — everything is saved to the browser's `localStorage`, keyed by the week (e.g. `crw-draft-2026-08-26`). That means:

- Draft data is per-browser, not shared between teammates. Whoever is the primary editor for the week should be the one filling in `index.html` and generating the report.
- `localStorage` is shared between `index.html` and `report.html` as long as they're opened from the **same web address** (same domain, e.g. both on the same GitHub Pages site). If you open the files directly from your computer (double-clicking, `file://` links) some browsers isolate local storage per file and `report.html` may not find the data — publish via GitHub Pages (below) for reliable behavior, or run a simple local server if testing before publishing.
- Once a report is downloaded and committed to `reports/`, it's no longer dependent on `localStorage` at all — that's the point of the archive, and why `view-reports.html` reads from GitHub instead.

## Using the form

Open `index.html` in a browser (or the published GitHub Pages link). No install, no login.

- **Week of** — the two date fields at the top control which draft is loaded/saved. Changing them switches to that week's draft.
- **Summary** — the one mandatory highlight bullet for the week.
- **Active Projects** — one row per currently active initiative, grouped the same way as the source report. Each row has an **Update this week?** dropdown:
  - **No updates** (default) — nothing more to do for that project.
  - **Yes — add update** — reveals a text box below the row to fill in.
  - A row with an update is highlighted so it's easy to see what's changed at a glance.
- **Other / Miscellaneous** — a catch-all for anything that isn't tied to one of the listed active projects.
- **Out of Office** — a line per team member for planned time out this week; leave blank if none.
- **Recognition** — free text, per the report's own rule to recognize at least one teammate each week.
- **Sign Off** — each of the six names (Kelly, Barry, Tessa, Laura, Andrew, Jan) has a checkbox. Checking it records that person's sign-off with a timestamp. The counter above shows how many of 6 have signed.
- **Download Markdown** — grabs a `.md` snapshot directly from the form, without navigating to `report.html`.
- **Clear Draft** — wipes the current week's saved data.

## Publishing the finished report

Once everyone has signed off:

1. Click **Save & View Report** for a final read-through on `report.html`.
2. Click **Download Markdown** (available on both pages) to generate a `.md` file of the completed report.
3. Add that file to the `reports/` folder in this repo — see `reports/README.md` for the naming convention and step-by-step instructions (GitHub web UI or git command line) for committing it.
4. It will now show up on `view-reports.html` automatically.
5. Optionally, also replace the report block at the top of this README with the same content, so anyone landing on the repo sees the latest report first.

## Updating the active project list

The active projects are hardcoded in **both** `index.html` and `report.html`, in an `ACTIVE_PROJECTS` array near the top of each `<script>` block. When a project closes, is cancelled, is added, or a paused project resumes, update that array in both files (add/remove a string from the relevant category's `items` list) — they need to stay in sync since each file builds its own copy of the report independently.

## Publishing with GitHub Pages

1. Push this folder to `github.com/trkrichards/CS-Weekly-Status-Report`.
2. **Settings → Pages** → set **Source** to "Deploy from a branch," branch `main`, folder `/ (root)` (or wherever this folder lives in the repo).
3. GitHub publishes it at `https://trkrichards.github.io/CS-Weekly-Status-Report/`.

## Files

- `index.html` — the fillable form.
- `report.html` — the read-only report view that `index.html` links to.
- `view-reports.html` — browses the full archive of committed reports.
- `reports/` — archive of finished, signed-off weekly reports (Markdown files).
- `README.md` — this file (current report + usage instructions).
