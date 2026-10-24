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
- Tone: adult dark comedy with real consequence (AD-033), targeting an R rating, with visible consequential violence, selective humor, and an evolving nightmare language for Hercules's trauma.
- Medium: handcrafted clay stop-motion language, even when produced with video-generation models.
- Structure: a braided, selectively nonlinear presentation interweaves Hercules's journey with active supporting-character, creature, and divine threads. Hera, Eurystheus, Iolaus, threatened communities, Prometheus, Atlas, Cerberus, and the gods may initiate or reframe movements before Hercules enters them.
- World: the Labors, divine politics, mortal institutions, Prometheus's punishment, and the Underworld belong to one causally connected mythic system rather than an anthology of disconnected quests.
- Scope boundary: the Deianeira/Nessus/death/apotheosis cycle is reserved for a later film or separately approved coda.

G002 approved the original story boundaries; user-approved amendments AD-024 through AD-031 now govern tone, haunting, Olympus, Zeus, Hera's continuous campaign, world unity, the progressively revealed purposes of the Labors, and braided nonlinear presentation. Material changes must be recorded as superseding entries in `01_research/adaptation_decisions.md`.

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
