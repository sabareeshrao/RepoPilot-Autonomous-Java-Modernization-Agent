# RepoPilot Engineering Rules

## 1. Repository Language Guardrail

All content committed to this repository must be written in English.

This rule applies to:

- source code comments;
- documentation;
- task names and descriptions;
- commit messages;
- pull request titles and descriptions;
- issue titles and descriptions;
- architecture decision records;
- examples and sample data intended for repository use;
- configuration comments;
- test names and test documentation;
- generated project documentation that is committed to the repository.

Chat conversations may use mixed languages. Repository artifacts may not.

Before committing or pushing a batch, repository content must be reviewed for compliance with this rule.

## 2. GitHub Is the Durable Source of Truth

Conversation memory is not authoritative project state. Every new development session starts by reading the current GitHub repository.

## 3. Mandatory Session Preflight

Before implementing a new batch:

1. Verify repository access.
2. Verify the default branch.
3. Read the latest remote commit state.
4. Inspect the repository structure relevant to the next work.
5. Read `docs/roadmap/MASTER_ROADMAP.md`.
6. Read `docs/tracking/TASK_REGISTRY.md`.
7. Read `docs/tracking/PROGRESS.md`.
8. Read `docs/tracking/BATCH_HISTORY.md`.
9. Read dynamic, bug, and hardening task trackers.
10. Identify the latest completed task.
11. Check unresolved blockers and dependency changes.
12. Select only dependency-ready work for the next batch.

## 4. Batch Lifecycle

Each build batch follows this lifecycle:

1. Remote preflight.
2. Task selection.
3. Implementation.
4. Verification.
5. User review when requested.
6. Remote state recheck before push.
7. Reconciliation if remote state changed.
8. Commit and push.
9. Remote verification.
10. Tracking update.

## 5. Stale-State Protection

A batch must not blindly push if the remote branch changed after the batch began.

If the remote state changed:

1. inspect the new commits;
2. determine whether the batch conflicts with them;
3. reconcile the implementation;
4. rerun verification;
5. push only after the batch is based on the current remote state.

## 6. Task Integrity

- Baseline task IDs are immutable.
- Dynamic work receives a dynamic task ID.
- Bugs receive a bug task ID.
- Hardening work receives a hardening task ID.
- Task history is not rewritten to create an artificial clean history.

## 7. Repository Structure

The initial governance structure is:

```text
README.md
docs/
  roadmap/
    MASTER_ROADMAP.md
  tracking/
    TASK_REGISTRY.md
    PROGRESS.md
    BATCH_HISTORY.md
    DYNAMIC_TASKS.md
    BUG_TASKS.md
    HARDENING_TASKS.md
  architecture/
    ENGINEERING_RULES.md
```

Future application modules are introduced only when their baseline tasks require them.

## 8. Verification Before Completion

A mini-task is complete only when its acceptance criteria are satisfied. A batch is complete only when its included mini-tasks are complete and the committed remote state is verified.
