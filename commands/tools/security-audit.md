Security audit for: $ARGUMENTS

Analyze the code for security vulnerabilities:

## 1. Input Validation
- [ ] All user inputs validated
- [ ] Input length limits enforced
- [ ] Type checking on inputs
- [ ] Sanitization of special characters

## 2. Injection Attacks
- [ ] SQL injection (parameterized queries)
- [ ] Command injection (no shell with user input)
- [ ] XSS (output encoding)
- [ ] Path traversal (validate file paths)

## 3. Authentication & Authorization
- [ ] Proper authentication checks
- [ ] Authorization on all protected routes
- [ ] Session management secure
- [ ] Password handling (hashing, no plaintext)

## 4. Data Protection
- [ ] Sensitive data encrypted
- [ ] No secrets in code/logs
- [ ] Proper error messages (no stack traces to users)
- [ ] PII handling compliant

## 5. Dependencies
- [ ] Check for known vulnerabilities: `npm audit`
- [ ] Dependencies up to date
- [ ] No unnecessary dependencies

## Output Format
For each finding:
- Severity: CRITICAL / HIGH / MEDIUM / LOW
- Location: file and line
- Description: what's the vulnerability
- Impact: what could an attacker do
- Remediation: how to fix it
