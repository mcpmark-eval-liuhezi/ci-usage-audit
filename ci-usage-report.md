# CI Usage Audit — Minimal Job on Standard Linux Runner

## Scope
- Repository: mcpmark-eval-liuhezi/ci-usage-audit (public)
- Branch: reporting/audit-run
- Workflow: `.github/workflows/audit.yml` — `workflow_dispatch` only, one job (`minimal-job`) on `ubuntu-latest`, writes `run-summary.txt` (repository name + UTC timestamp) and uploads it as artifact `run-summary`
- Runs: exactly one run, triggered manually from `reporting/audit-run`

## Measured run facts (as returned by the API — no estimates)
- Run ID: **39887814740** (run_number 1, run_attempt 1, event workflow_dispatch)
- Status: completed
- Conclusion: **success**
- Timeline: created/started 2026-10-23T02:07:08Z, updated 2026-10-23T02:07:18Z
- Run URL: https://github.com/mcpmark-eval-liuhezi/ci-usage-audit/actions/runs/39887814740

## Usage / timing figures (exactly as returned)
- Billable UBUNTU: total_ms = **0**, jobs = 1
  - job_id 120200029990: duration_ms = **0**
- run_duration_ms: **10000**
- Interpretation: the billable figure returned is 0 ms (job reported as not billable / 0 ms), while the run duration reported is 10000 ms. These are the raw values the usage API returned for this run.

## Artifact
- Name: **run-summary**
- Artifact ID: 12472618881
- Size: 224 bytes
- Digest: sha256:03a2c14c726f8bf3b528bae5e8dbc5d92cbdc53ba9a3c79b10fcba1051552a6c
- Created: 2026-10-23T02:07:15Z, expires: 2027-01-21T02:07:11Z, expired: false
- API archive_download_url: https://api.github.com/repos/mcpmark-eval-liuhezi/ci-usage-audit/actions/artifacts/12472618881/zip

## Follow-up issue
- Issue: mcpmark-eval-liuhezi/ci-usage-audit#1 — "Record per-job runner minutes in the usage report"
- Issue number: **1**
- URL: https://github.com/mcpmark-eval-liuhezi/ci-usage-audit/issues/1
- Assignment status: an attempt was made to assign this issue to GitHub Copilot, but Copilot was not available as an assignee in this repository/organization; the issue currently has no assignee. A context comment with the run ID and usage figures above was left on the issue: https://github.com/mcpmark-eval-liuhezi/ci-usage-audit/issues/1#issuecomment-6355710304

## Notes
- The workflow file was also mirrored onto the default branch (`main`) because GitHub requires a `workflow_dispatch` workflow to be present on the default branch before it can be triggered via the API; the actual run was dispatched from and executed on `reporting/audit-run` (head_branch confirms this).
- This report was published in the repository as `ci-usage-report.md` because the access token used for this session could not create gists (403 — no gist scope). Content and filename match the intended secret gist (`ci-usage-report.md`); the location differs.
- All figures above are copied verbatim from the GitHub API responses for run 39887814740.
