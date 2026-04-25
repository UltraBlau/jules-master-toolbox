# Jules Master Toolbox: AI Agent Entry Point

This directory contains a portable set of workflows and prompts designed to make any repository "Jules-Native." 

**Instruction for AI Agents:**
When starting work in this repository, read this file completely. Use the defined `jules` CLI patterns and follow the structured workflows in `/workflows` for all autonomous tasks.

## 🚀 Quick Start: Jules CLI Reference
Use the following command patterns for all Jules interactions:
- `jules new "<task>"`: Create session in current repo.
- `jules new --repo <owner/repo> "<task>"`: Target specific repo.
- `jules new --parallel <1-5> "<task>"`: Multi-agent concurrent exploration.
- `cat <file> | jules new`: Pipe complex prompt/spec directly to agent.
- `jules remote list --session`: List active/stale sessions.
- `jules remote pull --session <id> --apply`: Fetch + atomic local patch application.

## 📂 Workflow Directory
Follow these step-by-step guides for specific engineering goals:
0. **Onboarding:** `workflows/project_onboarding.md` (Run this first in a new project!)
1. **Security:** `workflows/security_audit_fix_loop.md` (Audit -> Issue -> Fix)
2. **Quality:** `workflows/continuous_quality_improvement.md` (Coverage Hunter)
3. **Performance:** `workflows/performance_optimization.md` (Profiling -> Benchmarking -> Fix)
4. **New Feature (TDD):** `workflows/feature_flow_1_tdd_scaffolding.md`
5. **New Feature (Parallel):** `workflows/feature_flow_2_parallel_implementation.md`
6. **New Feature (Hardening):** `workflows/feature_flow_3_review_and_polish.md`

## 🎭 Agent Prompt Library
Scoped Markdown files for autonomous roles are located in `/prompts`:
- **Security:** `prompts/security/` (Backend, Core, IoT, Frontend)
- **Quality:** `prompts/quality/` (UX, Code Smells, Flaky Tests, Coverage)
- **Performance:** `prompts/performance/` (DB optimization, Dependency Upgrades)

## ⚖️ Core Mandates
1. **Scope Restriction:** Always limit agents to specific directories to prevent context overflow.
2. **Double-Verification:** Use one agent to find/document problems and another to implement fixes.
3. **Traceability:** Everything must be logged via GitHub Issues or PRs.

---
*Created by Gemini CLI & @UltraBlau to standardize the AI-Native Developer experience.*
