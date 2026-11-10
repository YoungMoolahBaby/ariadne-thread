# Threat models: drift to deception

"Getting lost" covers very different situations. A thread that handles one may be useless against another, so it helps to name them. They are ordered from mildest to worst.

## 1. Drift

Nobody wants you lost, and nothing is broken. You are simply absorbed, tired, disoriented or a little detached, and you lose track of time, place or self. This is the common case today and the one most research addresses.

*Defence:* gentle, well-designed transitions; clocks; routines; reminders.

## 2. The careless simulation

Software fails. An app freezes with your view inside it, crashes the tracking, captures the button you would use to leave, or simply has no clear way out. The "logout button is missing" premise of *Sword Art Online* (see [fiction](../elsewhere/fiction.md)) is, in its mild form, just a bug.

*Defence:* an exit path that does not depend on the app working: something the platform or the hardware guarantees.

## 3. The captivating simulation

The world does not lie to you, but it is built to keep you. Leaving costs you progress, streaks, social standing or a moment you will not get back. Engagement metrics reward this. Folklore knew it well: eat the food of fairyland, or the pomegranate seeds of the underworld, and you cannot fully leave.

*Defence:* exits that are always available and never punished; budgets set from outside, before you go in, when you are in your usual frame of mind.

## 4. The hostile simulation

The content lies. It draws a fake exit, a fake room, a fake "you are home now", or it tampers with the breadcrumbs you left. This is a security problem, and computer security has spent decades on its desktop version: a web page drawing a fake browser window, a program drawing a fake login prompt (see [computer security](../elsewhere/security.md)).

Here we assume the platform and hardware are still honest and only the content is hostile, the way a browser can be honest while a website is not.

This is not hypothetical. Researchers have intercepted the exit signal on a consumer headset and shown a fake home environment that fooled 26 of 27 people (Yang et al. 2024), and have moved immersed users to physical locations without their knowledge (Casey et al. 2019). See [what headsets ship today](../research/products.md) and [computer security](../elsewhere/security.md).

*Defence:* a trusted path: something the content cannot draw, intercept or imitate.

## 5. Your own mind

The hardest case is not outside you. Confusion, dissociation, fatigue, intoxication, or simply wanting to stay can all stop you from using a thread that works perfectly. In the far future, a direct neural interface might even reach the memory you would use to check whether you are out.

*Defence:* designs that need no reasoning in the moment (rehearsed, physical, by feel), and designs that **act on you rather than only informing you**: someone or something that brings you out whether or not you notice you need it.

## Beyond the list: the dishonest platform

If the hardware or the platform itself is hostile, and controls every sense, no test you perform with your senses can be trusted. This is the old philosophical problem of the evil demon (see [philosophy](../elsewhere/philosophy.md)). The only threads left are ones anchored entirely outside the system: other people and independent hardware that can pull you out physically. This book treats that case as the boundary of what design can do, not as something to solve.

## How the brainstorm uses this

Every idea in the [catalogue](../brainstorm/ideas.md) is rated against threats 1 to 5 in the [comparison](../brainstorm/comparison.md). The pattern that comes out of that table is the main finding of the brainstorm so far: **the further down this list you go, the further outside the simulation the thread has to be anchored.**
