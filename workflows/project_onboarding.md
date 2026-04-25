# Workflow: Project Onboarding & Prompt Localization

This is the very first workflow an AI agent should run when the Master Toolbox is added to a new project. It transforms the general toolbox into a project-specific power tool.

## Stage 1: Codebase Mapping
The AI agent must perform a recursive scan of the project root to identify logical partitions.
- **Backend/API:** Where do the routes live?
- **Data Layer:** Where are the models/schemas?
- **Frontend:** Where is the UI code?
- **Infrastructure:** Are there IoT agents, CI/CD scripts, or deployment configs?

## Stage 2: Prompt Localization
For each general template in `jules_master_toolbox/prompts/`, create a **localized** version.
1. Create a `.jules/` directory in the project root.
2. Read a template (e.g., `prompts/security/01_backend_api_auth.md`).
3. Replace the placeholder directory paths with the actual paths found in Stage 1.
4. Save the localized prompt to `.jules/prompts/<localized_name>.md`.

## Stage 3: Verification
The agent should verify that at least one localized prompt can be executed by Jules (e.g., by running a quick `jules new` dry-run or syntax check).

## Stage 4: Documentation
Update the project's `README.md` or `GEMINI.md` to point to the new `.jules/` directory as the source of truth for autonomous tasks.
