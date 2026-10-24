# G007 — Scene/Shot Generation System

Status: Pending

## Objective

Define and validate the inheritable scene- and shot-level contracts connecting screenplay intent, canonical asset inputs, continuity, editorial decisions, prompt compilation, and model-specific generation runs.

## Dependencies

G005 and G006.

## Project scenarios advanced

PS-03, PS-04, PS-05, PS-07.

## Constraints

- Separate model-neutral intent from model adapters.
- Every generated scene has one scene package; every shot inherits from exactly one scene package.
- Every asset binding references a stable version and declares its generation-input role.
- Shot overrides must be explicit and cannot silently contradict visual canon or continuity.
- Preserve generation history rather than overwriting runs.
- Scene packages inherit story-time state and causal predecessors from the scene index; edit-order adjacency is a separate relationship and cannot silently determine continuity.
- Hinges (hinge-in, hinge-out) and ambient threads from the scene index must be representable, and dense multi-thread tableaux must be representable as layered plates, not only as single shots (AD-035).

## In scope

- Scene and shot schemas; inheritance and override rules; asset-input roles; continuity handoff; prompt compilation; provider capability matrices; model routing; Higgsfield adapter; negative constraints; cost fields; run logging; selection states; and one dry-run sequence package.

## Exclusions

- Generating the full film or packaging every screenplay scene.

## Deliverables

- `05_generation/scene_schema.yaml`
- `05_generation/shot_schema.yaml`
- `05_generation/shot_list.csv`
- `05_generation/inheritance_and_compilation.md`
- `05_generation/model_adapter_spec.md`
- `05_generation/provider_capabilities.yaml`
- `05_generation/adapters/higgsfield.md`
- One schema-valid dry-run scene package with child shot packages.

## Acceptance criteria

- [ ] The scene and shot schemas jointly represent every field required by PS-04.
- [ ] A scene package owns shared narrative, spatial, visual, asset, and continuity context and enumerates its child shots.
- [ ] Every shot inherits from exactly one resolvable scene package and declares only active assets and intentional overrides.
- [ ] Every asset input declares a versioned asset ID, role, and required view or derivative when applicable.
- [ ] Model-neutral intent and model-specific prompt/settings are stored separately.
- [ ] Compilation deterministically resolves global style, asset inputs, scene context, shot instructions, and the selected model adapter.
- [ ] The Higgsfield adapter implements `platforms/HIGGSFIELD.md`, including project/folder/Element IDs, Hero Frame, structured camera controls, underlying model/version, cost fields, and output metadata.
- [ ] A live capability matrix records which Higgsfield models support Elements, start/end frames, motion references, sound, duration, resolution, and multi-shot behavior.
- [ ] Shot routing selects a model that exposes every required control or produces an explicit unsupported-field failure.
- [ ] Camera, lens, focal length, aperture, grade, and speed controls are not duplicated inconsistently between structured fields and prompt prose.
- [ ] The exploratory/final quality and credit-approval policy blocks short and cheap before extending or finalizing accepted motion.
- [ ] Continuity-in and continuity-out states are explicit and machine-checkable.
- [ ] Scene and shot schemas distinguish story-time continuity, causal predecessor, edit-order predecessor, and presentation order for nonlinear sequences.
- [ ] Scene packages carry hinge-in, hinge-out, and ambient-thread references from the scene index, and layered-plate shots resolve their component plates.
- [ ] The dry-run sequence resolves its scene, child shots, canonical asset versions, and compiled generation requests.
- [ ] Invalid, missing, or retired IDs cause validation failure.
- [ ] Generation runs and selections can be added without overwriting prior history.

## Expected verification evidence

- Schema and inheritance fixtures for valid and invalid packages.
- Scene/shot/asset resolution, override, and continuity handoff checks.
- Deterministic prompt-compilation snapshot or equivalent comparison.
- Higgsfield adapter fixture covering supported routing, unsupported-field failure, provider-ID round trip, and cost capture.
- Manual dry-run review from story, visual, and editorial perspectives.
