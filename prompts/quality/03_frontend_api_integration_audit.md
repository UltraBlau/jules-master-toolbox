# Jules Objective: Frontend Component & API Integration Audit

You are a senior frontend engineer acting autonomously. Your goal is to identify and resolve exactly 1 or 2 UI bugs, state management edge cases, or unhandled API errors within the React application.

**Scope Restriction:**
Limit your investigation to the following files and directories:
- `frontend/src/pages/`
- `frontend/src/components/`
- `frontend/src/hooks/` (if any API data fetching hooks exist)
- Ignore backend Python files unless absolutely necessary to align an API contract.

**Your Workflow (Do not ask for further instructions):**
1. **Analyze:** Read the React components in your scope to identify a potential issue. Look for missing error boundaries, unhandled Promise rejections in `fetch` or `axios` calls, missing dependency arrays in `useEffect`, or scenarios where the UI could crash if the backend returns unexpected data (e.g., null instead of an array).
2. **Reproduce:** Since frontend unit tests might not be fully configured, write a clear, reproducible scenario description in the code comments or add a React Testing Library test if the framework supports it. Alternatively, add defensive console warnings to trap the bug during local development.
3. **Fix:** Implement the minimal, most robust fix in the React code. Add proper loading states, error fallbacks, or optional chaining (`?.`) where data is assumed.
4. **Verify:** Run the frontend build process (e.g., `npm run build` or `npm run lint`) inside the `frontend/` directory to ensure your React code compiles without syntax errors or linting warnings.
5. **Finalize:** Ensure your changes are clean, idiomatic, and contain no "debugging" artifacts. Provide a concise summary of what you fixed.

**Constraints:**
- Fix a maximum of 2 issues. Once 2 are fixed and verified, stop.
- Do not rewrite components to use different libraries. Stick to the established React and Tailwind CSS patterns.
- Ensure the frontend builds successfully before completing the task.
