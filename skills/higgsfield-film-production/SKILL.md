---
name: higgsfield-film-production
description: Prepare, validate, or execute Higgsfield-ready image and video generation for the Hercules claymation project. Use for Higgsfield model selection, Hero Frames, reference-bound shots, start/end frames, shot prompts, generation metadata, pilot comparisons, or continuity review; do not use for story canon or screenplay decisions.
---

# Higgsfield Film Production

Treat repository story and visual-canon files as authoritative. Treat Higgsfield as a provider adapter.

## Workflow

1. Read `platforms/HIGGSFIELD.md`, `ARCHITECTURE.md`, and the applicable scene, shot, and asset records.
2. Refuse generation when the shot lacks an approved asset binding or Hero Frame required by the project gate.
3. Query the live Higgsfield catalog before selecting a model. Prefer controls required by the shot over a universal default.
4. For serious 4–15 second cinematic motion, evaluate the current Seedance offering first; evaluate Cinema Studio for the highest-fidelity camera work and Kling for simpler or lower-cost shots. Confirm current capabilities rather than relying on these defaults.
5. Put composition, identity, costume/state, location, light, clay materials, and depth in the approved Hero Frame. Put narrative action, physical motion, emotional beat, and otherwise-unfixed information in prompt prose.
6. Express camera, focal length, aperture, duration, resolution, start/end frames, and supported motion controls structurally. Do not duplicate conflicting values in prose.
7. Generate one shot at a time during validation. Use automatic multi-shot generation only for an explicit experiment or a low-continuity montage.
8. Save the compiled prompt, resolved assets, controls, model/version, generation ID, output, and cost data defined in `platforms/HIGGSFIELD.md`.
9. Review identity, geography, screen direction, clay texture, stepped motion, artifacts, and endpoint continuity before approval.

## Prompt contract

Compile each shot in this order:

1. subject and continuity state;
2. one readable action and emotional change;
3. physical secondary motion;
4. camera movement only when not represented by a structured control;
5. claymation motion/material constraints;
6. exclusions needed to protect canon.

Avoid keyword piles, competing actions, unsupported controls, and full-scene prompts. Do not ask a single generation to solve an entire dramatic scene.

## Higgsfield CLI boundary

Use the official `higgsfield` CLI when execution is requested. Check authentication and ask the user to complete interactive login when required. Run live model/workflow discovery before invoking a model, use one-shot create-and-wait behavior when available, and return the media URL plus a compact generation summary.

Read `references/provenance.md` when updating this skill or reconciling it with upstream Higgsfield guidance.
