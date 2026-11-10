# Prototypes to build now

Five prototypes, each small enough to build and test on its own with today's hardware. Each names the ideas it tests, what to build, and what we would learn.

## 1. The thread layer (PC VR)

*Tests: P2 return stack, P3 breadcrumb bar, P8 real home vector, H7 black box.*

OpenXR lets developers install **API layers**: small libraries that sit between every OpenXR app and the runtime, seeing each call the app makes. A layer sees every session begin and end, every frame and the real head pose, and can add its own image on top of the app's. Tools such as OpenKneeboard already draw overlays into other people's games this way.

- **Build:** an API layer that
  - keeps a stack of sessions entered (P2) and logs them with timestamps and real poses to a file outside the app's reach (H7),
  - remembers the real start pose and, on a held button, draws the breadcrumb bar, time in, and an arrow to the start spot (P3, P8).
- **Learn:** how often people actually lose track of place and time; whether "point home" gets used; what the black-box logs of real sessions look like.
- **Limits:** layers drawn inside a single app (a world inside a world) are invisible unless apps declare them; a later step could propose a small OpenXR extension for declaring them.

## 2. The airlock

*Tests: P6 airlock, Y3 letter from before, Y4 re-entry checklist.*

- **Build:** a passthrough-capable app (Quest, or PC with passthrough) with a scene to spend time in, and two ways out:
  - **abrupt**: the scene cuts to passthrough, or the headset comes off;
  - **airlock**: the scene dims, the real room opens as a window, then all around; the real clock and time spent appear; the "letter from before" plays; a three-item checklist; then off.
- **Measure:** after each exit, time to point at the real door and to state the real time and the time spent; reach accuracy for a real object and memory of where real objects are (the two drifts Cheymol & Lopes 2025 found); a short balance test; a brief questionnaire about how real things feel; preference.
- **Learn:** whether a standard airlock measurably shortens re-orientation, and whether people accept the extra seconds. Existing work pulls both ways: people prefer brief transitions (Feld et al. 2024), but clearing carry-over took about a minute (Gottsacker et al. 2024). See [leaving VR](../research/exiting-vr.md).

## 3. Reality heartbeat

*Tests: H4 reality heartbeat, and the out-of-band principle generally.*

- **Build:** a watch app that taps a private rhythm every few minutes, chosen by the user, with the tap count encoding minutes since entry.
- **Study A:** during long sessions, stop the heartbeat at a random moment. How long until people notice?
- **Study B:** have the VR controllers play imitation taps. Can people tell the watch rhythm from a copy on a different device and body site?
- **Learn:** whether an out-of-band rhythm is noticed at all under absorption, and how much training it needs.

## 4. Find the start spot

*Tests: H3 tether, P8 real home vector, against redirected walking.*

- **Build:** a walking scene with redirected walking (the view slowly rotates so people walk a curved real path while seeing a straight one). At the end, the world goes dark and the person must walk back to the real start spot.
- **Conditions:** nothing; a light retractable cord from the start spot; a wristband that vibrates toward home; a visual "point home" arrow from the platform.
- **Measure:** distance from the real start spot, time taken, confidence.
- **Learn:** how badly redirection breaks people's sense of place, and which thread repairs it best. A clean, small study.

## 5. Rope length with a dead man's switch

*Tests: P9 rope length, H6 dead man's switch.*

- **Build:** before entry, the person sets a time budget; at two thirds, a gentle warning; at the end, the airlock starts. Separately, an occasional "still with us?" check that fades the world if missed twice.
- **Measure:** how often budgets are overridden; whether the checks are answered automatically without thought (habituation); annoyance ratings.
- **Learn:** whether pre-commitment works for immersion the way it partly works for screen time, and how to make a vigilance check that stays meaningful.

## Tools

- **OpenXR** for anything that must work across apps (prototype 1). API layers are the natural home for a cross-app thread on PC.
- **Bevy with bevy_openxr**, Unity or Godot for the standalone scenes in prototypes 2, 4 and 5.
- **A smartwatch** (Wear OS or watchOS) for prototype 3.
- For studies with other people: ethics review if done formally, and a sitter present for long sessions, as the research on long-term immersion did.
