---
name: review-hercules-script
description: Run the Hercules story review panel on a scene, sequence, synopsis, beat sheet, or draft. Use when checking story or writing quality at story, sequence, or scene level, when estimating whether the work is functional and enjoyable, or when a goal's acceptance criteria call for a review checkpoint.
---

# Review Hercules script

Applies `02_story/review_rubric.md`. Read it first. Reviews inform the user's decisions and never approve anything. Panel output is model-generated, tends to flatter, converge, and pad, and has been calibrated on one scene pair and one synopsis run (`02_story/reviews/`).

## Choose the level and the tier

1. **Level** decides the lenses: story (reel, chapter list, synopsis), sequence, or scene. Prefer reviewing pages and reels. A synopsis-only panel is poor value (the first cost about 313,000 tokens for fourteen lines); run one only when the user asks. Do not use scene lenses on a synopsis or the reverse. See the rubric table.
2. **Tier** decides the cost. A reviewer call costs about 60,000 tokens of fixed overhead.
   - Tier 0: scripts only (IDs, scene card present, runtime sums, banned terms in opening movements). Run on every edit.
   - Tier 1: two reviewers per scene (cold reader plus one auditor). Batch several scenes into one call at sequence level.
   - Tier 2: full panel. Key scenes, any Tier 1 flag, each locked chapter, each reel version.
   - Tier 3: people. A read or listen of chosen pages (G012), viewers of each reel version (G014), viewers of each chapter cut (G013, G015).

## Protocol

1. **Prepare inputs.** Reviewers receive only the pages under review, inline in the prompt. Cold readers receive no canon. The boundary auditor receives only the boundary rules, quoted from the decision log. Intentions are never given to auditors (see rubric: boundaries and intentions).
2. **Run each lens in its own isolated subagent.** Tell each: use only the text provided; no tools, no file reads, no lookups. Do not say which version is the draft under test or what the writer hopes to see.
3. **Require evidence.** Every finding quotes the page (15 words or fewer), praise included.
4. **Use this output format** for every lens:

   ```text
   VERDICT: Pass / Fix / Fail (for your lens only)
   FINDINGS: up to 5, each: [High|Med|Low] "quote" - problem - suggested direction
             (fewer is fine; "none" is acceptable)
   WHAT WORKS: up to 3, each with a quote
   OPEN QUESTION: one thing you still want to know
   Max 300-450 words.
   ```

5. **Synthesize, do not average.** Report a verdict table, findings shared by several lenses, disagreements, and what worked. Never gate on a vote or a mean.
6. **Verify reviewer claims** about the myth or canon against `01_research/` before treating them as findings. In calibration, three reviewers wrongly flagged "twelve years" against "ten labors"; Apollodorus gives both.
7. **Discount by medium.** A synopsis states its own meaning; do not over-weight heavy-hand findings that point only at the synopsis's explanatory voice.
8. **Resolve each finding** as fixed, rejected with reason, or routed to a named goal. Taste questions go to the user.
9. **Record** the review under `02_story/reviews/` with panel composition, pages reviewed, reviewer prompts, token cost, findings, disagreements, and resolution status.

## Preambles

- **Scene:** "You are one reviewer on a panel evaluating a short scene from an unproduced adult dark-comedy claymation feature about Hercules. Use ONLY the scene text below. Do not use any tools, read any files, or look anything up. Every finding must quote the page (15 words max per quote). Be direct; if something works, say why briefly."
- **Story:** same, with "a synopsis (not a screenplay)" and add: "A synopsis cannot show whether dialogue is good, so judge only shape, promise, and the story's pull."

## Scene lenses

- **Cold audience (functional and enjoyable).** You know nothing about the project. Report (a) in two sentences what you think is happening and who each character is (retell); (b) any confusion or drift; (c) your prediction of the next scene; (d) engagement 1 to 5; (e) lines where you smiled, winced, or felt something, with a quote and the kind of feeling; (f) would you skip this scene on a second viewing; (g) the most alive moment and the deadest moment.
- **Story analyst.** State the scene's purpose, entering condition, turn, and exit. Test: turn, want and obstacle, delete (what later scene breaks if this is cut), exposition (a line whose main job is telling the audience what both speakers know), and blind voice.
- **Comedy punch-up writer.** Identify the comic engine. Mark each line meant to be funny and say whether it lands. Flag flat stretches and any joke at the expense of a victim, grief, or someone powerless. Suggest at most two punch-up directions from character, not added quips.
- **Claymation production reader.** The film is handcrafted clay stop-motion. Describe the scene as silent action in 3 to 5 sentences using only what the page shows physically, and name the principal physical event or say there is none. Flag what is hard to stage in clay and what the medium does especially well.
- **Tone reader.** The intended register is dark comedy with real consequence: humor from the powerful and the procedural; grief, victims, and the dead never the butt of a joke. Judge only tone.
- **Boundary auditor.** Given the quoted boundary rules, report each violation or risk with a quote and rule number. Do not score how well the scene "expresses" any rule. Also list conflicts with common mythology (to be verified, step 6).
- **Heavy-hand detector.** Does anything announce its own meaning? Is a motif explained instead of felt? Is a mechanism repeated until it is formula? Does the text tell the audience how to feel? Would a specific human detail do more than the stated theme? For each, say whether to cut the explanation, dramatize it, or leave it implicit.
- **Pairwise reader** (use when revising, and whenever a goal offers the user variants: run it before the user chooses, as input and not as the choice). Given versions A and B of a scene, choose one, quote why, and say what the other does better.
- **Stance variants** of the cold audience (rotate across scenes): a casual viewer who knows only the popular Hercules; a comedy fan; a myth reader; an animation fan; a skeptic.

## Story lenses

- **Cold pitch reader.** React as a viewer who has just been pitched this film: retell the story in three sentences; the chapter where interest peaked and where it sagged; chapters that felt like the same kind of scene; the final image you expect; would you buy a ticket (1 to 5) and why; anything you could not follow.
- **Story analyst (causality and premise).** For each adjacent pair of chapters say THEREFORE, BUT, or AND THEN. State the central dramatic question and whether the ending answers it; what the protagonist wants and needs and whether chapters pressure the gap; whether the premise pays off or is only stated; which chapter is cheapest and which most costly to cut.
- **Ledger keeper.** List every planted object, line, image, relationship, or thread and where it is paid off, dropped, or paid off without being planted. List threads that appear only in the running-threads section and no chapter carries.
- **Energy and variety rater.** Score each chapter 1 to 5 for expected pull, with tone and set-piece type in two words each. Flag flat runs of three, three chapters of the same shape, register whiplash, a weak third quarter, and an ending too quiet or too busy. State confidence.
- **Heavy-hand detector.** As above, applied to the synopsis, plus: does any chapter seem to exist to demonstrate a decision rather than because the story needs it?
- **Chronology reader** (when presentation order differs from story time). Reconstruct story time from presentation order and say where you were unsure.
- **Disclosure auditor.** After each chapter, state what the reader knows about the family catastrophe and compare with the disclosure map.

## Limits

- Never present a panel verdict as approval or as proof the writing is good or enjoyable.
- Reaction instruments are weakest for laughter and emotion. Collect human reactions on a few scenes and compare; discount the panel if they disagree.
- Before relying on the panel for subtle problems, calibrate again with subtle planted defects and a good-versus-better pair.
- People reading pages and watching the reel and the chapter cuts are the real tests.
