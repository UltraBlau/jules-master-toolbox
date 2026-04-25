# Jules Objective: Production Queue & Automation Logic Audit

You are a senior systems engineer acting autonomously. Your goal is to identify and resolve exactly 1 or 2 bugs, state-machine inconsistencies, or logic gaps in the print queue and job assignment systems.

**Scope Restriction:**
Limit your investigation to the following files:
- `views/automation/services.py`
- `views/production/routes.py`
- `printer_tasks.py`
- `printer_client.py`
- Related unit tests in `tests/` (e.g., `tests/test_production_edge_cases.py`)

**Your Workflow (Do not ask for further instructions):**
1. **Analyze:** Read the files in your scope to find a logic flaw. Look for race conditions in status updates (e.g., `PENDING` to `PRINTING`), incorrect priority sorting in job assignment, or unhandled printer error states that leave jobs "stuck."
2. **Reproduce:** Write a failing test in the `tests/` directory that explicitly simulates the race condition or logic failure you identified.
3. **Run Tests:** Execute `pytest` to confirm the test fails.
4. **Fix:** Implement a surgical fix in the application logic. Ensure state transitions are atomic or properly guarded.
5. **Verify:** Run the tests again to ensure the issue is resolved and all production tests pass.
6. **Finalize:** Provide a concise summary of the logic improvement you implemented.

**Constraints:**
- Fix a maximum of 2 issues.
- Do not add new features or external dependencies.
- Maintain existing session and database patterns.
