# Wayfinding, breadcrumbs and redirection

Breadcrumb trails have been in VR research for over thirty years, as a way to find your way *around* a virtual world. The same field also developed techniques that quietly separate where you think you are from where you really are.

## Breadcrumbs in virtual worlds

- **Darken & Sibert (1993)** built one of the first navigation toolsets for virtual environments, including **breadcrumb markers** dropped along the user's path. A later account notes their weakness: the markers did not show *direction*, so a trail could tell you where you had been, but not which way led back.
- **Darken & Sibert (1996)** studied wayfinding in large virtual worlds with grids and maps (not breadcrumbs). Their principles still read well as thread requirements: **"Always show the observer's position"**, **"Provide frequent directional cues"**, and divide the world into distinct places.
- **Ruddle (2008)** generated trails *automatically* from a user's own movement. When people returned to an environment five to eight weeks later, the trails cut how far they had to search.

## Redirection: the world bends your path

- **Razzaque et al. (2001)** introduced **redirected walking**: rotating the virtual scene slightly as people walk, by amounts too small to notice, so they walk a curved real path while seeing a straight one. It lets large virtual spaces fit in small rooms.
- **Suma et al. (2011)** redirected people by changing the virtual room behind their backs (moving a door, for example). People rarely noticed.
- **Tseng et al. (2022)**, "The Dark Side of Perceptual Manipulations in Virtual Reality", showed that redirection and similar techniques can be turned into weapons that cause physical harm.

## What this means for the thread

1. **Breadcrumbs need direction.** Darken and Sibert's markers had the same flaw that cave divers solved with *arrows* rather than plain markers (see [real ropes](../elsewhere/real-ropes.md)). A thread must say which way is out, not only where you have been.
2. **Automatic beats manual.** Ruddle's trails came from movement the user did anyway. A thread should be laid down without effort: you should never have to remember to drop a crumb.
3. **In-world breadcrumbs are bread.** Every trail in this literature is drawn by the virtual world itself. Good for navigating *inside*; not trustworthy as the way *out*.
4. **Your sense of real position can be bent without you noticing.** Redirection is harmless in its intended use, but it means the real-to-virtual alignment can drift silently, and Tseng et al. show it can be abused. Only tracking held by the platform, not the content, knows the real way back ([P8](../brainstorm/ideas-platform.md#p8-real-home-vector)). The [find-the-start-spot prototype](../brainstorm/prototypes.md#4-find-the-start-spot) tests exactly this.
5. **The hostile-content threat is not hypothetical.** Research has already demonstrated perceptual manipulation as an attack.
