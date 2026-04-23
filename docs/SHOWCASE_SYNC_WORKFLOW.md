# Main Repo -> Showcase Repo Sync Workflow

This workflow keeps public showcase docs up to date without leaking code or secrets.

## Repositories

- Private development repo: `oyakm` (real codebase).
- Public showcase repo: `oyakm-showcase` (docs and sanitized assets only).

## Operating model

1. Build features in private repo as normal.
2. For each meaningful release/change, extract only:
   - Capability-level updates,
   - Architecture-level changes,
   - White-label process notes,
   - Sanitized screenshots if needed.
3. Apply these updates in the showcase repo documentation.
4. Run the security gate checklist from `SECURITY_SCOPE_MATRIX.md`.
5. Commit and push only sanitized docs/assets.

## What to copy vs not copy

- Copy: Markdown docs, Mermaid diagrams, sanitized screenshots.
- Do not copy: source files, config files, secret files, migrations, deployment scripts.

## Suggested showcase `.gitignore`

Use a strict deny-list for common leak paths:

```gitignore
# Secrets and environment files
.env
.env.*
*.pem
*.key
*.p12
*.jks
*.keystore
google-services.json
GoogleService-Info.plist

# Build and temporary files
node_modules/
build/
dist/
.DS_Store
```

## Update cadence

- Minimum: after each production-relevant capability release.
- Preferred: weekly update window.
- Acceptable: bi-weekly if no major capability change occurred.
- Commit format standard: `docs(showcase): <short update summary>`.

## Ownership

- Product/tech owner approves capability wording.
- Security gate is mandatory before every public push.
- Legal/commercial texts are published only after counsel review where required.
