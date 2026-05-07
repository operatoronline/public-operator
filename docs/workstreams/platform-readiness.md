# Platform Readiness Workstream

## Goal

Define the shortest credible path to public release and separate launch blockers from nice-to-haves.

## Launch recommendation

Treat the public launch as a **local-first downloadable product**, not a hosted multi-tenant SaaS launch.

That is the faster and more credible path based on current product maturity.

## Core blockers

### Critical
1. Launch scope is still ambiguous, local-first product vs hosted multi-tenant platform.
2. Supportability and observability are too thin for public users.
3. Brand, domain, and distribution messaging are inconsistent.

### Important
4. Diagnostics and log export are not productized enough.
5. Public users need clearer runtime state and setup validation.

## Alpha, beta, GA gates

### Private alpha
- local install path works reliably
- gateway state is visible and understandable
- basic diagnostics are available
- product messaging is consistent

### Public beta
- onboarding is guided
- support/export diagnostics exist
- release packaging and docs are coherent
- beta scope is explicit and enforced

### GA
- release process is repeatable
- incident/support loop is mature
- product claims are validated and stable

## Two-week execution sequence

### Week 1
- freeze launch contract: local-first downloadable product
- align README, website, releases, and docs to that contract
- define diagnostics and support minimums

### Week 2
- add user-facing diagnostics export path
- improve runtime health visibility
- write public beta readiness checklist
- run install-to-first-success tests on clean environments

## Success metric

A public user can understand what Operator OS is, install it, diagnose basic failures, and use it without confusion about whether it is local software or hosted infrastructure.
