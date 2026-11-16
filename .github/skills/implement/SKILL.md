---
name: implement
description: 'Implement a human-approved task plan, committing each task separately, then run a code-review agent and address actionable findings. Use /implement only after the user approves the plan.'
argument-hint: 'Approved task IDs or task-plan path'
user-invocable: true
---

# Implement Approved Tasks

Implement only the user-approved tasks, in dependency order. Use the `task-implementer` agent for each task and `code-reviewer` for the resulting changes.

## Preflight

1. Confirm explicit user approval of the task plan.
2. Read the tasks, linked requirements/designs, repository instructions, and current branch/worktree status.
3. Identify the exact task scope and baseline commit.
4. Do not overwrite or include unrelated user changes. If uncommitted changes conflict with the task, stop and ask; if unrelated, preserve them and ensure they are excluded from commits.
5. If required scaffolding or decisions are missing, report the blocker instead of inventing project conventions.

## Execution

1. For each approved task, invoke `task-implementer` with only that task and its required context.
2. Require the agent to make and validate the task's changes, then create one commit containing only that task's files. Commit message must include the task ID and use the repository's required Copilot co-author trailer.
3. Verify the commit succeeded and inspect its file list before proceeding to the next task. Never stage or commit unrelated changes.
4. After all task commits, invoke `code-reviewer` on the implementation diff from the recorded baseline. The reviewer is read-only and must report actionable findings with file, line, severity, and rationale.
5. If actionable findings exist, use `task-implementer` to fix them in a separate, narrowly scoped commit, then run `code-reviewer` again. Repeat at most two fix/review rounds; if issues remain, stop and report them rather than looping indefinitely.
6. Run targeted validation for changed behavior where possible. Do not claim a check passed unless it ran successfully.

## Boundaries

- Do not proceed to `/test` automatically; testing is the next user-invoked phase.
- Do not amend commits or rewrite history.
- Do not commit generated secrets, real personal/health data, unrelated files, or test artifacts that are not part of approved tasks.
- If an agent cannot safely isolate its task commit from other work, stop and ask the user.

## Output

Report task commits, changed files, validation results, review findings/fixes, and any remaining blockers. Leave the next action to the user.
