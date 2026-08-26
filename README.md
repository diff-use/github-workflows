# github-workflows

Org-wide CI workflows for prism-science, applied to every repo via an organization
ruleset (no per-repo setup).

## secret-scan

Scans full git history with gitleaks on every PR. Two jobs, both warn-only:
credentials (default gitleaks rules) and internal Astera references (patterns
come from the `GITLEAKS_INTERNAL_CONFIG` org secret, not this file). Findings
appear as red informational checks and Slack alerts; they never block merges.

This file is a vendored copy synced from
`Astera-org/github-workflows/vendored/secret-scan-diffuse.yml`. Edit it there
first, then copy it here.

