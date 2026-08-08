# G006 — Canonical Visual Asset Library

Status: Pending

## Objective

Create the approved core visual canon and manifest required to depict the screenplay consistently across human and model-driven production.

## Dependencies

G004 and G005.

## Project scenarios advanced

PS-03, PS-05, PS-06, PS-07.

## Constraints

- Maintain one authoritative visual library.
- Keep exploratory, approved, and model-derived assets separate.
- Version all approved assets and continuity states.

## In scope

- Recurring mortal and Olympian characters, Prometheus, principal creatures, mortal and divine locations, props, costumes, scale chart, expressions, damage states, nightmare/memory variants, Hero Frames, location continuity locks, provider-ready derivatives, and reference manifest.

## Exclusions

- Complete shot prompts and final video generation.

## Deliverables

- `04_asset_library/asset_manifest.yaml`
- Approved master sheets and model-ready derivatives.
- `03_visual_bible/scale_chart.*`
- `03_visual_bible/continuity_states.md`
- Character/creature Element derivatives and location master/reverse packages required by `platforms/HIGGSFIELD.md`.

## Acceptance criteria

- [ ] Every entity required by the screenplay scene index has an asset ID or an approved incidental-asset policy.
- [ ] Every recurring entity has an approved version, master path, provenance, and necessary continuity states.
- [ ] Character, costume, prop, wound, and environment states are keyed to story chronology independently of presentation order so nonlinear editing cannot silently revert continuity.
- [ ] The Olympian ensemble, Olympus environments, Prometheus and his rock, and all recurring nightmare/memory symbols have approved assets or explicitly approved reuse/variation rules.
- [ ] Hercules has approved turnarounds for every costume and damage state used in the screenplay.
- [ ] Creature sheets describe anatomy, scale, movement, and rig-sensitive failure risks.
- [ ] Approved assets expose the model-ready views and derivatives needed for declared generation-input roles.
- [ ] Each principal character and creature has clean identity, front, three-quarter, expression, material, scale, and shot-matched Hero Frame derivatives where required.
- [ ] Materially different costumes or damage states resolve to explicit asset versions or separate provider Elements.
- [ ] Every principal location records geography, playable routes, three depth planes, a blocking anchor, one motivated light, a three-quarter master, and an approved reverse.
- [ ] Hero Frames have an approval gate covering composition, identity, state, location, light, material, depth, and visible artifacts before animation.
- [ ] Exploratory, approved, and derivative files are distinguishable by path and manifest status.
- [ ] No approved shot can resolve silently to an unversioned asset.

## Expected verification evidence

- Manifest schema and path validation.
- Scene-index-to-asset coverage report.
- Manual turnaround, scale, and continuity-state review.
