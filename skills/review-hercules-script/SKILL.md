---
name: review-hercules-script
description: Run the Hercules story review panel on a scene, sequence, beat sheet, or draft. Use when checking treatment, beat sheet, or screenplay quality at scene level or macro level, or when a goal's acceptance criteria call for a review checkpoint.
---

# Review Hercules script

Applies `02_story/review_rubric.md`. Read it first. Reviews inform the user's decisions; they never approve anything. Panel output is model-generated, tends to flatter and converge, and has been calibrated on one scene pair only (`02_story/reviews/calibration/calibration_results.md`).

## Protocol

1. **Choose scope and checkpoint** from the rubric: scene, sequence, beat sheet, or full draft.
2. **Prepare inputs.** Reviewers receive only the pages under review, inline in the prompt. Cold readers receive no canon. The canon auditor receives the text of the active decisions it must check (AD entries quoted, not summarized).
3. **Run each lens in its own isolated subagent.** Tell each: use only the text provided; no tools, no file reads, no lookups. Do not tell reviewers which version is the draft under test or what the writer hopes to see.
4. **Require evidence.** Every finding quotes the page (15 words or fewer). Praise must quote too.
5. **Use this output format** for every lens:

   ```text
   VERDICT: Pass / Fix / Fail (for your lens only)
   FINDINGS: up to 5, each: [High|Med|Low] "quote" - problem - suggested direction
             (fewer is fine; "none" is an acceptable answer)
   WHAT WORKS: up to 3, each with a quote
   OPEN QUESTION: one thing you still want to know
   Max 300 words.
   ```

6. **Synthesize, do not average.** Report a verdict table, findings that several lenses share, and disagreements. Keep disagreements visible.
7. **Check reviewer claims about myth and canon** against `01_research/` before treating them as findings. In calibration, three reviewers wrongly flagged "twelve years" against "ten labors"; Apollodorus gives both.
8. **Resolve each finding** as fixed, rejected with reason, or routed to a named goal. Taste questions go to the user.
9. **Record** the review under `02_story/reviews/` with panel composition, pages reviewed, reviewer prompts, findings, and resolutions.

## Scene lenses

Prompts below are the ones used in calibration. Prefix each with: "You are one reviewer on a panel evaluating a short scene from an unproduced adult dark-comedy claymation feature about Hercules. Use ONLY the scene text below. Do not use any tools, read any files, or look anything up. Every finding must quote the page (15 words max per quote). Be direct; if something works, say why briefly."

- **Cold audience.** You know nothing about the project. Report (a) in two sentences what you think is happening and who each character is; (b) any confusion or drift; (c) your prediction of the next scene; (d) engagement 1 to 5 and the one thing that most made you want to keep watching or stop.
- **Story analyst.** Infer and state the scene's purpose, entering condition, turn, and exit condition. Then test: turn, want and obstacle, delete (what later scene breaks if this is cut), exposition (any line whose main job is telling the audience what the speakers already know), and blind voice (cover the names; could you tell speakers apart?).
- **Comedy punch-up writer.** Identify the comic engine. Mark each line meant to be funny and say whether it lands. Flag flat stretches and any joke at the expense of a victim, grief, or someone powerless. Suggest at most two punch-up directions that come from character, not added quips.
- **Claymation production reader.** The film is handcrafted clay stop-motion. Describe the scene as silent action in 3 to 5 sentences using only what the page shows physically, and name the principal physical event (or say there is none). Flag anything hard to stage in clay (unconstrained crowds, continuous transformations, invisible thoughts, unspecified effects) and anything the medium does especially well.
- **Tone reader.** The intended register is dark comedy with real consequence: humor comes from the powerful and the procedural; grief, victims, and the dead are never the butt of a joke. Judge only tone: does any line cheapen grief or harm; does the register stay consistent with the stakes or collapse into farce or lecture; does the scene tell you how to feel or let you; is the powerful character both funny and dangerous.
- **Canon auditor.** Given the quoted active decisions, report each violation or risk with a quote and a rule number, and list conflicts with common mythology the rules do not cover (to be verified, see step 7).
- **Myth-literate viewer** (optional). Does this feel like Hercules? Where does it depart from the traditions, and does the departure earn its place?
- **Skeptic** (optional). What would make me stop watching?

## Macro lenses (beat sheet, sequence, full draft)

- **Cold reader, chronology.** Read the scenes in presentation order. Reconstruct story-time order and state where you were unsure.
- **Story analyst, causality.** For each adjacent pair of beats, state whether the link is "therefore", "but", or "and then".
- **Ledger keeper.** List every planted object, line, or thread and where it is paid off or dropped.
- **Energy rater.** Score each scene 1 to 5 for pull and tone, and flag runs of three or more flat scenes or three scenes with the same shape.
- **Premise reader.** Does the catch (a system that cannot be satisfied) pay off, and is the ending earned?
- **Disclosure auditor.** Compare what a cold reader knows after each scene about the family catastrophe with the disclosure map.

## Limits

- Never present a panel verdict as approval or as proof the writing is good.
- Before relying on the panel for subtle problems, calibrate it again with subtle planted defects and with a good-versus-better pair.
- Table reads with real people and the G010 animatic are the real tests.
