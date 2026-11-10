# Computer security: trusted paths

Computer security has spent fifty years on a question very close to this book's: how does a person know they are dealing with the real system, and not a program pretending to be it? Its answers carry over almost directly, and recent research has started applying them to headsets.

## The trusted path

The US Department of Defense's *Trusted Computer System Evaluation Criteria* (the "Orange Book", 1985) required systems at its higher levels to provide a **trusted communication path** between the user and the system's trusted core, initiated exclusively by the user. At the highest level it had to be "logically isolated and unmistakably distinguishable from other paths."

**Windows' Ctrl+Alt+Del** is the best-known implementation. The login process registers it at start-up as the *secure attention sequence*, ensuring no application can intercept it, and switches to a separate secure desktop when it is pressed. Larry Osterman, who worked on it, explained the reason for Windows NT 3.1: "we needed to have a keystroke sequence that couldn't be intercepted by any application." Ctrl+Alt+Del was chosen because no shipping application used it.

## The line of death

Eric Lawrence's essay **"The Line of Death"** (2017) describes the browser's version: the browser controls the top of the window (address bar, padlock), and the website controls every pixel below. Trust indicators must live above the line. But even that fails: a page can draw a picture of a whole browser window, trusted UI included, and full-screen mode hides the real one entirely.

**Jackson et al. (2007)** tested this. Fake browser windows drawn inside a page (*picture-in-picture* attacks) fooled users as well as the best other technique, Extended Validation indicators did not help, and users who had read the browser's help file about security indicators became more likely to trust *both* real and fake sites.

## Detecting that you are inside a simulation

Programs sometimes need to know whether they are running inside a virtual machine, which is a direct analogue of "am I in the simulation?".

- **Joanna Rutkowska's "Red Pill" (2004)** detected virtual machines with a single processor instruction, by noticing where a system table had been relocated. It later stopped working reliably on newer hardware.
- **Garfinkel et al. (2007)**, "Compatibility is Not Transparency", concluded that "building a transparent VMM is fundamentally infeasible, as well as impractical from a performance and engineering standpoint." Timing, memory caches and unusual devices always give the virtual machine away.

## Records that cannot be rewritten

- **Measured boot.** During start-up, each stage hashes the next component *before* running it into a TPM register that can only be extended, never overwritten, so a component cannot erase its own measurement. The TPM can sign a report of these measurements for a remote verifier (*remote attestation*).
- **Shadow stacks.** On a function call, Intel CET processors push the return address both to the normal stack and to a protected **shadow stack** that applications cannot write. On return, if the two differ, the processor stops the program. The return address is literally the breadcrumb back to the caller, and the shadow stack is its pebble copy.

## Security research on headsets

The question has now reached VR and AR directly:

- **Hosfelt et al. (2020)**, "Look Before You Leap" (preprint), note that the immersive web **"has no concept of a browser chrome"**: no line of death. In a small study of three trusted-UI designs, the most-liked design was the least effective, and a spoofed indicator fooled 44% of participants.
- **Cheng et al. (2024)**, "When the User Is Inside the User Interface" (USENIX Security), identify properties that make AR interfaces hard to secure, and demonstrate input forgery, clickjacking, denial of input, an object-in-the-middle attack and object erasure across five platforms. Every platform allowed at least three.
- **Cheng et al. (2023)** (USENIX Security) studied perceptual manipulation attacks in mixed reality. Effects carried into later tasks even after the attack stopped, and some defences participants invented for themselves backfired.
- **Mukherjee et al. (2025)**, "Shadowed Realities" (USENIX Security), found five new UI attack techniques in WebXR, mostly unnoticed by users.
- **Casey et al. (2019)**, "Immersive Virtual Reality Attacks and the Human Joystick" (IEEE TDSC), attacked the chaperone and overlays on consumer headsets, and in a deception study **moved immersed users to physical locations without their knowledge**.
- **Yang et al. (2024)**, "Inception Attacks: Immersive Hijacking in VR" (preprint), intercepted the exit signal on Meta Quest and showed a **fake home environment** instead. It fooled 26 of 27 participants (see [what headsets ship today](../research/products.md)).

## Lessons for the thread

1. **Reserve the input.** A control no content can intercept is the foundation. Headsets have one ([H1](../brainstorm/ideas-hardware.md#h1-the-arch)).
2. **Reserve the output too.** Ctrl+Alt+Del works because it switches to a *separate desktop* that applications cannot draw on. A headset that answers the reserved button with more pixels on the same display is only half a trusted path, and *Inception Attacks* shows the other half being exploited.
3. **VR has no line of death.** Content owns every pixel. The equivalent has to be found elsewhere: a different sense, a different device, real light, or a moment the platform owns in time rather than in space (the airlock that only ever follows the reserved button).
4. **Indicators that users must read are weak.** Picture-in-picture and spoofed VR indicators fooled large fractions of users, and training sometimes made it worse. Prefer threads that *act* over threads that *inform*.
5. **Perfect simulation is hard in practice.** Garfinkel et al.'s conclusion is mildly encouraging: something always leaks. But they were talking about programs inspecting hardware. A human inspecting rendered senses is a far weaker detector.
6. **Keep the way back in write-protected storage.** Measured boot and shadow stacks are working designs for [measured immersion (P4)](../brainstorm/ideas-platform.md#p4-measured-immersion) and [the return stack (P2)](../brainstorm/ideas-platform.md#p2-the-return-stack).
7. **The hostile-content threat is real, demonstrated and published.** Fake exits, moving people physically and invisible interface attacks have all been shown on consumer hardware.
