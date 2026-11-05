---
name: cycle-hercules
description: Project overlay for the global `cycle` skill in the Hercules repository. Use together with `cycle` whenever advancing a Hercules roadmap goal; it adapts the generic loop to this creative, document-based workflow.
---

# Cycle overlay for Hercules

Use the global `cycle` skill for the loop. Where this overlay conflicts with it, this overlay wins for this repository. The user's instructions and `AGENTS.md` still outrank both.

## Source of truth

- Project completion contract: `PROJECT.md` (purpose, target outcome, scenarios PS-01 to PS-08, non-goals, definition of approved).
- Roadmap: `ROADMAP.md`. Goal specs: `goals/G0NN-*.md`. Cycle state: `goals/ACTIVE.md`. Backlog: `BACKLOG.md`.
- Story canon: `01_research/adaptation_decisions.md`. Read its "Current canon at a glance" table first; later AD entries supersede earlier ones.
- `framework/current-goal.yaml` does not exist here. `goals/ACTIVE.md` is the execution state.
- Goal status uses the vocabulary in `goals/README.md` (Pending, Ready, Active, Blocked, Complete), not the generic candidate/discovery states.

## Adaptations

1. **Creative approval is the user's.** `PROJECT.md` says an artifact is approved only when its status is recorded as `approved`. Do not self-approve treatment, canon, designs, or screenplay. A goal stays Active until the user approves its creative deliverables; report it as "criteria met, awaiting approval".
2. **Open questions stay open.** If a goal lists open story questions, decide them with the user during development. Do not resolve them silently to close the goal, and do not treat unresolved ones as blockers unless an acceptance criterion requires a decision.
3. **Decision log for material changes.** Any change to approved canon, tone, structure, or boundaries is a new dated, superseding entry in `adaptation_decisions.md`. Do not rewrite history.
4. **Goals are pre-written specs, not stubs.** Do not create replacement stubs. Prepare the next goal by adding routed findings to its existing file and updating `goals/ACTIVE.md` and `ROADMAP.md`. Do not begin it.
5. **Slicing.** Goal files here carry many criteria and several deliverables, so the "three to five criteria" sizing check does not apply. A goal may span several sessions: name the current slice (for example one deliverable), record progress in the goal file, and keep it Active until every criterion passes.
6. **Learning layer is off.** This project is not teaching a domain. Skip the pre-goal brief, build log, and study notes.
7. **Verification is review, not tests.** Use the goal's own evidence list (duration sums from the scene index, coverage reviews, ID cross-checks, YAML parsing, link checks). Script mechanical checks where possible and say plainly which checks are judgments by a reader.
8. **Handoff packet.** Replace "Try it" and "Diagram delta" with: reading order of changed documents, a one-paragraph story-so-far, the open questions still carried, and any decision the user must make. Keep the outcome card and the suggested commit message.
9. **Domain skills.** Use `develop-hercules-screenplay` for research, canon, treatment, screenplay, scene and shot work. Use `higgsfield-film-production` only from G007 onward. Finish story and provider-neutral decisions before compiling anything through Higgsfield.
10. **Anti-churn for story.** A repeated rewrite of the same structure counts as one failure lineage. After two failed structural passes, stop and ask the user whether the contract or a constraint needs to change.
11. **Branches and PRs.** Work on a branch, never directly on `main`. Commit and push only when the user asks.
