# Automation: work across app ecosystems

## Purpose

Find an existing software solution that coordinates supported devices from
different vendors, reducing dependence on separate apps. Begin with requirements
and compatibility research; keep custom controller development a last resort.

## Capture the need

| Device or routine | Current app / exact model | Desired shared behavior               | Verified integration |
| ----------------- | ------------------------- | ------------------------------------- | -------------------- |
| Lighting          | User to supply            | Control a chosen group from one place | Unknown              |
| Daily routine     | User to describe          | Coordinate selected devices           | Unknown              |

Ask what must work locally, which devices already exist and what compromises are
acceptable. A shared dashboard, an automation engine and a device protocol solve
different jobs; choose based on the needed operations.

## Research existing software

[Home Assistant](https://www.home-assistant.io/) is a candidate to investigate,
not a selected dependency. Check its [integrations](https://www.home-assistant.io/integrations/)
against exact device models. Its [local-control guidance](https://www.home-assistant.io/faq/is-my-data-private/)
describes direct local communication where devices support it; some integrations
still depend on vendor services. Do not promise that every device can escape its
cloud ecosystem.

A deployed controller needs a running host; see [installation options](https://www.home-assistant.io/installation/).
Research and workspace planning remain useful without one. Account connections,
hosting and physical-control acceptance belong to a later implementation scope.

## Next

- [ ] Inventory two device models and one desired routine. Compare existing
      software/integrations, then propose the smallest useful trial with its gaps
      and host requirements. Write custom code only for a demonstrated missing capability.

## Use the session commands

Use these inside the agent; shared meanings live in the
[workflow reference](../../docs/workflow.md#session-requests).

- `context examples/automation`: establish the device models and desired routine.
- `discover examples/automation`: compare existing software and integrations.
- `check examples/automation`: verify compatibility claims against exact models
  and identify cloud dependencies or missing evidence.
- `advance examples/automation`: complete the selected research step; installation
  or device operation needs its own approved scope.
- `trim examples/automation`: propose consolidating notes or overlapping solutions.
- `status examples/automation`: report the recommendation and next useful step.

## Start here

> Read this project's AGENTS.md and README. Help me research how to coordinate
> my devices across vendor apps. Ask for exact models and the routine I want,
> then compare existing local-control options using current official evidence.
> Propose a small trial; do not install software, connect accounts or control devices.

**Useful result:** a compatibility-backed recommendation with a bounded next step.
Live device behavior remains unverified until a separately scoped trial succeeds.

**Learner checkpoint:** explain which part is the controller, which protocol a
device uses and whether the chosen routine depends on a cloud service. Point to
the evidence for one exact model and name what a later trial still needs to prove.
