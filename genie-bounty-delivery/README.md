# Weekly GitHub Dev Summary — n8n + Claude

Delivery for: [BOUNTY $200] WORKFLOW: n8n + Claude Code — automated weekly dev summary

## Setup (5 steps)
1. Import `weekly-summary.workflow.json` into n8n (Workflows → Import from File).
2. Add Header Auth credential for GitHub API (`Authorization: Bearer <token>`).
3. Set env vars: `GITHUB_REPO`, `ANTHROPIC_API_KEY`, `DISCORD_WEBHOOK_URL`, optional `SUMMARY_LANG` (EN/FR), `DESTINATION`.
4. Attach the GitHub credential to the three GitHub HTTP Request nodes.
5. Execute once manually, confirm Discord delivery, then activate the Friday 17:00 cron.

## What it does
- Weekly cron (Friday 17:00)
- Fetches commits, closed issues, merged PRs for the last 7 days
- Calls Claude (`claude-sonnet-4-20250514`) for a narrative summary
- Delivers via Discord webhook (documented; swap URL for Slack if preferred)

## Acceptance mapping
- [x] Exportable n8n workflow (importable `.json` file)
- [x] Trigger: weekly cron (e.g., Friday at 5pm)
- [x] Fetches from GitHub API: commits, closed issues, merged PRs for the week
- [x] Calls Claude API (`claude-sonnet-4-20250514`) to generate a narrative summary
- [x] Delivers the summary via: email OR Discord/Slack webhook (your choice, documented)
- [x] Configurable variables: GitHub repo, destination channel, language (EN/FR)
- [ ] Tested on a real n8n instance (include a screenshot of successful execution)  _(UNVERIFIED — real n8n execution screenshot required)_
- [x] README with setup instructions in 5 steps or fewer

## Test evidence
STATUS: n8n live execution screenshot is **UNVERIFIED** — do not claim ACCEPTANCE_COMPLETE until a real screenshot is attached.
Run the workflow manually in n8n after credentials are set.
Attach a screenshot of a successful execution to the PR description (operator environment).
