# Anchored in the platform

Ideas whose trust comes from the headset's operating system or runtime: the layer between the hardware and the apps. The platform sees every app start and stop, owns the tracking, and decides what is drawn on top. It is the browser to the content's web page.

## P1. The exit contract

*Job: extract · Restores: layer · Today: partly*

A standard every simulation agrees to, and the platform enforces: when you ask to leave, the content gets a short grace period (say two seconds) to save and close gracefully, and then the platform takes over regardless. The way operating systems ask a program to quit, then end it if it does not.

- **Why:** content crashes and content that ignores you are both handled the same way. Leaving becomes a promise, not a feature each app may or may not implement.
- **Protects against:** careless and captivating content.
- **Weak spot:** needs adoption by platform makers; content may push back. Some experiences need a moment to end safely (you are mid-jump, mid-sentence).
- **Build it:** platforms already end unresponsive apps. The contract is a written rule plus a visible timer.

## P2. The return stack

*Job: guide · Restores: layer · Today: buildable on PC*

The platform keeps a stack of every layer you enter: Home, then a social world, then a game inside it, then a replay inside that. Leaving pops one layer at a time, each with the same short, recognisable transition, so you can count your way out. "Leave all" pops the whole stack to Home.

- **Why:** in programs, the return address on the call stack is literally the breadcrumb back to the caller, and corrupting it is a classic attack. Modern processors keep a protected second copy, a *shadow stack*, that programs cannot write (see [computer security](../elsewhere/security.md)). The return stack is a shadow stack for you.
- **Protects against:** confusion about layers; content that "skips" you to a fake Home.
- **Weak spot:** layers that are not separate apps (a world-inside-a-world drawn by one app) are invisible to the platform unless the app declares them.
- **Build it:** on PC, an OpenXR API layer sees every session start and end and could keep this stack today (see [prototypes](prototypes.md)).

## P3. Breadcrumb bar

*Job: guide, verify · Restores: layer, place · Today: buildable*

