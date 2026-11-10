---
name: develop-hercules-screenplay
description: Develop the Hercules claymation feature from mythology research through canon, treatment, Fountain screenplay, scene packages, shot plans, prompts, and visual-reference requirements. Use when outlining, writing, revising, breaking down, or continuity-checking this project's story or screenplay and its production handoff.
---

# Develop Hercules Screenplay

Preserve the separation between story, visual canon, and generation defined in `ARCHITECTURE.md`. Advance only the active Cycle goal unless the user explicitly broadens scope.

## Source order

1. Read `PROJECT.md`, `ROADMAP.md`, `goals/ACTIVE.md`, and the active goal.
2. Read completed upstream artifacts named by that goal. When they exist, read `02_story/spine.md`, `02_story/canon_now.md`, and `05_generation/capability_sheet.md` before writing anything; write from the spine and the scene card, and to what the sheet says the models can do.
3. For mythology claims, prefer primary ancient sources and reputable scholarly translations or reference works. Record variants; do not silently merge incompatible traditions.
4. Treat approved project canon as binding after the canon goal closes. Route later discoveries to the backlog unless they invalidate acceptance criteria.

## Story workflow

1. Define the dramatic question, Hercules's want/need, opposing force, moral cost, and final image on one page (the spine). Whether he transforms is a story choice (AD-036), but he must want something the story pressures.
2. Select myths because they advance that arc, not merely because they are famous.
3. Decide structure by writing key scenes in two or three genuinely different variants for the user to choose between, then by cutting a still-frame reel with temp voices and watching it. Do not write a long treatment ahead of pages.
4. Draft in Fountain, following "Writing a scene" below. Keep action filmable, present-tense, and specific; reveal interior change through behavior, choice, image, and dialogue.
5. Maintain scene IDs that survive revision. For every scene, state dramatic purpose, entering condition, turn, exit condition, cast, location, time, continuity state, and required visual assets.
6. When a chapter is locked, run a breakdown before designing anything: an entity-by-state matrix (characters, creatures, locations, props, costumes, damage states, by scene) and the asset demand list it implies. Each new state is a cost; cut or merge states the story does not need.
7. Break approved scenes into shots only after scene intent stabilizes. Every shot must have one editorial purpose and one principal visual change.
8. Pair every shot with asset bindings, a Hero Frame requirement, dialogue or audio, shot class, camera/blocking data, duration target, motion prompt, exclusions, and continuity endpoints.

## Writing a scene

A model left alone writes toward the average: tidy turns, lines that state the theme, one voice for everyone. Each step below exists to push against that.

### What the writer is given

A writing pass receives only: the spine, the scene card, the voice sheets for the characters present, the capability sheet's writing guidance, the taste file, the ledger entries the scene touches, and the pages immediately before it. It does not receive the decision log, goal files, review lenses, or reviewer questions. When drafting through a subagent, put exactly these inline and tell it to use nothing else.

### Standing documents

- **Voice sheets** (`02_story/voices/<character>.md`). Made of lines, not adjectives: ten to fifteen sample lines in the character's mouth, what they never say, what they want in any room, and how they behave when they are losing. A sheet is ready when a cold reader can pick the character's lines out of an unlabeled mix.
- **Taste file** (`02_story/taste.md`). Lines and moments the user loved or rejected, quoted, dated, with the user's reason in their own words. Append whenever the user reacts to a page. Record the reaction; never rewrite it into a rule. Writers get it as examples.
- **Ledger** (`02_story/ledger.yaml`). After each locked scene: who knows what, what was planted and where it pays off, and the state of props, costumes, wounds, and relationships at exit. Check it by script for payoffs with no plant, plants with no payoff, and state that changes with no scene to change it.

### Steps

1. **Mine the sources.** Before writing, pull a handful of odd, concrete specifics for this scene from `01_research/` and the cited ancient texts and objects: a gesture, an object, a procedural detail, a contradiction between tellings. The jar and the eagle came from there. Label anything invented (AD-021).
2. **Takes before drafts.** Produce five to eight one-paragraph takes, each from an isolated writer with a different brief: whose scene it is, what the principal physical event is, what the comic engine is, where it starts. Takes must differ in approach, not wording. The user picks two or three to draft.
3. **Silent pass.** Write the scene as action only. It must be followable with the sound off and built from actions that decompose into short shots.
4. **Dialogue pass.** Add speech from the voice sheets. People talk to get something from each other, not to inform the audience.
5. **Cut pass.** Remove about a fifth. Cut every line that states the scene's meaning, every repeated joke, and anything the silent pass already shows.
6. **Punch-up pass.** At most two changes, each from character or situation. No added quips.
7. **Hear it.** Before review, produce a temp-voice read of the chosen variants, or have the user read them aloud. Comedy timing does not show on the page. If neither is possible, record that the pages were not heard.
8. **Review and choose.** Run the pairwise reader and Tier 1 (`skills/review-hercules-script/SKILL.md`). The user chooses. Record the choice and append their reactions to the taste file.
9. **Lock.** Update the ledger and re-run its checks.

### Pages that compile

So that the breakdown can be produced by a parser rather than by rereading:

- Each scene heading carries its stable ID as a Fountain scene number: `INT. TIRYNS - THRONE ROOM - DAY #SC_010_JAR#`.
- Characters, creatures, and significant props are capitalized on first appearance in a scene, with one consistent name each.
- A change of costume, damage, or prop ownership is written as a visible action, never assumed.
- The scene card lives beside the page as `<page>.card.yaml` (purpose, entering condition, turn, exit condition, principal physical event, engine, cast, location, story-time anchor). The page itself stays free of production metadata (PS-02).

## Claymation constraints

- The capability sheet outranks this list wherever they differ: it records what was measured, and this list is the starting assumption.
- Write for tangible sets, puppets, replacement faces, rigs, miniature scale, tactile clay surfaces, and deliberate stepped motion.
- Favor readable silhouettes, motivated staging, and actions that can be decomposed into short clips.
- Track costume, damage, prop ownership, scale, geography, light direction, and entrance/exit states.
- Avoid prose that depends on invisible thoughts, unconstrained crowds, or continuous transformations without a planned technique.

## Production handoff gate

A scene is not generation-ready until its dramatic function is approved and all shots resolve to versioned canonical assets. A shot is not generation-ready until its start state, end state, Hero Frame, principal motion, camera behavior, duration, and provider-neutral prompt are explicit.

Do not embed provider syntax in the screenplay. Compile it later through the relevant platform skill.
