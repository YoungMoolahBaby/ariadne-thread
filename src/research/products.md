# What headsets ship today

The major platforms already have the beginnings of a thread: a reserved control, a boundary and a way to see the room. This chapter records what each documents, as of November 2026.

## Apple Vision Pro

- **Digital Crown.** Turning it adjusts how immersive the view is; double-clicking shows your surroundings; pressing it can exit an app and return to the Home View. Apple's design guidelines state that **visionOS apps do not receive direct information from the Digital Crown**. It is reserved for the system.
- **People break through.** You can see people when they approach you, even in an immersive experience.
- **Movement and boundaries.** Moving faster than a brisk walk clears your view and reduces immersion; leaving the boundary entirely reveals your surroundings. Apple's guidelines give immersive apps a boundary of about 1.5 m, beyond which passthrough rises and the app's visuals are replaced.
- **Design guidance.** The guidelines also say: "Avoid requiring people to use system controls to reduce immersion": apps should offer their own way down as well.

## Meta Quest

- **Meta button.** Meta's developer documentation: "The Meta button allows you to open or close the universal menu. It is an **OS-level feature and is not customizable**."
- **Boundary.** Virtual walls appear when you get close to the edge of a stationary or room-scale area, and the system can automatically switch to passthrough at the edge.
- **App control.** Apps may hide the boundary only while they are showing passthrough.

## PlayStation VR2

- **Function button** on the headset lets you instantly see your room.
- **See-through view** activates automatically when you leave the play area, after a warning near its edge.
- Whether games can block the Function button is not documented.

## SteamVR

- **System button.** Valve's OpenVR documentation: the system button input "is a special case that is used to summon or dismiss the SteamVR dashboard. The value of this component **will not be available to applications**."
- **Chaperone** shows the edges of the play area as tracked devices approach them.

## A reserved control already exists, but its result can be faked

Meta, Apple and Valve each document **one control that applications cannot intercept**. In security terms (see [trusted paths](../elsewhere/security.md)), this is a secure attention key, and it is the hardware basis for [the Arch (H1)](../brainstorm/ideas-hardware.md#h1-the-arch).

But a reserved *button* is only half of a trusted path. **Yang et al. (2024)**, "Inception Attacks: Immersive Hijacking in VR" (preprint), showed on Meta Quest that a malicious script could **intercept the user's exit-app signal and launch a fake home environment instead**. It deceived **26 of 27 participants**, and those who noticed glitches put them down to normal VR bugs. The attack needed developer mode or debugging access, so it is not a flaw in the reserved button itself. It shows what the button's *result* looks like to the user: a home screen, which is just more pixels, and pixels can be faked.

## What this means for the thread

1. **The extractor's input is mostly solved.** The major platforms reserve a control.
2. **The extractor's output is not.** What you see after pressing it is drawn on the same display as everything else. A trusted path needs feedback the content cannot imitate: a physical sensation, real light ([H2](../brainstorm/ideas-hardware.md#h2-real-light)), a separate device ([H4](../brainstorm/ideas-hardware.md#h4-reality-heartbeat)).
3. **Today's controls are menus.** They open a dashboard or a home view. None is documented as a single, unconditional "take me out, all the way" action.
4. **Place is well served, layer is not.** Boundaries and passthrough protect the body's place. Nothing tells you how many layers deep you are or where you entered.
5. **Apple's guidance already points the right way.** Content should offer its own gentle way down; the system control stays as the guaranteed one. That is the *bread for comfort, pebble for the exit* pattern.
