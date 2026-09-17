# RepoPilot: Autonomous Java Modernization Agent

RepoPilot is an Agentic AI engineering system for understanding, modernizing, validating, and safely changing Java and Spring Boot repositories.

## Mission

RepoPilot will progressively learn to:

1. Inspect Java and Spring Boot repositories.
2. Understand project structure, dependencies, source code, tests, and configuration.
3. Build modernization plans from developer goals.
4. Apply deterministic transformations where possible.
5. Use LLM reasoning for ambiguous engineering decisions.
6. Compile and test every meaningful code change.
7. Diagnose failures and perform controlled repair attempts.
8. Review generated changes for correctness, scope, risk, and security.
9. Require human approval for high-impact operations.
10. Produce Git-ready, reviewable changes and pull requests.

## Roadmap Model

- Baseline roadmap: 2,315 mini-tasks.
- Baseline task IDs: `RP-xxxx`.
- Dynamically discovered work: `RPD-xxxx`.
- Bug-fix work: `RPB-xxxx`.
- Hardening, security, and performance work: `RPH-xxxx`.
- Existing task IDs are immutable after they are assigned.
- Execution order may change when dependencies or newly discovered work require it.

## Repository Language Policy

All content committed to this repository must be written in English. This includes source code comments, documentation, task descriptions, commit messages, pull request text, issue text, examples, configuration comments, and architecture records.

Conversation outside the repository may use other languages, but repository artifacts remain English-only.

## Source of Truth

The GitHub repository is the durable source of truth for project state. Every new development session must inspect the latest remote state and project tracking files before continuing work.

## Current Build State

- Current batch: `BATCH-0001`
- Baseline tasks in this batch: `RP-0001` through `RP-0005`
- Project stage: governance and engineering foundation
