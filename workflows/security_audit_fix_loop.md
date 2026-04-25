# Workflow: The Recursive Security Audit

This workflow uses Jules as a penetration tester to find vulnerabilities without making messy changes, then tracks and fixes them systematically.

## Stage 1: Discovery (The Audit)
Dispatch autonomous agents to scan specific modules and write findings to `security_findings/`.

**Command:**
```bash
cat jules_master_toolbox/prompts/security/<target>.md | jules new --repo <owner/repo>
```

## Stage 2: Retrieval
Pull the generated markdown reports from the completed Jules sessions.

**Command:**
```bash
jules remote pull --session <ID> --apply
```

## Stage 3: Tracking
Convert each `.md` file in `security_findings/` into a GitHub Issue.
*Tip: Ensure issues are tagged with `security` and `jules-fix` labels.*

## Stage 4: Remediation (The Fix)
Dispatch a fresh Jules agent to fix a specific issue.

**Command:**
```bash
gh issue list --label security --json title | jq -r '.[0].title' | jules new --repo <owner/repo>
```
