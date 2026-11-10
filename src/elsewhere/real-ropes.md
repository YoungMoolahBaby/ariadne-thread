# Real ropes: caves, fires, mines, mountains, space

People who work in places where getting lost kills have built literal threads, refined by accident reports over decades. Their rules transfer surprisingly directly.

## Cave diving

Cave divers follow a **continuous guideline** from open water into the cave and back. Sheck Exley's *Basic Cave Diving: A Blueprint for Survival* (1979) built each chapter around accident reports. His analysis of cave-diving deaths grouped them into a few causes, chief among them **failing to keep a continuous guideline to the surface** and **failing to reserve two thirds of the breathing gas for the exit**. Training and lights were added to the list later.

Markers on the line form a small tactile language, readable in zero visibility:

- **Line arrows** are directional. They point along the line toward the exit (or the nearest air), and divers can tell which way they point **by feel**. In caves with several entrances, an arrow may point to a different exit from the one your team used.
- **Cookies** are deliberately **non-directional** personal markers. Divers cut notches or holes in their own so they can recognise them by touch.
- **REMs** (referencing exit markers) are directional only to the diver who placed them; to everyone else, they count as cookies. Training guidance is blunt: personal markers **should not be trusted unless the diver or team installed them**.

The **rule of thirds**, a standard practice derived from that gas reserve, uses a third of the gas going in, a third coming out, and keeps a third for emergencies. You turn around when the first third is used, however good the dive is.

## Firefighting

Firefighters in smoke-filled buildings lay **guidelines** from the entry point.

- **UK.** National guidance requires that "the exit direction on all guidelines should be clearly and easily identifiable **by touch**", using paired tabs along the line. A firefighter rejoining a main line from a branch checks the first set of tabs to make sure they are heading the right way. Branch lines carry tallies with holes equal to the branch number, and there are limits on how many main and branch lines one entry point may have. The exact tab geometry sits in brigade training notes.
- **US.** Practice varies by department. One published method marks the line with knots every ten feet: **one knot then two means *in*; two knots then one means *out***.

The convention differs by country and even by brigade, but the principle is the same everywhere: **the line itself tells you which way is out, by touch**.

## Mine rescue

US federal regulations (30 CFR 75.380) require a **continuous, durable directional lifeline** in coal mine escapeways, with:

- reflective material every 25 feet;
- a **directional cone** at least every 100 feet, its tapered end pointing into the mine, so the wide end leads out;
- two cones in a row meaning a branch line ahead;
- four cones forming two diamond shapes marking a branch to a cache of self-rescue breathing devices;
- a spiral coil marking a branch to a refuge;
- a sphere marking doors at intersections.

Regulators have refused to accept existing rails or conveyor structures as a substitute, because their tactile markers get damaged.

## Mountains

On glaciers, climbers mark their route with **wands** (thin bright stakes) and, where wands run short, ski-pole holes every five to ten metres, which may be the only safe way to retrace the route in a whiteout.

## Space

Spacewalkers stay tethered to the station. As a last defence if a tether fails, NASA's **SAFER** (Simplified Aid For EVA Rescue) is a small nitrogen-jet pack that lets an astronaut fly back. The thread has its own backup.

## Lessons for the thread

1. **Continuity is the first rule.** Exley's top cause of death was a break in the line. A thread with a gap is not a thread ([R2](../brainstorm/requirements.md#ten-requirements)).
2. **Direction must be built into the trail.** Plain markers say "someone was here"; arrows say "out is this way". Darken and Sibert's 1993 VR breadcrumbs lacked exactly this (see [wayfinding](../research/wayfinding.md)).
3. **Readable by touch, without light or thought.** Every one of these systems is designed for zero visibility and high stress. The thread's equivalent is a sense the simulation does not own ([H3](../brainstorm/ideas-hardware.md#h3-the-tether), [H4](../brainstorm/ideas-hardware.md#h4-reality-heartbeat)).
4. **A small tactile vocabulary goes a long way.** The mine lifeline encodes *out*, *branch*, *supplies*, *refuge* and *door* with five shapes. A depth gauge or haptic thread could carry *out*, *layer boundary*, *home* and *time* the same way ([H5](../brainstorm/ideas-hardware.md#h5-depth-gauge)).
5. **Trust only the markers you placed.** The REM rule is *pebbles, not bread* from inside the cave: a marker someone else placed may serve their exit, not yours. In a simulation, only markers you or your platform laid down count ([P5](../brainstorm/ideas-platform.md#p5-pebbles-not-bread)).
6. **Reserve the way back before you start.** The rule of thirds decides when to turn around *before* the dive, not in the moment ([P9](../brainstorm/ideas-platform.md#p9-rope-length)).
7. **Do not accept substitutes that degrade.** The mine regulators' refusal is a design principle: a thread made of something that wears out or can be damaged is not a lifeline.
8. **Have a backup for the thread itself.** SAFER exists because tethers fail.
