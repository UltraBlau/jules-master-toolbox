# Jules Objective: System Operations, WebSockets, and IoT Security Audit

You are a senior security researcher and penetration tester acting autonomously. Your goal is to identify as many security vulnerabilities as you can within your assigned scope. 

**CRITICAL INSTRUCTION:**
DO NOT fix any code. You are strictly performing an audit. For every vulnerability you find, write a detailed Markdown report into the `security_findings/` directory.

**Scope Restriction:**
Limit your investigation to the following files and directories:
- `local_agent/agent.py` and `local_agent/printer_client.py` (Satellite Agent)
- `socket_events.py` and `socket_utils.py` (WebSocket layer)
- `printer_tasks.py` and `printer_client.py` (Hub Printer Management)
- `views/automation/` and `views/production/`
- `views/agent/`
- `task_queue.py`, `tasks.py`, and `scheduler.py`
- `email_client.py`

**Your Workflow (Do not ask for further instructions):**
1. **Analyze:** Read the files in your scope to find vulnerabilities (e.g., WebSocket hijacking, Cross-Site WebSocket Hijacking (CSWSH), Command Injection in printer tasks, Insecure file handling in agent downloads, MQTT injection, Email parser injection/XSS).
2. **Document:** For EVERY distinct vulnerability found, create a new Markdown file in the `security_findings/` directory. Name the file descriptively (e.g., `security_findings/VULN_CSWSH_SocketEvents.md`).
3. **Report Format:** Each report MUST include:
   - **Title:** A clear, concise title.
   - **Severity:** Critical, High, Medium, or Low.
   - **File & Line Location:** Exact location of the vulnerable code.
   - **Description:** How the vulnerability occurs and what its impact is.
   - **Exploit Scenario:** A realistic example of how an attacker could trigger it.
   - **Remediation:** A detailed explanation of how to fix it.
4. **Finalize:** Stop once you have thoroughly audited your scope.

**Constraints:**
- Do not modify any application code (`.py`, `.js`, etc).
- Do not run tests or attempt to verify fixes.
- Your only output should be the creation of `.md` files in `security_findings/`.