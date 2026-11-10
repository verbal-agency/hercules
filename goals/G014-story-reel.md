# G014 — Feature Story Reel

Status: Pending

## Objective

Play the whole film in time at the cheapest possible resolution: one still per beat, temp voices, and real timing. Iterate it with viewers until the chapters can be locked.

## Dependencies

G011 (capability sheet) and G012 (spine, chosen tentpoles, chapter list). May run before or after G013.

## Project scenarios advanced

PS-01, PS-02, PS-07.

## Constraints

- The reel is a story test, not a design. Stills are rough and exploratory and approve no look.
- Every beat is a scene someone could shoot; no summary cards standing in for undecided story.
- Change the story by re-cutting and rewriting, then watching again. Do not add rules to fix a reel problem.
- Story time and presentation order are recorded separately for every scene (`ARCHITECTURE.md`).
- Original inventions are labeled and traceable to the decision log (PS-01).

## In scope

- Pages or scriptment for every chapter, at reel fidelity (dialogue may be rough outside the tentpoles).
- A scene index with stable IDs, presentation order, story-time anchor, chapter, cast, location, purpose, and measured duration.
- A reel: still per beat, temp voices, timing, and minimal sound.
- At least two full iterations, each watched by people other than the writer, with notes recorded and answered.
- A lock list: which chapters are ready for production, in what order.
- A first feature-wide breakdown (entities and states by chapter) to forecast asset demand and cost from the G011 or G013 rates.

## Exclusions

- Polished dialogue for every scene, approved designs, generated video, and final sound.

## Deliverables

- `02_story/chapters/NN_<name>.fountain` for every chapter
- `02_story/scene_index.yaml`
- `07_edit/reel/vNN/` (reel, timeline inventory, and viewing notes per version)
- `02_story/lock_list.md`
- `05_generation/breakdown/feature_forecast.yaml`

## Acceptance criteria

- [ ] The reel plays from opening image to final image with no missing or summarized scene.
- [ ] Measured runtime is within the approved range, or a deviation is approved by the user.
- [ ] Every reel scene maps to exactly one scene-index entry, and story time is reconstructable from the index.
- [ ] At least two reel versions exist, each with recorded reactions from viewers other than the writer, and each note is fixed, rejected with a reason, or routed.
- [ ] The story-level review tests in `02_story/review_rubric.md` (causal chain, setup and payoff ledger, variety, energy curve, premise payoff) have been run on the final version and High findings are resolved or excepted by the user.
- [ ] Every mythological beat is traceable to a source or a labeled invention.
- [ ] The lock list names the chapters approved for production and their order.
- [ ] The forecast estimates shot count, asset states, and cost for the feature from measured rates.

## Expected verification evidence

- Duration sum and ID cross-check by script.
- Viewing notes for each version.
- Review records with resolution status.

## Carried findings

- From G003: every displacement in story time needs a hinge visible in the story; carry consequences across Labor transitions so the world does not reset; no nightmare as automatic punctuation; Prometheus is seen before his chapter.
- From the synopsis review: the eagle, the thumbprint, the "smell", Iolaus, and the legend thread were planted without payoff or had no carrying chapter. The reel is where the ledger is checked.
- Dense multi-thread tableaux (the simultaneous dawns) are a known generation risk (AD-035). Mark each one in the scene index so the forecast prices it.
