# Hercules

Development workspace for a claymation adaptation of the traditional Hercules stories and the visual-reference system needed to generate consistent video.

The project has three linked but separate production layers:

1. **Story** — research, decisions, treatment, screenplay, and scenes.
2. **Visual canon** — approved characters, creatures, locations, props, materials, lighting, and continuity states.
3. **Generation** — inheritable scene and shot packages, asset bindings, and model adapters derived from the screenplay and visual canon.

Start with [PROJECT.md](PROJECT.md), [ARCHITECTURE.md](ARCHITECTURE.md), and [ROADMAP.md](ROADMAP.md). Cycle state and goal specifications live in [`goals/`](goals/).

Provider-specific production mappings live in [`platforms/`](platforms/). They implement the model-neutral architecture without becoming its source of truth. The first candidate profile is [Higgsfield](platforms/HIGGSFIELD.md).

## Cycle convention

When asked to **cycle**:

1. Read the project, architecture, roadmap, backlog, and `goals/ACTIVE.md`.
2. Activate the next ready goal if none is active and the user authorized a cycle.
3. Complete exactly that goal and verify each acceptance criterion.
4. Route discoveries to a named future goal or the backlog.
5. Mark it complete and prepare, but do not begin, the next eligible goal.
