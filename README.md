# CLH Weekly Status

A single-page status report for the Clinical Learning Hub (CLH) workstreams — migrations, SSO/onboarding, Q3 readiness, and support signals — published as a static site.

## Viewing the report

Open `index.html` directly in a browser, or publish it with GitHub Pages (see below) for a shareable link.

## Updating the report

The report is one static HTML file with no build step.

1. Open `index.html` in any text editor.
2. Update the `<span id="genDate">` line in the header with the current date.
3. Edit the content inside each `<section>` — each status line is a `<div class="item">`. Copy an existing item to add a new one.
4. Use the tag classes to flag status at a glance:
   - `tag risk` — red, for blocked/overdue items
   - `tag watch` — yellow, for items to monitor
   - `tag ok` — green, for resolved/on-track items
5. Commit and push. If GitHub Pages is enabled, the live page updates automatically within a minute or two.

## Publishing with GitHub Pages

1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch."
4. Select the `main` branch and `/ (root)` folder, then save.
5. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`.

## Collecting updates

There are two ways for teammates to submit a status update — both feed the same content into `index.html`.

### Option A: `form.html` (fillable page, hosted on GitHub Pages)

A plain HTML form with the same fields as the GitHub Issue Form below. It needs no backend, so it works as a page on GitHub Pages.

1. Open `form.html` and set `GITHUB_OWNER` and `GITHUB_REPO` near the bottom of the file to your repo's owner/name.
2. Once published, it's linked from the report page via **Submit an update →** in the header, or can be shared directly as `.../form.html`.
3. Whoever fills it out has two options:
   - **Copy HTML snippet** — copies a ready-made `<div class="item">` block to paste straight into the matching section of `index.html`.
   - **File as GitHub issue** — opens a new tab with GitHub's Weekly Status Update issue form pre-filled from what they typed, so the submission is tracked in **Issues** before being folded into the report.

### Option B: GitHub Issue Form directly

`.github/ISSUE_TEMPLATE/weekly-status-update.yml` adds a GitHub Issue Form so teammates can submit updates without using `form.html` at all.

1. Push this repo to GitHub — the form appears automatically under the repo's **Issues → New issue** button (labeled "Weekly Status Update").
2. Anyone with access to the repo can fill it out: workstream, item title, status, owner, week, update details, and next steps.
3. Submitted issues are tagged with the `status-update` label, so you can filter **Issues** by that label to see everything submitted for the week.
4. Fold each submission into `index.html` as a new `<div class="item">` in the matching `<section>`, then close the issue once it's been incorporated.
5. `.github/ISSUE_TEMPLATE/config.yml` disables blank issues so all submissions go through the structured form; update the placeholder `OWNER/REPO` link in that file once the repo is created.

## Files

- `index.html` — the status report page.
- `form.html` — fillable form for submitting a status update (no backend required).
- `.github/ISSUE_TEMPLATE/weekly-status-update.yml` — the GitHub Issue Form teammates can also use directly.
- `.github/ISSUE_TEMPLATE/config.yml` — issue template settings.
- `README.md` — this file.
