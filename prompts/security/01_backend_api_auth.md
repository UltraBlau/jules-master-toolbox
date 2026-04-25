# Jules Objective: Backend, API, and Authentication Security Audit

You are a senior security researcher and penetration tester acting autonomously. Your goal is to identify as many security vulnerabilities as you can within your assigned scope. 

**CRITICAL INSTRUCTION:**
DO NOT fix any code. You are strictly performing an audit. For every vulnerability you find, write a detailed Markdown report into the `security_findings/` directory.

**Scope Restriction:**
Limit your investigation to the following files and directories:
- `app.py` and `factory.py`
- `config.py` and `utils/settings.py`
- `utils/auth.py` and `auth_utils.py`
- `utils/security.py`
- `views/api/` (all API routes)
- `views/settings/` (configuration endpoints)
- `views/debug/` (debug endpoints)

**Your Workflow (Do not ask for further instructions):**
1. **Analyze:** Read the files in your scope to find vulnerabilities (e.g., Auth Bypass, IDOR, SQL Injection, Path Traversal, Hardcoded Secrets, SSRF, XSS in JSON responses, Rate Limiting flaws).
2. **Document:** For EVERY distinct vulnerability found, create a new Markdown file in the `security_findings/` directory. Name the file descriptively (e.g., `security_findings/VULN_IDOR_API_Settings.md`).
3. **Report Format:** Each report MUST include:
   - **Title:** A clear, concise title.
   - **Severity:** Critical, High, Medium, or Low.
   - **File & Line Location:** Exact location of the vulnerable code.
   - **Description:** How the vulnerability occurs and what its impact is.
   - **Exploit Scenario:** A realistic example of how an attacker could trigger it (e.g., a curl command or malicious payload).
   - **Remediation:** A detailed explanation of how to fix it.
4. **Finalize:** Stop once you have thoroughly audited your scope.

**Constraints:**
- Do not modify any application code (`.py`, `.js`, etc).
- Do not run tests or attempt to verify fixes.
- Your only output should be the creation of `.md` files in `security_findings/`.