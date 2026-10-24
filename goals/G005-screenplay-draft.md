# G005 — Screenplay Draft One

Status: Pending

## Objective

Write a complete, standalone first-draft feature screenplay that implements the approved treatment and visual-language constraints.

## Dependencies

G003 and G004.

## Project scenarios advanced

PS-01, PS-02, PS-07.

## Constraints

- Preserve scene IDs without embedding production prompts in screenplay prose.
- New mythological inventions require decision-log entries.
- Write action that can plausibly be staged in claymation.
- Every scene contains a physical event that carries its meaning and could be followed with the sound off; comedy arises from character and situation (AD-033).
- Preserve Hercules as messy, not moralized, and the gods' commentary as partial and non-expository (AD-034, AD-036).

## In scope

- Complete screenplay, scene-index synchronization, revision notes, and story-level continuity review.

## Exclusions

- Final shot list, asset generation, and model prompts.

## Deliverables

- `02_story/screenplay.fountain`
- Updated `02_story/scene_index.yaml`
- `02_story/draft_01_notes.md`

## Acceptance criteria

- [ ] The screenplay has a complete beginning, middle, climax, and resolution with no placeholder scenes.
- [ ] Every screenplay scene maps to exactly one stable scene-index entry.
- [ ] Nonlinear presentation follows the approved presentation plan (chapters, hinges, and simultaneous threads from G003), and every scene's story-time position and causal state remain consistent even when editorially separated from its predecessor.
- [ ] Names, chronology, and Labor outcomes conform to approved decisions.
- [ ] The opening and every allusion to the family match the approved disclosure map, and every displacement uses its approved hinge.
- [ ] Every scene passes a sound-off clarity read.
- [ ] The screenplay is readable without production metadata and contains no generation prompts.
- [ ] Estimated runtime is within the approved range or a deviation is documented.
- [ ] Setup/payoff and continuity issues found in review are resolved or explicitly routed.

## Expected verification evidence

- Fountain parse or screenplay-format validation.
- Bidirectional screenplay/scene-index ID check.
- Runtime estimate and manual continuity pass.
