# Roadmap

The project advances in three loops rather than a single chain of gates:

1. **Capability** — measure what the generation models can actually do, and write to that.
2. **Story** — decide the story by choosing between written pages and by watching a reel, not by adding rules.
3. **Production** — take one locked chapter at a time through every layer, from pages to an edited cut.

Exactly one goal is active during a cycle.

| Goal | Title | Depends on | Status | Primary outcome |
|---|---|---|---|---|
| G001 | Production foundation and cycle roadmap | — | Complete | Project charter, architecture, scenarios, roadmap, and cycle package |
| G002 | Mythology canon and adaptation decisions | G001 | Complete | Traceable source corpus, variant matrix, and approved story boundaries |
| G011 | Capability probe: the jar scene | G002 | Ready | A generated one-minute scene, a measured capability sheet, and a cost per accepted second |
| G012 | Story spine and tentpole pages | G002 | Ready | One-page spine, one-page current canon, and five key scenes chosen from written variants |
| G013 | *Eurystheus* short: first vertical slice | G011, G012 | Pending | A finished 3–5 minute chapter-one short, and schemas frozen at v1 from real data |
| G014 | Feature story reel | G011, G012 | Pending | The whole film as a timed still-frame reel with temp voices, iterated with viewers |
| G015 | Chapter production loop and handoff | G013, G014 | Pending | Each locked chapter taken through the validated slice; final handoff index |

G003 to G010 were superseded before activation. Their files are kept in [`goals/superseded/`](goals/superseded/).

## Sequencing rationale

- G011 and G012 do not depend on each other. G011 is recommended first because its findings constrain what G012 writes, but G012 may go first if provider access is not ready.
- G011 tests the largest unknowns (clay look, identity hold, dialogue, moderation, cost) on one minute of film before any screenplay or asset library depends on them.
- G012 settles the open story questions by putting alternatives on the page for the user to choose between.
- G013 proves the whole pipeline on one chapter and yields a watchable, pitchable short. Schemas are frozen only here, from what the slice needed.
- G014 tests the whole story in time at the cheapest possible resolution, before chapters two onward are produced.
- G015 scales only what G013 validated, one chapter at a time, in the order the reel locks them.

## Roadmap revision (2026-11-10, user-approved)

**What changed.** G003 to G010 (treatment, visual language, screenplay, asset library, shot system, pilot, full package, animatic) are replaced by G011 to G015.

**Why.**

- The earlier order first touched generation at G008 and first measured the story in time at G010. Both tests now come first.
- Story direction was being set by decisions written ahead of pages. The material reviewers responded to (the jar, the thumbprint, "Good morning, old friend") came from writing a scene.
- G003's acceptance criteria turned intentions into gates, which the review rubric itself warns against.
- The scene and shot schemas were specified before any generation and lacked dialogue, voice, and performance fields.

**What carries over.** The project scenarios in `PROJECT.md`, the three-layer separation in `ARCHITECTURE.md`, the adaptation decision log, the review rubric, and the provider profile all remain in force. Constraints from the superseded goals are carried into the new goals where they still apply; each new goal names its sources.

**What this reverses.** The earlier decision to defer Higgsfield account creation and paid experimentation until approved assets existed (recorded in G002 and the superseded G008). G011 needs provider access and a small approved credit budget before any canonical asset exists. Its outputs are exploratory and approve nothing.

Detailed, cycle-ready specifications are stored in [`goals/`](goals/). Material roadmap changes require user approval.
