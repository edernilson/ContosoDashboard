<!--
Sync Impact Report
- Version change: template placeholders -> 1.0.0
- Modified principles: initial constitution created for ContosoDashboard
- Added sections: Security & Privacy Requirements, Development Workflow
- Removed sections: none
- Templates requiring updates: ✅ .specify/templates/plan-template.md, ✅ .specify/templates/spec-template.md, ✅ .specify/templates/tasks-template.md
- Follow-up TODOs: none
-->

# ContosoDashboard Constitution

## Core Principles

### I. Training-First Scope
Every change MUST preserve the educational purpose of ContosoDashboard. Features must be understandable in a local training environment, use the existing mock authentication and sample data model unless a feature explicitly requires a different approach, and avoid introducing complexity that obscures the lesson being taught.

### II. Offline-First Architecture
The application MUST remain runnable without external services or cloud dependencies. New features MUST work in a local or offline setup and use abstractions or seams for infrastructure access so cloud migration remains possible without rewriting business logic.

### III. Security-by-Design
All new or changed behavior MUST preserve user isolation, authorization boundaries, and protection against IDOR and other common access-control issues. Protected pages and services MUST continue to enforce the same authorization rules as the existing training implementation.

### IV. Testable and Demonstrable Behavior
Each change MUST be verifiable by a clear manual or automated scenario before it is considered complete. When business logic changes, the implementation MUST include a regression test or a documented verification step that proves the behavior end to end.

### V. Simplicity Over Rushed Feature Growth
Features MUST be implemented with the smallest change that delivers the learning goal. New abstractions, dependencies, or UI patterns are allowed only when they clearly improve maintainability or support the training scenario without adding unnecessary complexity.

## Security & Privacy Requirements
New or changed functionality MUST maintain explicit, reviewable access controls and keep user data isolated by authenticated identity. Features that introduce files, data writes, or notifications MUST avoid cross-user exposure and remain suitable for local classroom use.

## Development Workflow
All work on this repository MUST follow the existing Spec Kit workflow: capture requirements in a feature spec, create a plan with explicit verification steps, and document the user-facing behavior that the change introduces.

- Changes that affect security, access control, or offline behavior MUST be called out in the plan and reviewed before merge.
- Documentation and quickstart guidance MUST be updated when a feature changes how the app is run or exercised.
- The repository MUST remain suitable for local classroom use without requiring external accounts or services.

## Governance
This constitution supersedes ad hoc shortcuts for this repository. Amendments require a documented rationale, an updated version number, and a review of any impacted templates or guidance before they are accepted.

- Changes that materially alter security posture, offline-first guarantees, or the training scope MUST be treated as a major or minor amendment and reviewed before implementation.
- Any deviation from these principles MUST be documented with the reason, the affected scope, and the planned mitigation.
- Compliance is evaluated during spec, plan, and implementation review by checking that new work preserves the principles above.

**Version**: 1.0.0 | **Ratified**: 2026-07-10 | **Last Amended**: 2026-07-10
