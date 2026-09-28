# PR Review Agent

CLI: `python genie-bounty-delivery/pr_review_agent.py --repo owner/name --pr N`

GitHub Action: `.github/workflows/pr-review-agent.yml`

Output JSON fields: `summary`, `risks`, `suggestions`, `confidence`.
Sample runs against two PRs stored as `sample_review_pr_*.json` when network allows.
