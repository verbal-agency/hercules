# Roadmap

Goals are executed in order unless a documented dependency or user decision requires reprioritization. Exactly one goal is active during a cycle.

| Goal | Title | Depends on | Status | Primary outcome |
|---|---|---|---|---|
| G001 | Production foundation and cycle roadmap | — | Complete | Project charter, architecture, scenarios, roadmap, and cycle package |
| G002 | Mythology canon and adaptation decisions | G001 | Complete | Traceable source corpus, variant matrix, and approved story boundaries |
| G003 | Feature treatment and story architecture | G002 | Ready | Character arcs, sequence treatment, beat sheet, and scene inventory |
| G004 | Claymation visual language | G003 | Pending | Model-neutral style, material, optical, lighting, camera, grade, and tone rules |
| G005 | Screenplay draft one | G003, G004 | Pending | Complete readable feature screenplay and synchronized scene index |
| G006 | Canonical visual asset library | G004, G005 | Pending | Approved core designs, Hero Frames, location locks, Elements-ready derivatives, and continuity states |
| G007 | Scene/shot generation system | G005, G006 | Pending | Scene inheritance, asset bindings, Higgsfield adapter, capability routing, and prompt compilation |
| G008 | Representative sequence pilot | G007 | Pending | Pilot validating Higgsfield workflow, model routing, continuity, claymation language, metadata, and cost |
| G009 | Full generation-ready production package | G008 | Pending | Every generated scene and shot packaged with validated assets and continuity |
| G010 | Animatic and production handoff | G009 | Pending | Timed feature animatic, coverage report, risk register, and production plan |

## Sequencing rationale

- G002 fixes what story is being adapted before dramatic structure is expanded.
- G003 fixes the feature architecture before expensive visual exploration.
- G004 establishes visual constraints early enough to inform screenplay action.
- G005 creates the standalone dramatic document before full asset and shot expansion.
- G006 establishes one visual canon before prompts proliferate.
- G007 tests scene inheritance, shot overrides, asset bindings, and model compilation before generation begins.
- G008 uses one difficult representative sequence to expose failures cheaply.
- G009 scales only the validated system.
- G010 measures the whole film in time before final production.

Detailed, cycle-ready specifications are stored in [`goals/`](goals/). Future goals may receive findings from earlier cycles, but material roadmap changes require user approval.
