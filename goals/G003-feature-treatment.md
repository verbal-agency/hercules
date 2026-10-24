# G003 — Feature Treatment and Story Architecture

Status: Ready

## Objective

Turn the approved canon into a complete feature architecture with character arcs, sequence treatment, beat sheet, and stable scene inventory.

## Dependencies

G002.

## Project scenarios advanced

PS-01, PS-02, PS-07.

## Constraints

- Follow approved adaptation decisions or record a superseding decision.
- Use stable scene IDs.
- Keep generation prompts and final visual design out of story documents.
- Target an adult R-rated dark comedy with visible consequence (AD-033); clay stylization cannot substitute for dramatic consequence.
- Build a recurring Olympus plotline, an evolving nightmare motif, and a pre-Labor-11 Prometheus setup without allowing any of them to become detachable exposition.
- Carry physical, relational, political, and divine state across Labor transitions so the world never resets between episodes.
- Use selectively nonlinear presentation while keeping story chronology and causality reconstructable. Favor simultaneity (distant figures woven into ordinary scenes) over flashback; every true displacement needs a visible in-story hinge and a named payoff (AD-031, AD-035). The degree of nonlinearity is an open question below.
- Rotate sequence agency and transition ownership across the ensemble and world; do not use a repeated return/assignment/Labor/nightmare loop.
- Open mid-service, not at the family's life or the madness; the catastrophe is withheld and alluded to, then presented in full at a deliberate point (AD-032).
- The gods are careless, may comment to the audience in partial and sometimes wrong ways, are not strictly invisible to mortals, and are never an exposition channel (AD-034). Hera is aghast, not remorseful, when the family's deaths play out.
- Hercules is messy, not moralized: no required improvement arc, no lesson that cancels earlier harm (AD-036).
- Every sequence leads with a physical event that carries its meaning and could be followed with the sound off; comedy arises from character and situation, not assigned rules (AD-033).

## In scope

- Logline, theme, dramatic question, mortal and divine character arcs or deliberate non-arcs (AD-036), a chapter plan (chapters named for the people who own them), a disclosure map for the family catastrophe, a hinge map for every displacement, an ambient-thread layer (clocks such as the eagle, the sky, and the ledger), a decision or deferral for each open story question, sequence treatment, pacing targets, beat sheet with separate story and presentation order, scene inventory, ensemble-agency map, transition-owner map, nightmare progression, Olympus progression, staged purpose revelations, and later-film boundary.

## Exclusions

- Screenplay dialogue, final designs, shot lists, and generation prompts.

## Deliverables

- `02_story/story_principles.md`
- `02_story/characters.md`
- `02_story/treatment.md`
- `02_story/beat_sheet.md`
- `02_story/disclosure_and_hinge_map.md`
- `02_story/scene_index.yaml` (with hinge-in, hinge-out, chapter owner, and ambient-thread fields)

## Acceptance criteria

- [ ] The treatment covers the feature from opening image through final image.
- [ ] Every sequence advances the feature's external conflict and at least one defined mortal or divine character arc or deliberate non-arc; Hercules remains the protagonist without being the sole source of agency and without a required moral-improvement arc (AD-036).
- [ ] All twelve Labors are classified as full sequence, compressed scene, montage beat, or omitted reference.
- [ ] Olympus and the mortal world causally interpenetrate: every divine scene changes mortal pressure or audience understanding, mortal outcomes provoke divine response, and Hera's campaign from the cradle onward is progressively exposed.
- [ ] Nightmare and waking-memory beats evolve (AD-025) without implying moral improvement (AD-036) and never turn Megara into a forgiving ghost.
- [ ] The feature opens mid-service with no scene of the family's life or the madness in the opening movements, and the disclosure map lists every allusion (who asks, what is withheld, what is learned) and the point of full presentation (AD-032).
- [ ] Every displacement in story time has a hinge visible within the story (line, object, animal, contradiction, character exit or entrance, or divine guide) and a named payoff; simultaneity is used where displacement is not needed (AD-035).
- [ ] Divine commentary is partial and biased, Zeus remains visibly passive, Hera's aghast exit is not remorse, and no Olympus scene is detachable exposition (AD-034, AD-026).
- [ ] Each sequence names its principal physical event and passes a sound-off clarity read.
- [ ] Every open story question below is decided, or explicitly deferred with a rationale and an owning goal.
- [ ] No nightmare functions as automatic post-Labor punctuation; every full nightmare or intrusion produces a dramatic turn in the scene where it appears.
- [ ] Prometheus is seen suffering before Labor 11 and his eventual release pays off the setup.
- [ ] The legal, political, divine, civic, and personal purposes of the Labors are planted and revised at multiple structural turns.
- [ ] Every Labor transition carries at least one persistent consequence, relationship, object, wound, reputation change, or divine action into the next movement.
- [ ] Labor movements are introduced or reframed through varied agents and mechanisms—including supporting characters, antagonists, gods, threatened communities, creatures, places, objects, or unanswered questions—rather than repeated court assignments.
- [ ] Every nonlinear displacement earns suspense, dramatic irony, thematic collision, or recontextualization, and the consequential chronology is reconstructable by the final act.
- [ ] Every scene index entry has a unique ID, presentation order, story-time anchor, viewpoint or transition owner, causal predecessors, location, characters, purpose, and estimated duration.
- [ ] Total estimated duration is within the approved range or a deviation is approved.
- [ ] Every original invention is traceable to the G002 decision log.
- [ ] The treatment is understandable without visual assets or prompts.

