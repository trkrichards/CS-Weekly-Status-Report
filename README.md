# Commercial Readiness Weekly Status Report

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

## How the two pages work together

This repo has two pages:

- **`index.html`** — the fillable form. This is where you enter updates.
- **`report.html`** — a separate, read-only report page. This is where you (or anyone) view the finished report.

Clicking **Save & View Report** on `index.html` saves your entries, then navigates to `report.html?week=<the selected week>`, which reads that saved data and renders it as a clean report — no form controls, just the content. Use **← Back to Edit** on `report.html` to return to the form.

**Print / Export PDF** on `index.html` does the same save-and-navigate, but opens `report.html` in a new tab with printing triggered automatically, so you get a clean printout without ever seeing the form.

### A note on where the data lives

There's no backend or database here — everything is saved to the browser's `localStorage`, keyed by the week (e.g. `crw-draft-2026-08-26`). That means:

- Draft data is per-browser, not shared between teammates. Whoever is the primary editor for the week should be the one filling in `index.html` and generating the report.
- `localStorage` is shared between `index.html` and `report.html` as long as they're opened from the **same web address** (same domain, e.g. both on the same GitHub Pages site). If you open the files directly from your computer (double-clicking, `file://` links) some browsers isolate local storage per file and `report.html` may not find the data — publish via GitHub Pages (below) for reliable behavior, or run a simple local server if testing before publishing.

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
3. Replace the report block at the top of this README with that content (or commit it to a `/reports` folder, e.g. `reports/2026-08-26_to_2026-09-02.md`, for a running archive) — a version-controlled record replacing the separate Word docs.

## Updating the active project list

The active projects are hardcoded in **both** `index.html` and `report.html`, in an `ACTIVE_PROJECTS` array near the top of each `<script>` block. When a project closes, is cancelled, is added, or a paused project resumes, update that array in both files (add/remove a string from the relevant category's `items` list) — they need to stay in sync since each file builds its own copy of the report independently.

## Publishing with GitHub Pages

1. Push this folder to GitHub.
2. **Settings → Pages** → set **Source** to "Deploy from a branch," branch `main`, folder `/ (root)` (or wherever this folder lives in the repo).
3. GitHub publishes it at `https://<your-username>.github.io/<repo-name>/`.

## Files

- `index.html` — the fillable form.
- `report.html` — the read-only report view that `index.html` links to.
- `README.md` — this file (current report + usage instructions).
