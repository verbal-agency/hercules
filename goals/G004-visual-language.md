# G004 — Claymation Visual Language

Status: Pending

## Objective

Approve a model-neutral visual language covering clay materials, design grammar, palette, motivated lighting, optical packages, camera, motion, scale, grading, violence, and transitions.

## Dependencies

G003.

## Project scenarios advanced

PS-03, PS-05, PS-06, PS-07.

## Constraints

- Visual rules must work across video models and practical stop-motion.
- References require provenance; exploration is not automatically canon.
- Human, divine, and monstrous materials must be distinguishable.
- The adult violence target must remain consequential in clay without relying on photorealism or assuming stylization lowers the rating. Its depiction must be tasteful and never gratuitous; every direct image must serve character, consequence, theme, or plot.
- Olympus, ordinary waking life, remembered violence, divine intrusion, and nightmare must have related but distinguishable visual grammars.
- Nonlinear shifts must have a legible temporal grammar that distinguishes story-time displacement, anticipatory cutaway, memory, nightmare, and divine vision without depending on exposition.
- Olympus shares sets with the mortal world (gods appear in mortal rooms, mortal smoke and objects cross into Olympus); the visual grammar must make that interpenetration legible, not a separate island (AD-026, AD-034).
- Simultaneity (distant figures such as Prometheus's eagle, Atlas's sky, and the ledger woven into ordinary scenes) needs a per-thread clock language and plans for layered plates, because dense multi-thread tableaux are a known risk for single-prompt generation (AD-035).
- Humor must be physical and stageable in clay (transformation, effort, scale, contraption); the dark-comedy register must coexist with unjoked consequence (AD-033, AD-024).
- Explore a material taxonomy in which mortals, gods, and monsters read as different makings (for example raw, handled clay versus finished or fired divine surfaces), and the clay-maker origin of mortals attributed to Prometheus.

## In scope

- Style principles, reference boards, material taxonomy, color script, motivated-light rules, optical packages, camera grammar, motion cadence, effects language, grade presets, scale strategy, adult violence representation, Olympus language, and nightmare/memory language.

## Exclusions

- Complete character turnarounds, screenplay pages, and shot prompts.

## Deliverables

- `03_visual_bible/style_bible.md`
- `03_visual_bible/materials.md`
- `03_visual_bible/camera_and_motion.md`
- `03_visual_bible/camera_rig_and_lenses.md`
- `03_visual_bible/lighting_and_grade.md`
- `03_visual_bible/color_script.md`
- `03_visual_bible/tone_and_violence.md`
- Provenance-complete reference boards.

## Acceptance criteria

- [ ] A reviewer can distinguish mortal, Olympian, monstrous, remembered, nightmare, and active divine-intrusion imagery using documented rules.
- [ ] Rules show how Olympus and mortal scenes share a set, how a god in a mortal room is rendered, and how per-thread clocks (the eagle, the sky, the ledger) are shown and read.
- [ ] A layered-plate approach is documented and tested for at least one dense multi-thread tableau.
- [ ] Temporal and transition rules let a viewer distinguish present action, displaced story time, anticipation, memory, nightmare, and divine vision while preserving purposeful ambiguity where approved by G003.
- [ ] Every feature sequence has an assigned palette and lighting state.
- [ ] Camera and motion rules define the intended stop-motion cadence and prohibited CGI-like behavior.
- [ ] Approved optical packages define camera/sensor profile, lens family, focal-length range, aperture/depth behavior, aspect ratio, and intended shot use.
- [ ] Every principal location defines one motivated light source, direction, falloff, and permitted grade treatments.
- [ ] Camera, lens, light, and grade rules can map to structured provider controls without becoming provider-specific canon.
- [ ] Violence rules specify direct, fractured-subjective, silhouetted, implied, and prohibited imagery, including distinct handling for the family deaths, human combat, creature combat, Prometheus's punishment, and aftermath, plus a narrative-purpose test that excludes gratuitous imagery.
- [ ] At least one visual example or test supports every major style rule.
- [ ] All external references satisfy PS-06 metadata.
- [ ] The bible contains no model-specific prompt syntax.

## Expected verification evidence

- Sequence-to-color-script coverage check.
- Rule-to-example traceability review.
- Reference-manifest validation.
