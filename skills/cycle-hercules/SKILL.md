---
name: cycle-hercules
description: Project overlay for the global `cycle` skill in the Hercules repository. Use together with `cycle` whenever advancing a Hercules roadmap goal; it adapts the generic loop to this creative, document-based workflow.
---

# Cycle overlay for Hercules

Use the global `cycle` skill for the loop. Where this overlay conflicts with it, this overlay wins for this repository. The user's instructions and `AGENTS.md` still outrank both.

## Source of truth

- Project completion contract: `PROJECT.md` (purpose, target outcome, scenarios PS-01 to PS-08, non-goals, definition of approved).
- Roadmap: `ROADMAP.md`. Goal specs: `goals/G0NN-*.md`. Cycle state: `goals/ACTIVE.md`. Backlog: `BACKLOG.md`.
- Story canon: `02_story/canon_now.md` once it exists (G012); until then, and as its history, `01_research/adaptation_decisions.md`. Read its "Current canon at a glance" table first; later AD entries supersede earlier ones.
- Model capability: `05_generation/capability_sheet.md` once it exists (G011). Story and shot planning are written to it.
- `framework/current-goal.yaml` does not exist here. `goals/ACTIVE.md` is the execution state.
- Goal status uses the vocabulary in `goals/README.md` (Pending, Ready, Active, Blocked, Complete, Superseded), not the generic candidate/discovery states.

## Adaptations

1. **Creative approval is the user's.** `PROJECT.md` says an artifact is approved only when its status is recorded as `approved`. Do not self-approve treatment, canon, designs, or screenplay. A goal stays Active until the user approves its creative deliverables; report it as "criteria met, awaiting approval".
2. **Open questions stay open.** If a goal lists open story questions, decide them with the user during development, by putting concrete alternatives in front of them (two or three written variants, two cuts) rather than an abstract choice. Do not resolve them silently to close the goal, and do not treat unresolved ones as blockers unless an acceptance criterion requires a decision.
3. **Decision log for material changes.** Any change to approved canon, tone, structure, or boundaries is a new dated, superseding entry in `adaptation_decisions.md`. Do not rewrite history.
4. **Goals are pre-written specs, not stubs.** Do not create replacement stubs. Prepare the next goal by adding routed findings to its existing file and updating `goals/ACTIVE.md` and `ROADMAP.md`. Do not begin it.
5. **Slicing.** Goal files here carry many criteria and several deliverables, so the "three to five criteria" sizing check does not apply. A goal may span several sessions: name the current slice (for example one deliverable), record progress in the goal file, and keep it Active until every criterion passes.
6. **Learning layer is off.** This project is not teaching a domain. Skip the pre-goal brief, build log, and study notes.
7. **Verification is review, not tests.** Use the goal's own evidence list (duration sums from the scene index, run-log counts, ID cross-checks, YAML parsing, link checks, playback, recorded viewer reactions). Script mechanical checks where possible and say plainly which checks are judgments by a reader.
8. **Handoff packet.** Replace "Try it" and "Diagram delta" with: reading order of changed documents, a one-paragraph story-so-far, the open questions still carried, and any decision the user must make. Keep the outcome card and the suggested commit message.
9. **Domain skills.** Use `develop-hercules-screenplay` for research, canon, treatment, screenplay, scene and shot work. Use `higgsfield-film-production` for G011, G013, and G015. In G011 the outputs are exploratory and approve nothing; from G013 onward, finish story and provider-neutral decisions for a shot before compiling it through Higgsfield.
10. **Anti-churn for story.** A repeated rewrite of the same structure counts as one failure lineage. After two failed structural passes, stop and ask the user whether the contract or a constraint needs to change.
11. **Evidence over rules.** When a page or a reel has a problem, fix it by rewriting or re-cutting and looking again. Do not add a constraint or an acceptance criterion to a goal to fix a creative problem, and do not turn an intention into a gate (`goals/README.md`, "Writing a goal").
12. **Two ready goals.** `goals/ACTIVE.md` may list more than one eligible goal. Activate the one the user names; if they name none, ask.
13. **Branches and PRs.** Work on a branch, never directly on `main`. Commit and push only when the user asks.
