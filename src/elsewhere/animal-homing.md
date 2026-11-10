# How animals find home

The desert ant *Cataglyphis* forages across featureless salt pans, wandering far from its nest on a winding path, then runs straight home. It is the best-studied natural "way back", and its failures are as instructive as its success.

## Path integration

The ant keeps a running **home vector**: the direction and distance back to the nest, updated with every step. It does not compute this exactly. **Müller & Wehner (1988)** showed that ants use a simpler approximation, which produces small but systematic errors, and errors grow with the length of the trip.

Distance is measured by counting steps. **Wittlinger et al. (2006)** put ants on tiny stilts after they reached a feeder: they overshot the nest on the way home. Ants with shortened legs undershot. The odometer can be fooled by changing the body.

## When the vector runs out

If the ant reaches the place where the nest *should* be and finds nothing, it starts a **systematic search**: loops that keep returning to the expected spot and slowly widen, so the most likely place gets searched most (Wehner & Srinivasan 1981, reviewed in Waldner & Merkle 2018).

Ants carried by an experimenter from a feeder to unfamiliar ground run their **full stored home vector** anyway, and search where the nest would have been. Their internal sense of home moved with them.

## The vector only resets at home

The most striking result: **Knaden & Wehner (2006)** found that only cues associated with *being inside the nest* reset the home vector to zero. Ants caught right at the nest entrance and released there **still ran off along their home vector, away from the nest they were standing at**.

## Landmarks near home

Close to the nest, when the home vector is nearly used up, ants switch to landmarks, which override path integration (Bregy et al. 2008). The internal estimate gets you close; recognisable features finish the job.

## Lessons for the thread

1. **An internal sense of direction drifts, and the drift grows with distance.** The longer and more winding the session, the less your own sense of the way back should be trusted. An outside record is needed ([P8](../brainstorm/ideas-platform.md#p8-real-home-vector), [H7](../brainstorm/ideas-hardware.md#h7-black-box)).
2. **Change the body and you fool the odometer.** The stilts experiment is the animal version of redirected walking: alter how movement is measured and the internal map is wrong without the animal noticing (see [wayfinding](../research/wayfinding.md)).
3. **Arriving is not the same as resetting.** The ant at its own front door still runs off on its old vector. People leaving VR still reach for where virtual objects were (Cheymol & Lopes 2025, see [leaving VR](../research/exiting-vr.md)). Coming back needs an explicit **"you are home" reset**, a deliberate moment that zeroes the old vector. This is a job for the [airlock](../brainstorm/ideas-platform.md#p6-the-airlock).
4. **Have a fallback when the vector fails.** The systematic search is a good model for what a thread should do when tracking is lost: return to the most likely home position and widen out, honestly signalling uncertainty, rather than pointing confidently the wrong way.
5. **Combine an internal estimate with landmarks.** Path integration for the long trip, recognisable features for the last stretch: a [home base](../brainstorm/ideas-platform.md#p7-home-base) and personal anchors finish what the platform's vector starts.
