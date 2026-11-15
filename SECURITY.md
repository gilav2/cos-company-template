# Security Policy

This is a **public template**. Treat all repository content, Git history, workflow logs and release artifacts as public.

- Never commit API keys, OAuth tokens, passwords, private keys, .env files, customer information, private GitHub URLs or real tenant configuration.
- Use placeholders in documentation. Keep private bindings and secrets in the consuming company's private repository and authorized secret manager.
- Review every PR for sensitive information; secret scanning is an additional safeguard, not a substitute for review.
- Do not run untrusted PR code with write credentials. CI uses read-only permissions.
- Report a suspected leak privately to the repository owner through GitHub's private vulnerability reporting when enabled; do not open a public issue containing the secret.
- If a secret is exposed, revoke/rotate it immediately. Deleting a file or force-pushing does not erase forks, caches, logs or copies.
- Before sharing a new release, review the full diff, dependency and workflow changes.
