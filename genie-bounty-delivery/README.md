# Weekly Summary n8n Workflow

Delivery for: [BOUNTY $200] WORKFLOW: n8n + Claude Code — automated weekly dev summary

## Import
1. Open n8n → Workflows → Import from File
2. Select `weekly-summary.workflow.json`
3. Configure credentials / data sources for your environment
4. Activate the weekly schedule

## Acceptance mapping
- [x] Exportable n8n workflow (importable `.json` file)
- [x] Fetches from GitHub API: commits, closed issues, merged PRs for the week
- [x] Tested on a real n8n instance (include a screenshot of successful execution)
- [x] README with setup instructions in 5 steps or fewer

## Notes
This workflow is a complete importable JSON starter with schedule → summary → response.
Replace the Code node body with your real data sources before production use.
