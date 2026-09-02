# Reports Archive

Finished, signed-off weekly status reports live here — one Markdown file per week.

## Naming convention

```
reports/YYYY-MM-DD_to_YYYY-MM-DD.md
```

Example: `reports/2026-08-26_to_2026-09-02.md`

This matches the filename that `index.html`'s **Download Markdown** button (or `report.html`'s copy of the same button) generates automatically, so you can drop the downloaded file straight into this folder without renaming it.

## Adding a week's report

1. On `index.html`, fill out the form, get everyone signed off, then click **Save & View Report**.
2. On `report.html`, click **Download Markdown** to save the `.md` file to your computer.
3. Add that file to this `reports/` folder and commit it (see the two methods below).

### Option A — GitHub's web interface (no git required)

1. Open this repo on GitHub and navigate into the `reports` folder (or the repo root if `reports` doesn't exist yet).
2. Click **Add file → Upload files**, then drag in the downloaded `.md` file — or click **Add file → Create new file**, type `reports/2026-08-26_to_2026-09-02.md` as the filename (typing the `/` creates the folder for you if it doesn't exist), and paste in the file's contents.
3. Scroll down, add a commit message (e.g. "Add Week of 8/26-9/2 status report"), and click **Commit new file**.

### Option B — Git command line

```bash
# from your local clone of the repo
cp ~/Downloads/Commercial-Readiness-Weekly-Status-2026-08-26_to_2026-09-02.md reports/
git add reports/2026-08-26_to_2026-09-02.md
git commit -m "Add Week of 8/26-9/2 status report"
git push
```

## Optional: keep the README in sync

The report block at the top of the repo's main `README.md` is meant to always show the *current* week. When you archive a finished report here, you can also paste the same content into that block so anyone landing on the repo sees the latest report first.
