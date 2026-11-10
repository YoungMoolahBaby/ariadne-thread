# Anchored in hardware

Ideas whose trust comes from a physical device the content does not control.

## H1. The Arch

*Job: extract · Restores: layer, place · Today: partly*

One physical control, reserved by the hardware and operating system, which no app can capture, remap or delay, and which always does exactly one thing: start the way back. Named after the holodeck's "Computer, arch".

- **Why:** computing already has this. On Windows, Ctrl+Alt+Del is a *secure attention sequence*: programs cannot intercept it, so pressing it guarantees you are talking to the real system (see [computer security](../elsewhere/security.md)). Meta, Apple and Valve each document a headset control that apps cannot intercept (see [products](../research/products.md)).
- **What is new:** today's system buttons open a *menu*. The Arch should be a single unconditional action, held for a moment, that begins the exit sequence, whatever the content is doing. The feedback should also be hardware-only (a physical click, a change in the headset you can feel, real light) so the content cannot imitate the *response* either. This matters: researchers intercepted the exit on a consumer headset and showed a fake home screen that fooled 26 of 27 people (Yang et al. 2024).
- **Protects against:** careless, captivating and hostile content.
- **Weak spot:** you have to decide to press it. Useless against drift you do not notice, or against a dishonest platform.
- **Build it:** the button exists on every headset; the single-action behaviour would need the platform maker, or can be approximated on PC with a system-level overlay.

## H2. Real light

*Job: verify, extract · Restores: layer, place · Today: yes, in a few designs*

An exit that ends in real photons. A visor that flips up, or an optical shutter that opens, so the final step of leaving is your eyes receiving light straight from the room, with no camera and no display in between.

- **Why:** camera passthrough is a rendering, and a rendering can be faked. Glass cannot. Some earlier headsets had flip-up visors.
- **Protects against:** hostile content, and some of a dishonest platform: a shutter can be mechanical.
- **Weak spot:** only applies to optical headsets. Does nothing in a hypothetical direct-neural system. Adds weight and cost.
- **Build it:** mechanically simple; the open question is whether it can be done without making the headset worse.

## H3. The tether

*Job: guide, extract · Restores: place · Today: yes*

A literal thread. A light retractable cord from a clip at your start spot to your belt, or the soft version: a wristband that vibrates in the direction of home, driven by tracking that the content cannot see or change.

- **Why:** wired PC headsets already have a thread by accident: people use the cable to feel where they are. Wireless headsets removed it. Cave divers and firefighters trust a physical line over every other cue (see [real ropes](../elsewhere/real-ropes.md)).
- **Protects against:** drift in place, and redirection of your walking path.
- **Weak spot:** cords tangle and trip. The haptic version is only as trustworthy as its tracking.
- **Build it:** the cord is a weekend project. A good test: after a redirected-walking session, can people walk back to the start spot with eyes closed, with and without it?

## H4. Reality heartbeat

*Job: verify · Restores: layer, time · Today: buildable*

A watch or ring taps your wrist with a short rhythm every few minutes. The rhythm is private: chosen by you, or derived from a secret and the time, the way two-factor codes are. The content does not know the rhythm and cannot produce taps on that device. You learn to recognise it the way you recognise someone's knock.

- **Why:** it is an out-of-band channel, a different sense on a different device from the one rendering the world. Its absence is as informative as its presence: if the heartbeat stops, or sounds wrong, something is off. The tap count can also carry the time since entry, a clock the world does not control.
- **Protects against:** drift in time, hostile content that fakes a "you are out" scene (it cannot fake the heartbeat on the watch).
- **Weak spot:** subtle; people need training to notice its absence. A future system that writes touch directly to the brain could fake it.
- **Build it:** a simple watch app. The interesting study is whether people notice when it stops.

## H5. Depth gauge

*Job: guide, verify · Restores: layer · Today: buildable on PC*

A counter of how many layers deep you are, shown on a channel the content cannot draw on: a band that presses with one bump per layer, or a light at the edge of view driven by the display hardware rather than the app.

- **Why:** *Inception*'s danger was forgetting which level you were on. Nesting will become common long before full dive does.
- **Protects against:** confusion about layers; fake exits that "skip" levels.
- **Weak spot:** needs every layer to be registered (see [P2](ideas-platform.md#p2-the-return-stack)). A light in view can be imitated unless the content truly cannot draw there.
- **Build it:** a PC prototype can count nested sessions; the hardware indicator is the hard part.

## H6. Dead man's switch

*Job: extract · Restores: layer, time, self · Today: buildable*

Every so often, a gentle check asks for a small, deliberate response ("still me, still fine": a specific gesture, or a squeeze of a ring). Missing it once brings a louder check; missing it twice fades the world out to the real room. Train drivers have used vigilance devices of this kind for generations, and experts on getting users out of VR recommend exactly this escalation from gentle to forceful (Piumsomboon et al. 2022).

- **Why:** it is the only hardware idea here that works when you do *not* notice you need it. It catches absorption, sleep and dissociation.
- **Protects against:** drift, own mind.
- **Weak spot:** annoying if frequent; habituation (you answer without thinking); must never trigger in a moment where stopping suddenly is dangerous.
- **Build it:** straightforward on a headset or a watch; tune the interval with real users.

## H7. Black box

*Job: guide, verify · Restores: place, layer, time, state · Today: buildable*

An independent recorder (a phone or small device in the room) that logs where your body was, which apps and layers you entered, and when. It writes to storage the content cannot reach. After a session you can replay the path; during one, it is the evidence the other ideas draw on.

- **Why:** *pebbles, not bread* as a device. Also useful for research: there is very little real data on how people move between layers.
- **Protects against:** drift; tampering with in-world trails; confused memory afterwards.
- **Weak spot:** it informs, it does not act. Privacy: it is a recording of everything you did.
- **Build it:** a room camera or the headset's own tracking feeding a separate device.
