# G013 — *Eurystheus* Short: First Vertical Slice

Status: Pending

## Objective

Take chapter one through every layer, from locked pages to an edited short with sound, and freeze the production schemas at v1 from what the slice actually needed.

## Dependencies

G011 (capability sheet) and G012 (chosen opening and spine).

## Project scenarios advanced

PS-02, PS-03, PS-04, PS-05, PS-06, PS-08.

## Constraints

- Write and plan to the capability sheet. Ration what it rates expensive; avoid what it rates not possible.
- Assets are derived from the pages by breakdown, not designed ahead of need. Every costume or damage state is a cost the pages must justify.
- Approval is the user's: pages, designs, Hero Frames, and the final cut each need a recorded approval.
- Canonical assets, once referenced by an approved shot, are immutable; revisions create a new version (`ARCHITECTURE.md`).
- Style rules cover only what this chapter uses. Olympus, nightmare, and memory grammars arrive with the chapters that need them.
- Set the continuity and style thresholds before generating.

## In scope

- Chapter-one pages locked at 3 to 5 minutes, with scene cards and stable scene IDs.
- **Breakdown:** an entity-by-state matrix for the chapter (characters, creatures, locations, props, costumes, damage states, by scene) and the asset demand list it implies.
- Style rules v1 and approved canonical assets for exactly that demand list, with provenance.
- Scene packages, shot list, a start frame per shot, generation, selects.
- Voices, sound, and an edited cut.
- **Schema freeze v1:** scene and shot records, asset manifest, and run record, built from the fields G011 and this slice used, with a validator.
- The remaining provider comparisons from `platforms/HIGGSFIELD.md`.

## Exclusions

- Any other chapter, the feature scene index, and assets no shot in this chapter uses.

## Deliverables

- `02_story/chapters/01_eurystheus.fountain` and its scene cards
- `05_generation/breakdown/ch01.yaml` (entity-by-state matrix and asset demand)
- `03_visual_bible/style_bible.md` (v1, chapter-one scope)
- `04_asset_library/asset_manifest.yaml` and approved masters
- `05_generation/schemas/` (v1) and a validation script
- `05_generation/ch01/` scene and shot packages; `06_generations/ch01/`; `07_edit/ch01/`
- `05_generation/slice_report.md` (cost, takes, failures by cause, what to change before chapter two)

## Acceptance criteria

- [ ] The locked pages pass Tier 1 on every scene and Tier 2 on the opening, and the user has approved them.
- [ ] Every entity and state in the breakdown resolves to an approved, versioned asset or an approved incidental-asset rule; no asset exists that no shot uses.
- [ ] Every shot record validates against schema v1 and carries its dialogue or audio, shot class, start (and end, where used) frame, resolved asset versions, and take history.
- [ ] Every selected shot can be traced from page to scene package to shot record to run to source output (PS-04).
- [ ] The same character in the same state stays consistent across the chapter's shots at the threshold agreed beforehand (PS-03).
- [ ] The cut plays start to finish with sound and communicates the chapter without explanatory text.
- [ ] At least two people other than the writer have watched the cut and their reactions are recorded.
- [ ] The slice report gives cost per accepted second, takes per accepted shot, and failures classified as story, asset, package, model, or editorial.
- [ ] The provider comparisons are complete or each omission is explained, and the provider is confirmed or rejected for G015.

## Expected verification evidence

- Schema validation and ID resolution by script, including fixtures that must fail.
- Breakdown-to-manifest coverage report.
- Playback review against the pre-agreed thresholds.
- Credit reconciliation.

## Carried findings

- From G006: locations record geography, playable routes, depth planes, a blocking anchor, one motivated light, a three-quarter master, and a reverse.
- From G007: keep story-time continuity, causal predecessor, and edit-order predecessor as separate fields; this chapter is linear but the schema must not assume that.
- From G004: mortals, gods, and monsters should read as different makings. Chapter one needs only the mortal and monster ends of that taxonomy.
- From AD-019: Roman imperial Hercules must not become the unmarked default design.
