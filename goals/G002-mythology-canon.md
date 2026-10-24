# G002 — Mythology Canon and Adaptation Decisions

Status: Complete

## Objective

Create a traceable research corpus and approve the mythological chronology, included episodes, variant policy, names, tone boundary, and invention policy for the feature.

## Completed dependencies

G001.

## Project scenarios advanced

PS-01, PS-06, PS-07.

## Architecture constraints

- Separate ancient testimony, later interpretation, inference, and original invention.
- Record provenance and rights status for visual sources.
- Do not write screenplay scenes or approve visual designs in this goal.

## In scope

- Primary and reputable secondary sources for birth, madness, Labors, Theseus, and the later-life cycle.
- Source bibliography with stable reference IDs.
- Episode/variant matrix and adaptation decision log.
- Pronunciation and naming sheet.
- Boundaries for violence, divine agency, humor, and historical/visual period.

## Exclusions

- Full treatment, dialogue, screenplay pages, final character design, and generation prompts.

## Deliverables

- `01_research/sources.md`
- `01_research/variant_matrix.md`
- `01_research/adaptation_decisions.md`
- `01_research/names_and_pronunciation.md`
- `01_research/reference_manifest.yaml`

## Acceptance criteria

- [x] Every planned major beat has at least one ancient source or is labeled original invention.
- [x] Conflicting placement of the madness is documented and one chronology is approved with rationale.
- [x] All twelve Labors have selected narrative versions and material rejected variants documented.
- [x] The roles of Megara, Iolaus, Eurystheus, Hera, Athena, Theseus, and the gods are explicitly decided.
- [x] The first feature’s ending and boundary with the Deianeira cycle are approved.
- [x] Every external visual reference has PS-06 provenance fields, including unknown rights where necessary.
- [x] No treatment scenes, final visual assets, or model prompts are introduced.

## Expected verification evidence

- Automated link and manifest validation where feasible.
- Manual cross-check from every intended beat to a source or invention label.
- Decision-log review confirming no unresolved story-architecture ambiguity remains.

## Carried risks

- Ancient sources conflict and must not be flattened into a false canon.
- A family-audience versus adult tone decision materially changes the madness sequence and must be resolved here. (Resolved as PG-13 at close; superseded by AD-024, R rating.)

## Approved outcomes

The following records what G002 approved at cycle close. AD-024 through AD-030, listed in the post-completion section below, supersede its audience and divine-frame boundaries for current development.

- Pseudo-Apollodorus's pre-Labor madness chronology governs; Euripides's post-Labor chronology remains documented and informs aftermath and friendship, not event order.
- All twelve Labors remain canonical, with G003 authorized to classify their screen treatment by dramatic weight.
- ~~The film targets a family-accessible teen audience at an approximate PG-13 boundary, with non-graphic family violence and non-stigmatizing divine madness.~~ Superseded by AD-024 (R, visible consequence); non-stigmatizing divine madness (AD-017) still holds.
- Cerberus's return completes compulsory service; choosing continued life completes the feature's emotional arc.
- Deianeira, Nessus, Iole, the pyre, and apotheosis remain outside this feature.
- Greek cultural naming surrounds the audience-facing name `Hercules`.

## Verification evidence

- `01_research/sources.md` maps every intended major beat to a cited ancient passage or an explicit original-invention label.
- `01_research/variant_matrix.md` contains exactly twelve numbered Labor rows plus documented chronology and connected-episode alternatives.
- `01_research/adaptation_decisions.md` records 23 approved decisions covering chronology, character functions, ending, tone, divine agency, humor, period, and invention policy.
- `01_research/names_and_pronunciation.md` records the Greek/Roman naming boundary and working pronunciations.
- `01_research/reference_manifest.yaml` parses successfully as YAML and contains all required PS-06 fields for three external visual references; each institution labels its image public domain.
- Primary Theoi, Scaife, and Metropolitan Museum links were retrieved during research. Several Perseus catalog endpoints returned transient timeout/502 responses during bulk verification; stable work/passage identifiers are recorded so those access failures do not erase source traceability.
- Mechanical checks confirmed 12 Labor rows, 23 decision entries, source IDs `SRC_A01` through `SRC_A12`, valid YAML, and no whitespace errors.
- Manual scope review found no treatment, screenplay scene, final visual asset, generation prompt, or provider-dependent work.

## Routed findings

- The user's decision to defer a Higgsfield account until approved assets exist is routed to G008 as a provider-onboarding constraint; it does not alter G002 story canon.

## Post-completion canon amendments

On 2026-08-08 the user approved a new adult tone, expanded divine frame, and braided nonlinear structure after G002 closed. The historical verification above remains accurate for the completed cycle; current canon is amended by AD-024 through AD-031 in `01_research/adaptation_decisions.md`:

- target an R rating with visible, consequential violence;
- haunt Hercules through evolving nightmares and waking intrusions without a forgiving Megara ghost;
- use recurring Olympus scenes, on-screen Hera strategy, divine gossip, and a present but culpably passive Zeus;
- treat Hera's attacks from the birth-order trick and cradle onward as one campaign;
- unify every Labor through persistent mortal and divine consequences;
- reveal the Labors' competing purposes in stages and show Prometheus on his rock before Labor 11;
- let supporting characters, gods, creatures, and future Labor figures propel a selectively nonlinear presentation while preserving reconstructable causality.

These amendments refine the starting constraints for G003; they do not reopen the completed research cycle.
