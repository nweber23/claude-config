# Security Guidelines

## Existing vulnerabilities found outside the current task

- Do not fix it inline — stay scoped to what was requested.
- Instead, record it in `SECURITY_REVIEW.md` at the project root (create it if it doesn't exist). Each entry should include: location (file:line), description, severity/impact, and a suggested remediation.
- Do not modify the vulnerable code until the user explicitly approves the fix.

## Dependencies

- Always ask before adding a new third-party dependency, regardless of how well-known the package is.
- State why it's needed and whether an existing dependency or the standard library could do the job instead.

## General practices

- Never hardcode secrets, API keys, or credentials — flag them if found in code or commit history.
- Watch for standard vulnerability classes (injection, XSS, auth/access-control gaps, insecure deserialization) when writing or reviewing code, per OWASP Top 10.
