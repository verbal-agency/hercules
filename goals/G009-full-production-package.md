# G009 — Full Generation-Ready Production Package

Status: Pending

## Objective

Scale the validated pilot system across the screenplay so every generated scene and planned shot is asset-resolved, generation-ready, and continuity-connected.

## Dependencies

G008.

## Project scenarios advanced

PS-03, PS-04, PS-05, PS-06, PS-07.

## Constraints

- Use the pilot-approved schema and quality rules.
- Resolve new asset or architecture gaps canonically, not inside isolated prompts.
- This goal packages shots; it does not require final-film generation.

## In scope

- Complete scene packages, shot decomposition, inheritance, coverage, asset resolution, continuity graph, model-neutral packages, compiled requests, provider mappings, cost estimates, and selected-model adapters.

## Exclusions

- Final generation of all shots, sound design, score, and final color.

## Deliverables

- Complete `05_generation/shot_list.csv`.
- Scene packages for all generated screenplay scenes.
- Child shot packages and compiled requests for all planned shots.
- Coverage and continuity reports.
- Updated asset manifest and provenance for approved discoveries.
- Provider run manifests linking project IDs to Higgsfield project, folder, Element, Hero Frame, model, generation, cost, and exported-output IDs.

## Acceptance criteria

- [ ] Every screenplay scene has a valid scene package and editorial coverage, or a documented no-generation rationale.
- [ ] Every scene and shot passes schema, inheritance, asset-ID, provenance, override, and continuity validation.
- [ ] Every scene package enumerates exactly the child shots assigned to that scene.
- [ ] Every shot’s executable request can be rebuilt from global style, resolved assets, scene context, shot instructions, and its model adapter.
- [ ] Every continuity state has a valid predecessor or an explicit establishing event.
- [ ] No package uses an unapproved or unversioned canonical asset.
- [ ] Model adapters exist for the selected production model without altering model-neutral intent.
- [ ] Every provider run preserves repository scene/shot/asset IDs alongside provider project/folder/Element/generation IDs and underlying model version.
- [ ] Every selected output has exported or reconstructable prompt, structured controls, resolved assets, cost, and source media.
- [ ] Provider-side edits or regenerations that affect canon are reconciled into repository versions before dependent shots proceed.
- [ ] Coverage and estimated shot durations reconcile with the target runtime.

## Expected verification evidence

- Full-package, inheritance, and compilation validation report.
- Screenplay/scene/shot coverage matrix.
- Continuity graph audit and total-duration calculation.
