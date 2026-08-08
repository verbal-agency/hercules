# Project Charter

## Purpose

Create a screenplay-ready adaptation of the traditional Hercules stories and a model-portable visual production system for generating a coherent claymation film.

## Target outcome

The completed development package will contain:

- traceable mythological research and explicit adaptation decisions;
- a feature treatment, beat sheet, and screenplay;
- one authoritative visual bible and versioned asset library;
- a scene and shot inventory connected through stable IDs;
- generation-ready scene and shot packages with asset bindings and continuity constraints;
- a validated pilot sequence and an animatic-ready production handoff.

## Current creative hypothesis

- Format: 105–115 minute feature.
- Working title: *Hercules: The Weight*.
- Dramatic spine: madness precedes the Labors, making them an act of atonement.
- Tone: mythic, tactile, emotionally serious, with selective humor and non-graphic treatment of family violence.
- Medium: handcrafted clay stop-motion language, even when produced with video-generation models.
- Scope boundary: the Deianeira/Nessus/death/apotheosis cycle is reserved for a later film or separately approved coda.

These are working decisions. Material changes must be recorded in the adaptation decision log created by Goal G002.

## Project-level acceptance scenarios

These scenarios describe the finished system. Individual goals reference them rather than redefining them.

### PS-01 — Traceable adaptation

Given a major story beat, a reviewer can identify its ancient source, competing variants, and any original adaptation choice.

### PS-02 — Standalone screenplay

Given only the screenplay, a human reader can understand the narrative without generation prompts, asset manifests, or production metadata.

### PS-03 — Visual continuity

Given two shots containing the same canonical entity and continuity state, the entity's design, scale, materials, costume, and damage state remain consistent.

### PS-04 — Reproducible generation package

Given a scene ID, a production artist can locate its shared narrative intent, spatial layout, canonical assets, visual state, continuity boundaries, prompt context, and child shots. Given a shot ID, the artist can resolve the inherited scene context plus its active asset inputs, action, camera, duration, overrides, negative constraints, and generation history.

### PS-05 — Model portability

Given a change of video-generation model, the story and visual canon remain valid; only model-specific derivatives and prompt syntax require replacement.

### PS-06 — Reference provenance

Given any external visual reference, its source, creator or institution when known, rights status, intended use, and retrieval date are recorded.

### PS-07 — Cycle resumability

Given a fresh agent or collaborator, the active goal, dependencies, scope, acceptance criteria, findings, and next eligible goal can be recovered from repository documents.

### PS-08 — Pilot viability

Given the approved pilot sequence, generated shots can be assembled into a coherent scene that preserves narrative action, claymation language, and cross-shot continuity at the agreed quality threshold.

## Non-goals

- Claiming that one ancient account is the single canonical Hercules story.
- Embedding model prompts in screenplay dialogue or action instead of generation packages.
- Treating generated exploratory images as approved canon automatically.
- Producing the entire final film before a representative pilot validates the system.
- Using untracked copyrighted imagery as production input.

## Definition of approved

An artifact is approved only when its status is explicitly recorded as `approved` in the relevant document or manifest. Presence in the repository alone does not imply approval.
