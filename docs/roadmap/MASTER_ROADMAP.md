# RepoPilot Master Roadmap

## Baseline

RepoPilot starts with a locked baseline of 2,315 mini-tasks across 100 major phases.

| Workstream | Phases | Baseline Mini-Tasks |
|---|---:|---:|
| Java and Repository Foundation | 1-9 | 210 |
| LLM and Core Agent Engineering | 10-22 | 330 |
| RAG, Memory, Context, and MCP | 23-35 | 310 |
| Safety, Sandbox, and Production Backend | 36-51 | 360 |
| Testing and Agent Evaluation | 52-62 | 240 |
| Observability, Security, GitHub, and CI/CD | 63-75 | 285 |
| Multi-Agent, Reliability, and Cost Engineering | 76-89 | 300 |
| UI, Java Modernization, GIS, and Production Capstone | 90-100 | 280 |
| **Total** | **100** | **2,315** |

## Task ID Classes

- `RP-xxxx`: locked baseline mini-task.
- `RPD-xxxx`: dynamically discovered implementation mini-task.
- `RPB-xxxx`: bug-fix mini-task discovered during implementation or verification.
- `RPH-xxxx`: hardening, security, resilience, or performance mini-task.

## Locked Rules

1. Existing task IDs are immutable after assignment.
2. Completed task history is never rewritten to hide prior work.
3. Baseline tasks are never silently deleted or merged into oversized tasks.
4. Dynamic work is added using the appropriate dynamic task class.
5. Architecture changes are recorded rather than silently replacing prior decisions.
6. Git history is the authoritative record of committed implementation progress.

## Dynamic Execution Rules

The baseline is locked, but execution is allowed to adapt.

Execution order may change when:

- a dependency must be completed earlier;
- a blocker is discovered;
- a bug must be fixed before continuing;
- a security or hardening requirement becomes necessary;
- integration work exposes missing implementation tasks.

A changed execution order does not renumber existing tasks.

## Mini-Task Definition

A mini-task must be a small, independently understandable engineering unit that can be implemented, verified, and tracked without hiding several unrelated changes inside one task.

Examples of suitable mini-tasks:

- Create the Maven execution result model.
- Capture process exit codes.
- Add timeout handling to Maven execution.
- Parse a Java class declaration.
- Add repository-scoped vector search.

Examples that are too large:

- Implement RAG.
- Build the agent.
- Add GitHub integration.

## Baseline Status

- Baseline mini-tasks: 2,315
- Baseline roadmap version: 1.0
- Current build batch: `BATCH-0001`
