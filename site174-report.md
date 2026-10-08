# site174

## What was built

site168 plus the site174 readouts, served as `index.html` and as `thinkwell-site174.html`. The 66 readouts are inlined as SVG, so the look tokens and the motion reach them. `readouts.css` sits at the end of the kit layer.

- **Slots.** Every placeholder named in `placements.json` now shows its readout inside the existing `.media` wrapper: 25 slots.
- **Product cards.** The 28 cards named in `placements.json` have a readout above their `h3`.
- **New sections.** Nine pages have a three-card readout section just before the closing call to action: P-simulate, P-context, P-widget, P-capture, U-think, U-hear, U-track, U-test, and U-brief.
- **Motion.** CSS only, from `readouts.css`: the wipe, then the ring. No script.

## Choices made on my own

1. Built on site168, the live version. There is no site170 in the repo or on the Mac.
2. site168 already used the class `rv` on page sections for their fade-in. Left alone, the readout wipe would have run on whole sections, so the fade-in class is now `rvl`, and `rv` means only a readout.
3. Each readout's `aria-label` is filled from `index.json` alt text when the page is built, so it carries the numbers. The drawings are unchanged.
4. There was no `nowidow` pass to run, so the new section headings, titles, and lines keep their last two words together with a no-break space.
5. site168's `.media` box used `overflow: hidden`, which makes it a scroll container. That made the readouts' `view()` timeline follow the readout inside its own box, so the motion finished at once and only the still showed. Boxes holding a readout use `overflow: clip` instead, which clips the same way without being a scroll container.
6. `readouts.css` ran the wipe over 10 to 80 percent of a readout's entry, about 140 px of scrolling at the bottom edge of the screen, so it was over before the eye got there. A page rule after it widens the ranges: the wipe runs from entry to 45 percent cover, while the readout rises to mid-screen, and the ring draws from 40 to 60 percent cover. `readouts.css` itself is unchanged, and the last frame is still the still.
7. Placeholders the kit doesn't name stay as they are: 82 scenario pages, `home-hero`, and `home-usecase-prepare`.

## Checks

Deferred until review, as the handoff asks. Every route renders with no script errors, and each page shows exactly the readouts `placements.json` lists for it.
