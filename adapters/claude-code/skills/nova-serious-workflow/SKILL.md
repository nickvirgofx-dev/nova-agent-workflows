---
name: nova-serious-workflow
description: Use when Claude Code starts or continues serious project work with Nova Serious Workflow v1.7: Obsidian brain/context, planning/spec, GitHub delivery, verification/risk gate, release/publish, sync-back/learning, and planner/orchestrator/review gates.
---

# Nova Serious Workflow for Claude Code

If the full pack is available, follow `workflows/nova-serious-workflow.md`. If this skill folder was copied alone, the compact rules below are sufficient to operate safely.

Claude Code usage notes:

- Keep project guidance small and local to the project.
- Do not assume a private vault or external memory exists.
- Prefer real files, tests, and command output over stored notes.
- Show a six-layer mini-plan before editing serious tasks: Obsidian Brain, Planning / Spec, GitHub Delivery, Verification / Risk Gate, Release / Publish, and Sync Back / Learning.
- Mark unused layers as `N/A` with a short reason; do not invent specs, GitHub issues, PRs, releases, or publishing for tiny local work.
- Keep task boards/checklists readable for a human.
- Do not add startup hooks or automatic recurring actions from this skill.
- Sync result, decisions, lessons, bug patterns, and next tasks back into project notes.
- Do not rewrite old completed tasks just to retrofit the six-layer format; apply the mini-plan from the next new task onward.
- For app, feature, GitHub, or PR work, use the planner/orchestrator/review overlay: state assumptions, keep specs and issues small, use one approved issue per branch or PR, review simpler options, and ask one plain-language clarification when the goal is blurry.
- Do not create GitHub issues, push, open PRs, mark PRs ready, merge, publish, deploy, or change repo settings without explicit approval for that exact action.
