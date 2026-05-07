# Product and Onboarding Workstream

## Goal

Make Operator OS usable by a new public-beta user without manual intervention.

## Public beta user promise

A user can download Operator OS, complete setup, start the gateway, and have a first successful chat in one guided flow.

## Core problem

Right now first-run setup is fragmented across:
- password setup
- model selection
- credentials
- channels
- gateway state

The product needs one clear activation path, not a set of adjacent setup surfaces.

## Ideal first-run journey

1. Install and launch Operator OS.
2. Set local admin password.
3. Choose a default model/provider.
4. Add required credentials.
5. Validate gateway readiness.
6. Start gateway.
7. Send first successful built-in chat message.
8. See next suggested action, like connect a channel, enable memory, or try a tool.

## Activation milestones

- app opened
- password configured
- default model configured
- credentials valid
- gateway running
- first chat sent
- first successful response returned
- first follow-up action completed

## Blockers

### Critical
1. No unified first-run setup funnel.
2. Gateway prerequisites are not translated into a guided checklist.
3. No activation instrumentation to measure drop-off.

### Important
4. Setup errors need inline remediation, not raw diagnostics.
5. Beta scope is too broad unless the first success path is defined tightly.

## Two-week execution sequence

### Week 1
- define the single public-beta first-run journey
- implement launcher checklist for setup prerequisites
- add inline validation for models, credentials, and gateway blockers
- define activation events and logging

### Week 2
- implement first-success confirmation state
- add next-step suggestions after first chat
- test onboarding with clean installs
- document top 10 onboarding failure states and resolutions

## Deliverables

- guided first-run checklist in launcher
- first-success funnel instrumentation
- onboarding failure-state copy
- public-beta activation dashboard definition

## Success metric

A new user can get from install to first successful response in under 10 minutes without operator help.
