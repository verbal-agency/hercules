# Production Architecture

## Three-layer system

### 1. Story layer

Human-readable dramatic sources: research, decision log, treatment, character arcs, beat sheet, screenplay, and scene index.

Rules:

- The screenplay remains readable without production metadata.
- Scenes receive stable IDs such as `SC_030_HYDRA_MARSH`.
- Source tradition, inference, and original invention are labeled in research documents.
- Model prompts never become the authoritative description of story intent.

### 2. Visual canon layer

The single source of truth for approved visual identity: characters, creatures, locations, props, palette, materials, scale, and continuity states.

Rules:

- Canonical entities receive stable IDs such as `CHR_HERCULES`, `CRE_HYDRA`, and `LOC_LERNA_MARSH`.
- Versions are immutable once referenced by an approved shot package. Revisions create a new version.
- Exploratory and approved assets remain visibly separated.
- Each external reference carries provenance and rights metadata.
- Model-ready crops and turnarounds are derivatives of approved masters, not independent designs.

### 3. Generation layer

Inheritable scene and shot instructions derived from the story and visual canon, then compiled for a selected video model.

Rules:

- Every screenplay scene that will be generated receives a scene package keyed by its stable scene ID.
- Scene packages own shared narrative intent, spatial layout, time, lighting, palette, material rules, continuity boundaries, canonical asset bindings, and scene-wide constraints.
- Shots receive stable IDs such as `SH_0063` and inherit from exactly one scene package.
- Shot packages own active asset inputs, starting state, one primary action whenever practical, camera, duration, continuity changes, and shot-specific overrides.
- Every asset binding references an explicit canonical version and declares its input role, such as `identity`, `environment`, `composition`, `style`, or `previous-shot-continuity`.
- Model-neutral intent is stored separately from model-specific prompt syntax and settings.
- Model adapters compile global style, scene context, shot instructions, resolved assets, and supported settings into an executable generation request.
- Raw generations, selects, and approved editorial outputs remain distinct.

## ID conventions

| Entity | Pattern | Example |
|---|---|---|
| Scene | `SC_NNN_SLUG` | `SC_030_HYDRA_MARSH` |
| Shot | `SH_NNNN` | `SH_0063` |
| Blocking/layout | `BLK_SCNNN_NAME` | `BLK_SC030_HYDRA_RING` |
| Character | `CHR_NAME` | `CHR_HERCULES` |
| Creature | `CRE_NAME` | `CRE_HYDRA` |
| Location | `LOC_NAME` | `LOC_LERNA_MARSH` |
| Prop | `PROP_NAME` | `PROP_BRONZE_SWORD` |
| Costume | `CST_NAME_STATE` | `CST_HERCULES_LIONSKIN` |
| Visual style | `STY_NAME` | `STY_TERRACOTTA_NIGHT` |

Canonical version references append `_VNN`, for example `CRE_HYDRA_V03`.

## Intended repository layout

```text
01_research/          sources, variants, decision log
02_story/             treatment, beats, characters, screenplay, scene index
03_visual_bible/      style rules and visual-development documents
04_asset_library/     exploratory and approved canonical assets plus manifest
05_generation/        schemas, scene packages, shot packages, and model adapters
06_generations/       raw outputs, selects, logs
07_edit/              storyboards, animatic, continuity notes
goals/                cycle state and goal specifications
```

Directories are created by the goal that first owns their contents; empty scaffolding is avoided.

## Required metadata

### Reference record

```yaml
reference_id: REF_0001
title: ""
source_url: ""
institution_or_creator: ""
retrieved: YYYY-MM-DD
rights_status: unknown
allowed_use: research-only
supports:
  - CHR_HERCULES
notes: ""
```

### Canonical asset record

```yaml
asset_id: CHR_HERCULES
version: 1
status: exploratory
master_path: ""
approved_by: null
approved_on: null
reference_ids: []
continuity_states: []
derivatives: []
notes: ""
```

### Scene package

```yaml
scene_id: SC_030_HYDRA_MARSH
status: planned
narrative_objective: ""
emotional_progression: ""
asset_bindings:
  - asset: LOC_LERNA_MARSH_V02
    role: environment
    views: [master, reverse]
    required: true
  - asset: CHR_HERCULES_V04
    role: identity
    views: [front, three_quarter]
    required: true
continuity_in: []
continuity_out: []
spatial_layout: BLK_SC030_HYDRA_RING_V01
time_and_weather: ""
lighting: ""
palette: ""
material_rules: []
model_neutral_scene_prompt: ""
scene_avoid: []
shots: []
```

### Shot package

```yaml
shot_id: SH_0001
scene_id: SC_001_STOLEN_BIRTH
status: planned
duration_seconds: 0
asset_inputs:
  - asset: CHR_HERCULES_V04
    role: identity
    views: [front, three_quarter]
    inherited_from_scene: true
starting_state: ""
continuity_in: []
continuity_out: []
camera: {}
action:
  start: ""
  primary_motion: ""
  end: ""
overrides: {}
model_neutral_shot_prompt: ""
shot_avoid: []
model_runs: []
selected_output: null
```

## Prompt compilation

The executable request is assembled rather than maintained as one hand-written master prompt:

```text
global style package
  + resolved canonical asset inputs
  + scene package
  + shot package
  + model adapter
  = executable generation request
```

Inheritance rules:

1. Global style establishes film-wide material and motion rules.
2. The scene package establishes shared visual, spatial, narrative, and continuity context.
3. The shot package narrows that context to active inputs, camera, duration, and one primary action.
4. Shot overrides must be explicit and may not silently contradict canonical asset identity or continuity.
5. The model adapter translates supported fields and records anything it cannot express.
6. The compiled request and resolved asset list are stored with each generation run for reproducibility.

## Provider adapters

Provider adapters translate the model-neutral package into a platform without moving canonical ownership into that platform.

Each adapter must define:

- the provider's project, scene, folder, element, and generation-ID mapping;
- a live capability matrix by underlying model and version;
- how canonical assets become provider-compatible derivatives or reusable elements;
- how global style, scene context, shot instructions, camera controls, and negative constraints are compiled;
- which fields are expressed as structured controls rather than repeated in prompt prose;
- supported start frame, end frame, motion-reference, audio, duration, resolution, and multi-shot behavior;
- cost estimation and approval points;
- export and round-trip metadata requirements;
- unsupported fields and the required fallback or validation warning.

The initial adapter candidate is defined in `platforms/HIGGSFIELD.md`.

### Platform run record

```yaml
provider: higgsfield
provider_project_id: ""
provider_folder_id: ""
provider_element_ids: []
provider_generation_id: ""
provider_model: ""
provider_model_version: ""
provider_controls: {}
hero_frame_asset: null
compiled_prompt: ""
resolved_assets: []
estimated_cost: null
actual_cost: null
source_output: ""
```

Provider IDs augment stable project IDs; they never replace them.

## Change control

- Story changes that alter intent update the treatment or screenplay and scene index.
- Visual changes update the canonical asset version and every affected future scene or shot package.
- Model changes add or replace derivatives and model-run records; they do not rewrite visual canon.
- Provider-side projects, Elements, prompts, and edits must be exportable or reconstructable from repository records.
- Retired IDs are never reassigned.
- Material schema changes require an architecture decision before dependent artifacts are updated.
