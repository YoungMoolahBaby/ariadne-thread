# Leaving VR: transitions and re-entry

Leaving VR is a recognised research topic, but a young one. Most work studies short sessions and comfort; nobody has yet studied nested exits or fake exits (see [gaps](#gaps)).

## The experience of leaving

**Knibbe et al. (2018), "The Dream is Collapsing"**, is the founding study. Interviews about exiting VR found five dimensions to the experience: *space, control, sociality, time* and *sensory adaptation*. People felt spatially disoriented on leaving regardless of how complex the virtual scene was, and they described exiting **"mentally first, then physically"**: the decision to leave comes before the body catches up. The paper proposes six designs for better exits.

**Cheymol & Lopes (2025)** measured what lingers. After leaving VR, participants' hand movements stayed redirected by up to 7 cm, and they recalled where an object had been *in VR* instead of where it really was (in one task, reaching for the virtual fire extinguisher's location). The body and memory do not snap back on their own.

**Gottsacker et al. (2024)** found "spatial cognitive residue": spatial memory of one virtual environment carries over into the next. Transitions of one minute between environments reduced it.

**Horst et al. (2021/2024)** compared eight "outro" transitions back to the physical world after short experiences. People preferred non-interactive outros, except one in which they could talk to the presenter; a presenter-controlled stop felt unobtrusive.

**Piumsomboon et al. (2022), "Ex-Cit XR"**, asked eleven experts for ways to get people out of immersive environments and collected 132 techniques in six groups: activities, cues, breaks, degradations, notifications and virtual agents. Users preferred subtle, in-world cues over forced breaks, and the authors recommend **escalating from gentle to forceful**.

## Going in gradually

The entry side has a longer history, and its techniques can run in reverse.

- **Steinicke et al. (2009)** had people enter VR through a virtual replica of the real room. Subjective presence was higher than with a direct cut (physiological measures did not differ), and a companion study found better distance estimation. The journal version is **Steinicke et al. (2010)**.
- **Valkov & Flagge (2017)**, "Smooth immersion", made entry a continuous process and found raised awareness and possibly higher perceived interactivity.
- **Jung et al. (2018)**, "In Limbo", used a gradual phase between the real and virtual body and room; it affected body ownership and presence.
- **Husung & Langbehn (2019)** compared transitions between virtual scenes; portals and orbs did well.
- **Billinghurst et al. (2001)**, the *MagicBook*, is the classic "transitional interface": a physical book as the handle for moving between the real world, augmented reality and full VR.

## Transitions between realities as a field

- **Auda et al. (2023)**, a scoping survey of 306 papers on cross-reality systems, gives a taxonomy of transitions and nine guiding principles. The best single entry point to the field.
- **Pointecker et al. (2022)** found fades were preferred for frequent switching during work, and portals suited rare switches between very different realities.
- **Feld et al. (2024)** found users clearly preferred **brief, efficient transitions** over elaborate continuous ones in task-driven work.
- **Gottsacker et al. (2026)** compared interfaces for previewing and switching between several virtual worlds, the closest existing work to moving between many layers.

## What this means for the thread

1. **Disorientation on exit is normal, not a sign of a bad app.** Knibbe found it regardless of scene complexity. A thread is not an edge-case feature.
2. **The mind leaves before the body.** The exit decision is the first step, so the exit control ([H1](../brainstorm/ideas-hardware.md#h1-the-arch)) matters, and the body needs its own re-calibration afterwards.
3. **Re-calibration has measurable targets.** Cheymol & Lopes give two: reach accuracy and memory of where real things are. Both make good measures for the [airlock prototype](../brainstorm/prototypes.md#2-the-airlock).
4. **There is a tension in the airlock's length.** People prefer short transitions (Feld 2024), but clearing residue took about a minute (Gottsacker 2024). A reasonable design: short by default, longer after long or deep sessions, never mandatory in an emergency.
5. **Escalation is the right shape for reminders.** Ex-Cit XR's gentle-to-forceful finding matches the [dead man's switch](../brainstorm/ideas-hardware.md#h6-dead-mans-switch).

## Gaps

This pass found no empirical HCI study of:

- exiting **nested** environments (VR inside VR), or how people experience **fake exits** (security research has demonstrated a fake exit as an attack: Yang et al. 2024, see [what headsets ship today](products.md); but not how people recover from one);
- whether people can tell real from rendered in high-fidelity passthrough mixed reality;
- exits after **very long** or habitual sessions in the home.

These are open, and each is a candidate study (see [open questions](../brainstorm/open-questions.md)).
