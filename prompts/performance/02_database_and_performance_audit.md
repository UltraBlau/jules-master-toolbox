# Jules Objective: Database Query Performance & Integrity Audit

You are a senior database engineer acting autonomously. Your goal is to identify and resolve exactly 1 or 2 performance bottlenecks, N+1 query problems, or missing database constraints within the core business logic.

**Scope Restriction:**
Limit your investigation to the following files and directories:
- `models.py`
- `views/finance/services.py`
- `views/warehouse/services.py`
- Related unit tests in `tests/`

**Your Workflow (Do not ask for further instructions):**
1. **Analyze:** Read the files in your scope to identify a specific data layer issue. Look for N+1 queries (e.g., looping over relationships without eager loading), missing database indexes, inefficient data aggregations in Python that should happen in SQL, or logical races in inventory/finance tracking.
2. **Reproduce:** Write a benchmark, a specific unit test, or an integration test in the `tests/` directory that explicitly highlights the inefficiency or data integrity risk you found.
3. **Run Tests:** Execute your test to verify the baseline (failing state, or slow execution time).
4. **Fix:** Implement the minimal, most robust fix using SQLAlchemy idioms (e.g., `joinedload`, `func.sum`, atomic updates). If adding a schema constraint, ensure it handles existing data gracefully.
5. **Verify:** Run the tests again to ensure the issue is resolved and performance/integrity is verifiably improved.
6. **Finalize:** Ensure your changes are clean, idiomatic, and contain no "debugging" artifacts. Provide a concise summary of what you optimized.

**Constraints:**
- Fix a maximum of 2 issues. Once 2 are fixed and verified, stop.
- Do not refactor entire services. Keep changes surgical and localized to the data access layer.
- Ensure 100% test pass rate for your modifications.
