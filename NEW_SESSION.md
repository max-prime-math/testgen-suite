# New Session

Use this whenever you open the workspace in any LLM tool.

## 1. Open The Workspace

- Start in the root folder: `/home/max/testgen-suite`
- Read these files first:
  - `WORKSPACE_OVERVIEW.md`
  - `CURRENT_STATE.md`
  - `COMMANDS.md`
  - `DECISIONS.md`

## 2. Identify The Task

Tell the assistant:

- which app you want to work on
- whether you want analysis, editing, or both
- whether the task is local to one app or cross-app

If you do not know yet, ask the assistant to infer the likely active app from `CURRENT_STATE.md`.

## 3. Use The Short Bootstrap Prompt

```text
Read WORKSPACE_OVERVIEW.md, CURRENT_STATE.md, COMMANDS.md, and DECISIONS.md first.
Then tell me:
1. what this workspace is,
2. which app appears active,
3. what the shortest next step is,
4. what you need from me, if anything.
Keep it short.
```

## 4. After A Commit

- Run or let the workspace hooks run `scripts/update-workspace-state.mjs`.
- Re-read `CURRENT_STATE.md` before continuing if the commit touched another repo or changed the plan.

## 5. If Switching Tools

- Re-open the same four root docs.
- Do not rely on the prior model session to remember the project.
- Treat the docs as the shared memory layer.

