# Comparing the ideas

A first-pass rating of every idea against the [five threats](../problem/threat-models.md). These are judgements to argue with, not measurements. Change them when evidence arrives, and log why in the [research log](../appendix/research-log.md).

**Legend:** ● strong · ◐ some · ○ little or none. *Presence cost* is how much the idea intrudes while you are not using it.

| ID | Idea | Job | Drift | Careless | Captivating | Hostile | Own mind | Presence cost | Today |
|---|---|---|:-:|:-:|:-:|:-:|:-:|---|---|
| H1 | The Arch | extract | ◐ | ● | ● | ● | ○ | low | partly |
| H2 | Real light | verify, extract | ◐ | ● | ○ | ● | ○ | medium | partly |
| H3 | The tether | guide, extract | ● | ◐ | ○ | ◐ | ◐ | medium | yes |
| H4 | Reality heartbeat | verify | ● | ◐ | ◐ | ● | ◐ | low | buildable |
| H5 | Depth gauge | guide, verify | ● | ◐ | ○ | ◐ | ◐ | low | PC |
| H6 | Dead man's switch | extract | ● | ◐ | ● | ◐ | ● | medium | buildable |
| H7 | Black box | guide, verify | ◐ | ◐ | ○ | ◐ | ○ | none | buildable |
| P1 | The exit contract | extract | ○ | ● | ● | ● | ○ | none | partly |
| P2 | The return stack | guide | ● | ◐ | ○ | ● | ◐ | low | PC |
| P3 | Breadcrumb bar | guide, verify | ● | ◐ | ○ | ◐ | ◐ | low | buildable |
| P4 | Measured immersion | verify | ○ | ◐ | ○ | ● | ○ | none | buildable |
| P5 | Pebbles, not bread | guide | ● | ● | ○ | ◐ | ○ | low | buildable |
| P6 | The airlock | guide | ● | ◐ | ◐ | ◐ | ● | medium | buildable |
| P7 | Home base | verify | ● | ◐ | ○ | ○ | ◐ | low | partly |
| P8 | Real home vector | guide | ● | ● | ○ | ● | ◐ | low | yes |
| P9 | Rope length | extract | ● | ○ | ● | ◐ | ● | low | partly |
| P10 | Leaving is free | (removes cost) | ○ | ◐ | ● | ○ | ◐ | none | partly |
| O1 | The anchor person | extract, verify | ● | ● | ● | ● | ● | low | yes |
| O2 | The call-back signal | extract | ● | ◐ | ◐ | ◐ | ● | none | yes |
| O3 | The buddy line | guide, extract | ● | ● | ◐ | ◐ | ◐ | low | buildable |
| Y1 | The totem | verify | ● | ◐ | ○ | ◐ | ○ | none | yes |
| Y2 | Reality-check habits | verify | ● | ○ | ○ | ◐ | ◐ | low | yes |
| Y3 | A letter from before | guide, verify | ● | ○ | ◐ | ○ | ◐ | none | yes |
| Y4 | Re-entry checklist | guide | ● | ○ | ○ | ○ | ◐ | none | yes |
| Y5 | Before and after | verify | ● | ○ | ○ | ○ | ◐ | none | yes |

## What the table says

1. **Nothing anchored in the content made the list.** That is deliberate: a trail drawn by the world is bread. In-world guides are fine as comfort, but they are not a thread.
2. **Against your own mind, acting beats informing.** The strong scores in the *own mind* column (H6, P6, P9, O1, O2) all either act on you or were decided before you went in. Ideas that only inform you depend on you noticing, and noticing is what fails.
3. **Against hostile content, only outside anchors hold.** Every strong score in the *hostile* column is anchored in the platform, in separate hardware or in a person.
4. **Captivation is answered by rules, not devices.** The strong scores there (H1, P1, P9, P10, H6) are guarantees about leaving: always possible, never punished, limits set in advance.
5. **The self is the least served starting point.** Only Y3, Y5 and the airlock (P6) aim at it at all. This is the biggest gap in the catalogue.
6. **The anchor person is the best single thread, and the least available.** Most immersion happens alone. Much of the design work is approximating O1 without a person.

## A starter thread

If someone wanted the strongest thread buildable today with consumer hardware, a reasonable first combination is:

- **H1 The Arch** (the headset's system button, used only for leaving) as the extractor,
- **P8 Real home vector** and **P2/P3 the return stack with a breadcrumb bar** as the guide,
- **H4 Reality heartbeat** on a watch as the out-of-band clock and layer check,
- **P6 The airlock** with **Y3 a letter from before** as the transition,
- **Y4 Re-entry checklist** as the habit,
- **O1 an anchor person** whenever the session is long, deep or new.

The [prototypes](prototypes.md) chapter breaks this into pieces that can each be built and tested on their own.
