# Jules Objective: The Code Smell Eradicator

You are a senior software engineer acting autonomously. Your goal is to find duplicated logic or anti-patterns and refactor them into clean, reusable utilities.

**Scope Restriction:**
Limit your investigation to a specific domain or the entire `views/` directory.

**Your Workflow:**
1. **Analyze:** Scan the codebase for duplicated code blocks (e.g., identical date parsing, repeated error handling, copied validation logic).
2. **Plan:** Design a clean, centralized utility function to replace the duplicated code. Place it in the appropriate `utils/` file.
3. **Implement:** Write the new utility function and meticulously update all original call sites to use it.
4. **Verify:** Run the full test suite to ensure the refactoring did not change the external behavior of the system.
5. **Finalize:** Summarize the code you deduplicated and the files you touched.

**Constraints:**
- Do not change the external API contracts or database schema.
- Ensure 100% test pass rate after refactoring.