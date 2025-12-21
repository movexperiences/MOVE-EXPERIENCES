# MOVE — Engineering Organization

MOVE is a technology company building a marketplace platform backed by proprietary product and data infrastructure.

## What we build

**Product surfaces**
- **Web**: onboarding, search, and user-facing flows
- **Mobile**: mobile-first experience and core user journeys
- **API**: domain services, authentication, and transaction orchestration
- **Ops/Admin**: internal tools for operations, quality, and support
- **Data**: telemetry, analytics, and experimentation foundations

**Core platform capabilities**
- Identity & access
- Catalog & discovery
- Transaction workflows
- Risk & trust primitives (policy-driven)
- Observability and event telemetry

## Architecture (high level)

- Service-oriented backend with clear domain boundaries
- Shared UI and design primitives across product surfaces
- Event-driven telemetry to support measurement and iteration
- Infrastructure designed for reproducible environments and auditability

## Technology stack (reference)

- **Frontend**: Next.js + TypeScript
- **Mobile**: React Native
- **Backend**: NestJS and/or FastAPI (service layer)
- **Data**: PostgreSQL (primary), optional caching/queues per domain needs
- **Infra**: containerized workloads + CI/CD via GitHub Actions
- **Observability**: error tracking + metrics/tracing (OpenTelemetry-compatible)

> Notes:
> - Not all repositories are public.
> - Stack may vary by product domain or lifecycle stage.

## Repositories

| Repository | Purpose | Visibility |
|---|---|---|
| `move-web` | Web application | Public/Private |
| `move-app` | Mobile application | Private |
| `move-api` | Core backend services | Private |
| `move-admin` | Internal tools (ops/support) | Private |
| `move-data` | Data pipelines / analytics tooling | Private |
| `move-docs` | Technical documentation and standards | Public/Private |

## Engineering standards

**Source control**
- Trunk-based or short-lived branches with mandatory PR reviews
- Small PRs, explicit context, and reversible changes

**Commit convention**
- Conventional Commits for structured history and automation compatibility :contentReference[oaicite:1]{index=1}

**Quality**
- Automated checks in CI (lint, tests, type checks where applicable)
- Clear ownership boundaries per domain

## Governance & security

- **CODEOWNERS** defines responsibility by area/module :contentReference[oaicite:2]{index=2}
- Least-privilege access via GitHub Teams and protected branches
- Secrets managed via GitHub Environments/Secrets (no secrets in code)
- Dependency supply-chain hygiene with **Dependabot security updates** :contentReference[oaicite:3]{index=3}

## Contributing

If a repository is public:
1. Open an issue with context and expected behavior
2. Submit a PR with:
   - scope and rationale
   - test/validation notes
   - rollback considerations (when relevant)

For private repositories, contribution follows internal access controls and ownership policies.

## Contact

- Engineering: `engineering@move.<tld>`
- Security: `security@move.<tld>`
- Organization: GitHub Discussions / Issues (when enabled)

---

<!--
Organization profile README location:
.github/profile/README.md
Reference: GitHub documentation/changelog on organization profile READMEs.
-->
