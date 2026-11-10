# G011 — Capability Probe: The Jar Scene

Status: Ready

## Objective

Generate one short scene end to end and measure what the models can and cannot do, so that story and schemas are written against evidence.

## Dependencies

G002. Requires provider access and a credit budget approved by the user (see "User decisions needed").

## Project scenarios advanced

PS-03, PS-05, PS-08.

## Why this scene

`02_story/reviews/calibration/scene_a_jar.fountain` is about one minute: one set, two on-camera speakers, an antagonist who is mostly a voice inside a jar, one heavy prop (the lion), one insert (the thumbprint), and a small court. It exercises identity, dialogue, weight, and an insert without needing a creature fight. Using it here does not make it canon or approve it.

## Constraints

- Everything produced is exploratory. No look, asset, or page is approved by this goal.
- Agree the acceptance threshold for a shot before generating (carried from G008).
- Keep the three layers separate: prompts live in generation records, not in the scene.
- Record every run, including failures. Failures are the main output.
- Stay inside the approved credit budget; stop and report if it runs out before the criteria are met.
- Keep schemas minimal. Record whatever fields each run needed; do not design the final schema here.

## In scope

- A short probe brief: shot list of about 12 to 15 shots, shot acceptance threshold, budget, and the models to try.
- Exploratory look frames for Hercules, Copreus, the jar, the lion, and the throne room.
- A start frame per shot, then video, for the whole scene on at least two underlying models where their controls allow.
- Dialogue: one on-camera line with lip movement, one line of voice from inside the jar, and a decision on how voices will be produced.
- One moderation test of the violence the story needs, staged as fractured or implied imagery in clay (carried from G003 and G008).
- A rough cut of the scene with sound.

## Exclusions

- Approving any design, writing new story pages, building an asset library, and any shot outside this scene apart from the moderation test.

## Deliverables

- `05_generation/probe/brief.md`
- `05_generation/probe/runs.yaml` (one record per run: inputs, prompt, model and version, controls, cost, result, verdict, failure reason)
- `06_generations/probe/` (raw outputs and selects, kept separate)
- `07_edit/probe/` (the rough cut)
- `05_generation/capability_sheet.md`

## Acceptance criteria

- [ ] The acceptance threshold and credit budget were recorded before the first generation.
- [ ] Every planned shot has at least one attempt, and every run is logged with its inputs, model, cost, and verdict.
- [ ] The scene is assembled into a rough cut with sound, or the sheet states exactly which shots could not be made and why.
- [ ] The capability sheet rates each of these as cheap, expensive, or not currently possible, with the runs that support the rating: clay surface and stepped motion; identity across shots and across a reverse angle; two characters in one frame; on-camera dialogue; off-camera voice; weight and contact (the lion drop); a small crowd; an insert; shot length limits; start-frame versus start-and-end-frame control.
- [ ] The sheet reports takes per accepted shot and cost per accepted second, and extrapolates both to a 3–5 minute short and to a feature.
- [ ] The moderation test result is recorded.
- [ ] The sheet ends with writing guidance: what to lean on, what to ration, and what to avoid.
- [ ] The sheet lists the record fields the runs actually needed, as input to the G013 schema freeze.

## Expected verification evidence

- Run log parsed and counted by script (attempts, accepts, cost totals).
- Playback of the rough cut by the user.
- Each sheet rating linked to run IDs.

## User decisions needed

- Provider account and login, and the credit budget for this probe.
- The shot acceptance threshold (what counts as "good enough to keep").

## Carried findings

- From `platforms/HIGGSFIELD.md`: Hero-Frame-first versus direct text-to-video, single-shot versus multi-shot, and one versus several reference Elements are worth comparing here where budget allows. The rest of that comparison list belongs to G013.
- From calibration notes on this scene: the king counting on his fingers cannot be seen from inside the jar, and "the court steps back all at once" implies an unconstrained crowd. Stage three or four named courtiers.
