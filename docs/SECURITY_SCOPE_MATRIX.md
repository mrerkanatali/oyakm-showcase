# Security and Scope Matrix (Showcase Repo)

This document defines what can and cannot be published in the showcase repository.

## 1) Publishable content

- High-level architecture diagrams.
- Capability descriptions for Flutter, API, backend, and admin areas.
- Generic data-flow explanations without schema-level details.
- Sanitized screenshots with no personal data, secrets, or internal hostnames.
- Commercial and white-label process documents.

## 2) Never publish

- Application source code (mobile, API, admin, worker, bridge).
- Real formulas, algorithm details, or implementation-level pseudo code.
- Endpoint-level internals (full route maps, request validators, auth internals).
- Database schema dumps, migrations, table/column-level structure.
- CI/CD internals, infrastructure state files, deployment secrets.
- Credentials: API keys, tokens, Firebase service accounts, keystores, passwords.
- Any customer or production data.

## 3) Allowed representation level

| Area | Allowed in showcase | Not allowed in showcase |
|------|----------------------|-------------------------|
| Flutter | Module map, UX capabilities, platform coverage | Widget trees, business logic, state code |
| API | Role in system, integration capabilities, security posture summary | Real endpoints, payload contracts, auth implementation |
| Backend | Operational capabilities, workflow summary | Worker code, queue logic details, cron internals |
| Admin | Feature groups and usage scenarios | Panel code, form validation logic, privileged flows |
| Calculators | Category-level descriptions and disclaimers | Formula details, constants, edge-case logic |

## 4) Security gate before every showcase update

1. Confirm no code files are included.
2. Confirm no secret-bearing files are included.
3. Confirm screenshots are anonymized.
4. Confirm docs avoid implementation depth.
5. Confirm no references to private URLs or credentials.

## 5) Guiding rule

Show what the platform can do, not how it is built internally.
