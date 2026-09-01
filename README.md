# CS-Weekly-Status-Report
CS Weekly Status Report 

A single-page status report for the Clinical Learning Hub (CLH) workstreams â€” migrations, SSO/onboarding, Q3 readiness, and support signals â€” published as a static site.

## Viewing the report

Open `index.html` directly in a browser, or publish it with GitHub Pages (see below) for a shareable link.

## Updating the report

The report is one static HTML file with no build step.

1. Open `index.html` in any text editor.
2. Update the `<span id="genDate">` line in the header with the current date.
3. Edit the content inside each `<section>` â€” each status line is a `<div class="item">`. Copy an existing item to add a new one.
4. Use the tag classes to flag status at a glance:
   - `tag risk` â€” red, for blocked/overdue items
   - `tag watch` â€” yellow, for items to monitor
   - `tag ok` â€” green, for resolved/on-track items
5. Commit and push. If GitHub Pages is enabled, the live page updates automatically within a minute or two.

## Publishing with GitHub Pages

1. Push this repo to GitHub.
2. In the repo, go to **Settings â†’ Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch."
4. Select the `main` branch and `/ (root)` folder, then save.
5. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`.

## Collecting updates with the fillable form

`.github/ISSUE_TEMPLATE/weekly-status-update.yml` adds a GitHub Issue Form so teammates can submit their own status updates without editing HTML.

1. Push this repo to GitHub â€” the form appears automatically under the repo's **Issues â†’ New issue** button (labeled "Weekly Status Update").
2. Anyone with access to the repo can fill it out: workstream, item title, status, owner, week, update details, and next steps.
3. Submitted issues are tagged with the `status-update` label, so you can filter **Issues** by that label to see everything submitted for the week.
4. Fold each submission into `index.html` as a new `<div class="item">` in the matching `<section>`, then close the issue once it's been incorporated.
5. `.github/ISSUE_TEMPLATE/config.yml` disables blank issues so all submissions go through the structured form; update the placeholder `OWNER/REPO` link in that file once the repo is created.

## Files

- `index.html` â€” the status report page.
- `.github/ISSUE_TEMPLATE/weekly-status-update.yml` â€” the fillable form teammates use to submit updates.
- `.github/ISSUE_TEMPLATE/config.yml` â€” issue template settings.
- `README.md` â€” this file.

