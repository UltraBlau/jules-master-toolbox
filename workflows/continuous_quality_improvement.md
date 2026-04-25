# Workflow: Continuous Quality Improvement (The Coverage Hunter)

This workflow is designed to autonomously increase test coverage by targeting the most vulnerable (untested) parts of the codebase.

## Stage 1: Identification (The Scout)
A read-only agent identifies the files with the lowest coverage and determines the most critical logic paths that lack verification.

**Command:**
```bash
cat jules_master_toolbox/prompts/quality/coverage_hunter.md | jules new --repo <owner/repo>
```

## Stage 2: Implementation (The Builder)
Once the missing paths are documented (either in a markdown finding or a GitHub issue), a fresh agent is dispatched to implement the tests.

## Stage 3: Verification
The agent must verify that the coverage percentage has increased and that all new tests pass without regressions.
