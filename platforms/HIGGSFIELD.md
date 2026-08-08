# Higgsfield Provider Profile

Status: Candidate for G008 pilot validation

## Role

Higgsfield may serve as the production cockpit for image development, reusable Elements, virtual-camera setup, video-model routing, generation, and initial editorial review. It does not own canonical story or visual decisions.

## Project mapping

| Project contract | Higgsfield mapping |
|---|---|
| Global style package | Project brief |
| Canonical character, location, or prop | Reusable Element derived from an approved master |
| Scene package | Scene setup: cast, mood, location, light, and continuity context |
| Shot package | Shot folder, Prompt Box settings, and structured controls |
| Camera specification | Virtual camera rack and motion controls |
| Shot-matched start image | Hero Frame or start frame |
| End-state target | End frame when supported |
| Model adapter | Selected Higgsfield/Cinema Studio model configuration |
| Generation run | Higgsfield generation plus exported prompt, controls, inputs, and output |

## Required repository metadata

```yaml
provider: higgsfield
higgsfield_project_id: ""
higgsfield_folder_id: ""
higgsfield_element_ids: []
higgsfield_hero_frame_id: ""
higgsfield_generation_id: ""
underlying_model: ""
underlying_model_version: ""
camera:
  body: ""
  lens: ""
  focal_length: ""
  aperture: ""
controls:
  genre: ""
  grade: ""
  camera_motion: []
  speed_ramp: ""
  duration_seconds: 0
  resolution: ""
  sound: null
start_frame: null
end_frame: null
motion_reference: null
compiled_prompt: ""
resolved_assets: []
estimated_credits: null
actual_credits: null
source_output: ""
```

## Asset preparation

### Characters and creatures

- Create a reusable Element only from an approved, versioned canonical master.
- Maintain separate Elements or derivatives for materially different costumes and damage states.
- Prepare a clean identity view, front and three-quarter views, key expressions, clay material close-up, scale reference, and shot-matched Hero Frames.
- Treat Soul ID as a real-person identity workflow unless pilot evidence supports the intended invented clay character; evaluate Soul Cast or ordinary Elements for Hercules and creatures.

### Locations

- Define geography, playable routes, three depth planes, and one motivated light before style embellishment.
- Approve a three-quarter master and a matching reverse.
- Name at least one physical blocking anchor rather than relying only on screen-left or screen-right.
- Preserve openings, anchor, light direction, materials, palette, and depth across views.
- Allow a single master wide only when off-frame invention cannot break later blocking or continuity.

### Hero Frame gate

Video generation may begin only after the shot’s Hero Frame or start frame passes composition, identity, costume/state, location, light, materials, depth, and artifact checks. A failed whole composition is regenerated from corrected inputs; local fixes are reserved for contained defects.

## Adapter behavior

- Read the live model controls before routing a shot; available Elements, duration, resolution, sound, start/end frames, and other controls vary by model.
- Prefer the model exposing the controls required by the shot rather than routing every shot through one model.
- Express camera, lens, focal length, aperture, grade, speed ramp, and other supported settings as structured controls; avoid duplicating them inconsistently in prompt prose.
- Keep prompts focused on narrative action, physical motion, emotional beat, and information not already fixed by the Hero Frame or structured controls.
- Block short at exploratory quality, then extend or finalize only approved motion.
- Record unsupported package fields and their fallback; do not silently drop them.

## Pilot comparisons

G008 must compare:

- manual setup versus AI Director assistance;
- one versus several reference Elements where supported;
- Hero-Frame-first versus direct text-to-video;
- single-shot versus automatic multi-shot;
- at least two viable underlying models;
- start-frame versus start/end-frame control;
- character and location continuity across a reverse angle;
- clay texture, proportions, and stepped stop-motion retention;
- metadata/export completeness and reproducibility;
- estimated versus actual credits per accepted second.

## Commitment gate

Higgsfield may become a preferred production adapter only if the pilot establishes acceptable identity, location, material, motion, metadata, cost, and export behavior. Failure keeps the model-neutral packages valid for another provider.