## Expected verification evidence

- Duration sum from the scene index.
- Beat-to-scene and character-arc coverage review.
- Source/invention traceability check for every sequence.
- Olympus/mortal causal-interpenetration and Hera-campaign progression review.
- Nightmare-evolution and Labor-purpose-revelation coverage review.
- Transition-state check across all twelve Labors.
- Story-time versus presentation-order reconstruction check.
- Sequence-agency and transition-owner review confirming that the supporting cast and world actively propel the plot.
- Disclosure-map and hinge-map review, including a first-read test of the opening movements.
- Open-question log showing each decision or deferral.
- Sound-off read of every sequence.

## Carried findings (from pre-G003 evaluation)

- Per AD-032, open mid-service with the family catastrophe withheld. G003 must include a disclosure map listing each allusion (who asks, what is withheld, what the audience learns) and the point of full presentation. Hercules's capacity for dangerous rage should still be established before that point (Linus remains mention-only).
- Theseus must be seeded before Labor 12 (AD-013); place the seed explicitly in the beat sheet.
- Run an early reader test on the nonlinear beat sheet (story-time versus presentation order) before drafting treatment prose.
- Estimate per-sequence durations early; twelve Labors plus Olympus and nightmares must fit 105–115 minutes.
- Provider moderation of violent imagery is untested; route to G008. Prefer staging that works as implied or fractured imagery, and test early with a claymation-framed sample.
- AD-033 to AD-035 also govern this goal: dark-comedy tone, careless documentary gods who are not strictly invisible, and a simultaneous world (recurring dawns, eagle as clock) in which any true displacement needs a visible hinge and a named payoff. Add a hinge map and an ambient-thread layer to the scene index.

## Open story questions (unresolved; decide during development)

Working direction: chapters named for people in the manner of Catch-22 (Eurystheus as the goalpost-moving bureaucracy; the family event returning in changing fragments; physical set pieces leading; jokes arising from character; the Labors as ensemble chapters). Hercules is messy, not moralized (AD-036). `02_story/outline_draft.md` (v4) predates this direction.

- **Gods' consequence:** an act (Hercules wounds Hera, per Iliad 5.392ff), an enforced witness (Hera cannot walk out), an ensemble job on Olympus, or fallout that arrives unforced. Undecided; do not force a payoff.
- **The "thirteenth line":** the king overreaching past Delphi's mandate (verify "twelve years" in SRC_A01 2.4.12), the restored-house task, or Hercules's own act afterward. Not a canonical Labor; any version is a labeled invention (AD-021).
- **Placement of the full family telling:** center (about 55%) or late (about 70%).
- **Degree of nonlinearity:** currently a retreat from AD-031's braid; confirm or restore.
- **Documentary frame:** reduced to occasional godly commentary; confirm.
- **Hermes narrating:** undecided. **Zeus's presence in the Megara chapter:** undecided.
- **Iolaus:** needs an arc and a clear exit and return across the chapters.
- **Running legend:** the inflating story of Hercules needs placements and a payoff.
- **Sources to add to the corpus before relying on them:** Hesiod, *Theogony* (Mecone sacrifice); Homer, *Iliad* 5.392ff (Hercules wounds Hera and Hades); Aeschylus, *Prometheus Bound*; Apollodorus 2.4.12 (length of service).
