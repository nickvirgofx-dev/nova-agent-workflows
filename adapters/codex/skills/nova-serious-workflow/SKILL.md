---
name: nova-serious-workflow
description: Use when starting or continuing a serious project with Nova Serious Workflow v1.8: context contract, Goal/Rider task framing, six-layer mini-plan, planning/spec, GitHub delivery gates, verification/risk gate, release/publish gate, sync-back/learning, structured risk approval, retry budget, task-thread events, runtime harness verdicts, and planner/orchestrator/review gates.
---

# Nova Serious Workflow

If the full pack is available, use `workflows/nova-serious-workflow.md` as the canonical public workflow. If this skill folder was copied alone, the compact rules below are sufficient to operate safely.

For Codex:

1. Read the project entry files before editing.
2. Prefer the user's current request and real files over stored notes.
3. Before meaningful edits, state a compact context contract: user goal, project, primary state files, exact source files, runtime/repo evidence, verification target, excluded context, and stop rules.
4. Frame serious tasks with Goal, Rider, done condition, verification, stop rule, and recommended intelligence.
5. Show a Nova Serious Workflow mini-plan before editing serious `T###` tasks:
   - Obsidian Brain Layer
   - Planning / Spec Layer
   - GitHub Delivery Layer
   - Verification / Risk Gate Layer
   - Release / Publish Layer
   - Sync Back / Learning Layer
6. Mark unused layers as `N/A` with a short reason; do not invent specs, GitHub issues, PRs, releases, or publishing for tiny local work.
7. Keep task IDs explicit, such as `T001`.
8. Use Markdown checkboxes in task boards and checklists.
9. Archive before compacting or restructuring important notes.
10. Before meaningful actions, classify the action as `allow`, `warn`, `review`, or `block`.
11. Stop before risky actions listed in the workflow.
12. If the same root cause fails twice, stop with exact command/action, error, evidence checked, and the next safer check.
13. Verify before marking complete.
14. Sync results, decisions, lessons, bug patterns, and next tasks back into project notes.
15. Do not rewrite old completed tasks just to retrofit the six-layer format; apply the mini-plan from the next new task onward.
16. For app, feature, GitHub, or PR work, use the planner/orchestrator/review overlay:
   - state assumptions and acceptance criteria;
   - keep specs and issues small;
   - use one approved issue per branch or PR;
   - review whether a simpler path exists;
   - ask one plain-language clarification when the goal is blurry.
17. Do not create GitHub issues, push, open PRs, mark PRs ready, merge, publish, deploy, register MCP, enable hooks, change global config, run database/index migrations, or change repo settings without explicit approval for that exact action.

Final report:

```text
completed:
files changed:
task updated:
intelligence used:
verification:
not tested:
risks:
next:
```