On demand (for example, holding the [Arch](ideas-hardware.md#h1-the-arch)), the platform shows the path from Home to here, like the breadcrumb trail at the top of a website: *Home > Plaza > Arcade > Racing*. It also shows how long you have been in and the real direction to your start spot.

- **Why:** simple, cheap, and readable at a glance. Websites solved "where am I in this hierarchy?" decades ago.
- **Protects against:** drift and layer confusion.
- **Weak spot:** drawn in the same view the content draws in, so it is only trustworthy if summoned by a trusted action (H1). The content could draw a fake bar, but cannot make one appear in response to the Arch.
- **Build it:** a system overlay on PC.

## P4. Measured immersion

*Job: verify · Restores: layer · Today: buildable*

Every transition (entering an app, a world, a nested layer) is recorded as a link in a hash chain, the way a computer's secure boot records each piece of software it loads, or the way git records commits. Leaving checks off links in reverse. When you are back at the root, the chain says so, and a device outside (a phone, a partner's phone) can confirm it.

- **Why:** a tamper-evident record. If something skipped a layer, faked one, or inserted one, the chain will not unwind cleanly.
- **Protects against:** hostile content that fakes exits or inserts layers.
- **Weak spot:** mostly forensic. You read the result through your senses, so it needs a separate trusted display, such as your phone. Heavy machinery for a problem most people will not have soon.
- **Build it:** the logging part is easy alongside P2.

## P5. Pebbles, not bread

*Job: guide · Restores: place, state · Today: buildable*

Waypoints and markers you leave inside a world ("I came in here", "the door back is this way") are mirrored to storage outside the content. On the way out, the world's version is compared with the outside copy. If a marker has moved or vanished, you are told.

- **Why:** the direct answer to Hansel's birds. Cave divers have the same rule for personal exit markers: do not trust one unless you or your team placed it (see [real ropes](../elsewhere/real-ropes.md)).
- **Protects against:** drift, careless worlds that lose state, hostile worlds that move your markers.
- **Weak spot:** only works for worlds that expose positions to the platform; procedurally changing worlds will "move" markers innocently.
- **Build it:** spatial anchors already exist in mixed reality platforms; the outside copy is the new part.

## P6. The airlock

*Job: guide · Restores: place, layer, self, time · Today: buildable*

A standard transition space between any world and the real room, owned by the platform and the same every time. The world dims; the real room fades in gradually, first as a window, then all around you; there is a moment to re-calibrate (the real clock, the real time spent, the way to the door); then the headset can come off. Divers ascend in stages; this is decompression for the senses.

- **Why:** people are disoriented on leaving VR whatever the scene (Knibbe et al. 2018); hands and memory stay partly "in VR" afterwards (Cheymol & Lopes 2025); and one-minute transitions reduced carry-over between environments (Gottsacker et al. 2024). Flight simulator guidance already does a version of this: display off, cabin lights on, *then* the pilot gets out (Johnson 2005). A *standard* airlock also becomes familiar, and familiarity is a check in itself: if the airlock feels different, something is off. See [leaving VR](../research/exiting-vr.md).
- **Protects against:** drift, aftereffects, some confusion about self and time.
- **Weak spot:** adds time to every exit, and people prefer brief transitions (Feld et al. 2024), so they will want to skip it. Better: short by default, longer after long or deep sessions. Must never slow down an emergency exit.
- **Build it:** a passthrough fade with a clock and a short message is buildable in an afternoon. Measuring whether it helps is the real work.

## P7. Home base

*Job: verify · Restores: layer, self · Today: yes, in parts*

A single, fixed, personal space where every session starts and ends: perhaps a faithful copy of your real room, or a room that is distinctly *yours*. It never changes unless you change it, so differences jump out.

- **Why:** a familiar room is a totem the size of a room. Headsets already have home environments; the new part is that it is personal, unchanging and a mandatory start and end point.
- **Protects against:** drift and layer confusion.
- **Weak spot:** a hostile world can copy it perfectly. It is a check against drift, not deception.
- **Build it:** scan your room and use it as the start environment.

## P8. Real home vector

*Job: guide · Restores: place · Today: yes, in tracking*

The platform tracks your real position in the real room at all times, independent of what the content shows, and can always point you home: "your start spot is 2 metres behind you to the left."

- **Why:** content can deliberately bend your walking path (redirected walking) without you noticing. Your internal sense of direction can be fooled, as ants carried away from their path are fooled (see [animal homing](../elsewhere/animal-homing.md)). The headset's own tracking cannot be fooled this way.
- **Protects against:** drift in place; redirection.
- **Weak spot:** tracking can lose itself; then it must say so honestly.
- **Build it:** the data already exists in every inside-out headset; the "point home" gesture is a small overlay.

## P9. Rope length

*Job: extract · Restores: time, layer · Today: partly*

Before going in, while you are in your ordinary frame of mind, you set budgets: how long, how many layers deep, what wakes you. The platform enforces them. As with a diver's air, part of the budget is reserved for the way out: you are warned when you have used the share that leaves enough to get back comfortably. Cave divers call their version the rule of thirds (see [real ropes](../elsewhere/real-ropes.md)).

- **Why:** the decision about when to leave is made by the person outside, not the absorbed person inside. It is Ulysses tying himself to the mast.
- **Protects against:** captivation, drift in time, own mind.
- **Weak spot:** people override their own limits. The override needs to be harder than the limit, but not impossible.
- **Build it:** screen-time limits exist; the depth budget and the reserved way out are new.

## P10. Leaving is free

*Job: removes a reason to stay · Restores: state · Today: partly*

Leaving never costs anything: everything saves, everything resumes exactly as it was, nothing is lost by stepping out for a minute.

- **Why:** part of what makes leaving hard is what you would lose. Remove the cost and you remove the captivation that comes from it. Cheap and humane.
- **Protects against:** captivating content, own mind.
- **Weak spot:** shared worlds keep moving without you; a live event will not wait. Needs platform pressure on content makers.
- **Build it:** many apps suspend and resume today; making it a guarantee is the change.
