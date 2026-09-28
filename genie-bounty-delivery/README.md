# PR Review Agent

CLI: `python genie-bounty-delivery/pr_review_agent.py --repo owner/name --pr N`
Alias shape: `claude-review --pr https://github.com/owner/repo/pull/123` → extract repo/PR and call the CLI.

GitHub Action: copy `pr-review-agent.workflow.yml` to `.github/workflows/pr-review-agent.yml`.

Output JSON fields: `summary`, `risks`, `suggestions`, `confidence` (map Low/Medium/High from score).
Sample runs against two PRs stored as `sample_review_pr_*.json` when network allows.
