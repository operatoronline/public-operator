# Services and Architecture Workstream

## Goal

Decide what level of managed-services maturity is required for public release and sequence the rest.

## Launch recommendation

Public launch should not depend on fully productized managed browser, repo, and sandbox services.

The public release can ship as a local-first Operator OS product first, while managed services remain selectively enabled and explicitly beta-scoped.

## Core blockers

### Critical
1. There is no canonical release baseline across planning docs yet.
2. Browser is not yet a first-class managed service.
3. Repo writes are not safely productized, there is no managed credential broker or PR lifecycle.

### Important
4. Shared control-plane primitives need to exist before services can feel cohesive.
5. Service capability exposure needs clearer gating and defaults.

## Required architecture move

Build the shared managed-service control plane contract first:
- capability registry
- short-lived service auth
- service lifecycle model
- policy boundary between kernel and services

Browser, sandbox, and repo all depend on that layer.

## Alpha, beta, GA framing

### Private alpha
- browser/sandbox/repo can remain partial and operator-assisted
- managed services are experimental

### Public beta
- service availability is explicit
- auth and capability boundaries are defined
- unsafe repo-write paths stay disabled by default

### GA
- service lifecycle and auth are productized
- managed services have stable guarantees and fallback behavior

## Two-week execution sequence

### Week 1
- define control-plane contract
- write capability registry spec
- define short-lived auth model
- classify service actions by safety level

### Week 2
- define rollout sequence for browser, sandbox, and repo
- specify fallback behavior when services are unavailable
- document which service features are beta-only vs launch-ready

## Success metric

Operator OS can publicly explain what managed services are available, how they authenticate, what is safely enabled, and what remains beta-scoped.
