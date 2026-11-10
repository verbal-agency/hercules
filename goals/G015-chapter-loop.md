# G015 — Chapter Production Loop and Handoff

Status: Pending

Provisional specification. Rewrite it from the G013 slice report and the G014 lock list before activation; do not treat the detail below as settled.

## Objective

Take each locked chapter through the slice validated in G013, in lock-list order, and deliver a handoff index for the whole film.

## Dependencies

G013 and G014.

## Project scenarios advanced

PS-03, PS-04, PS-05, PS-06, PS-07, PS-08.

## Constraints

- One chapter is the unit of work and the unit of a cycle slice.
- Use schema v1; a schema change is an architecture decision and is validated on the next chapter.
- Resolve new asset needs canonically through the breakdown, never inside an isolated prompt.
- A chapter that the reel has not locked is not produced.

## Per-chapter checklist

1. Lock the pages (Tier 1 on every scene, Tier 2 on key scenes, user approval).
2. Run the breakdown and extend the asset manifest and style rules for what is new.
3. Package scenes and shots; validate.
4. Generate, select, cut with sound.
5. Show the cut to viewers; record and answer notes.
6. Replace the chapter's reel section with the cut and re-watch the joins with its neighbours.
7. Update cost and take rates.

## Acceptance criteria

- [ ] Every chapter on the lock list has completed the checklist, or is recorded as cut or deferred by the user.
- [ ] Every shot validates and is traceable from page to source output.
- [ ] Every continuity state has a valid predecessor in story time or an explicit establishing event.
- [ ] The assembled film plays end to end, with placeholder, reel, and generated media visibly distinguished.
- [ ] A handoff index lets a fresh collaborator locate every authoritative artifact, and unresolved issues sit in a risk register or the backlog.

## Carried findings

- From G009 and G010: provider-side edits that affect canon are reconciled into repository versions before dependent shots proceed; the assembled film must never be presented as final while placeholders remain.
