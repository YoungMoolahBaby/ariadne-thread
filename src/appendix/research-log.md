# Research log

What was searched, when, and what came of it, so later passes can pick up where earlier ones stopped. Newest first.

## 2026-11-10 · Pass 1: founding the notebook

**Scope.** Two parallel literature passes plus a first brainstorm.

**Pass 1a: VR, HCI and psychology.** Verified citations (with DOIs) for exiting VR, transitions between realities, reality awareness, dissociation and aftereffects, long exposure, game transfer, presence, time, memory source confusion, wayfinding and redirection, dreams, simulator sickness and ethics.

Corrections made to citations written from memory:

- The breadcrumb-trail paper is **Darken & Sibert (1993, UIST)**, not their 1996 CHI paper, which uses grids and maps.
- **Nordahl et al. (2019)** is a workshop paper with no DOI, not a journal article.
- The term *breaks in presence* is best cited to **Garau et al. (2008)**; Slater & Steed (2000) count virtual-to-real transitions.
- The gradual-transition presence result is **Steinicke et al. (2009, IEEE VR)**; the 2010 *Computers & Graphics* paper is the journal synthesis.
- Simulator waiting periods are cited to **Johnson (2005)**, ARI Research Report 1832, read in full; the 1987 Navy field manual could not be opened.

Most useful new finds: Bajorunaite et al. (2023) "Reality Anchors"; Bonnail et al. (2024) memory source confusion; Cheymol & Lopes (2025) hand and memory drift after leaving VR; Gottsacker et al. (2024) cognitive residue; Piumsomboon et al. (2022) Ex-Cit XR; Porter & Robb (2022) lingering effects; Auda et al. (2023) cross-reality survey; Konkoly et al. (2021) two-way dialogue with dreamers.

Searched for and **not found**:

- empirical studies of nested VR ("VR within VR") or of fake exits;
- studies of whether people can tell real from rendered in high-fidelity passthrough mixed reality (the "visual Turing test" is a stated industry goal, not a published result);
- peer-reviewed work on dissociation specifically in social VR (one 2022 master's thesis, Taveira, Lisbon, N=358, unverified as peer-reviewed).

**Pass 1b: other fields and products.** Verified cave-diving marker conventions (arrows, cookies, REMs), UK and US firefighter guideline conventions, the US mine lifeline regulation, desert-ant path integration, trusted path and Ctrl+Alt+Del, the line of death, picture-in-picture phishing, VM detection, measured boot, shadow stacks, VR/AR UI security research, headset reserved controls (Apple, Meta, Valve), ICU reorientation, psychedelic-research safety, flotation, spaceflight re-adaptation and the state of sensory brain interfaces.

Most important find: **Yang et al. (2024), "Inception Attacks"**: a fake exit on Meta Quest fooled 26 of 27 participants. This turned the hostile-content threat from argument into evidence and sharpened [H1](../brainstorm/ideas-hardware.md#h1-the-arch): reserving the button is not enough, the *response* must be unspoofable too.

Flagged as uncertain:

- the exact UK guideline tab geometry (in brigade training notes; only student flashcards found);
- the origin of "lights" in Exley's list of accident causes (sources disagree);
- whether the Hosfelt et al. (2020) preprint was formally published;
- Orion results (company release only) and an unconfirmed October 2026 claim of a first Neuralink Blindsight participant;
- no published re-entry protocol was found for flotation tanks.

Book chapters and the bibliography were written from both passes; earlier text written from memory was corrected where they disagreed.

## Next passes (to do)

- Standards and regulation: any requirement for a guaranteed exit (IEEE, ISO, OpenXR, consumer-protection rules on dark patterns, store policies). See [ethics](../research/ethics.md).
- Practical exit procedures in military, medical and industrial simulation that never reached academic VR research.
- Folk practice in heavy-use communities (social VR, sim racing, flight sim) for how people re-orient after long sessions.
- Standards for declaring nested layers to the platform (an OpenXR extension proposal?).
