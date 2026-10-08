# site177

## What changed from site175

site177 replaces the site175 and site176 kits on the same branch. The site170 base, the sections, the group links, and the All features layout carry over from `site175-report.md`.

- **No clicks.** The readouts' click and key handler and their `tabindex` are gone. A click or tap does nothing, and Tab skips them.
- **Hover loops.** These come from the site177 `readouts.css`, with no script. The rest of the picture dims to 35%. A point ring spins as a partial arc every 1.1 seconds, a region ring marches its dashes every 1.4 seconds, and a ringed label gets a highlight that sweeps across every 1.8 seconds.
- **Arrival.** Each picture fades in once from 97% size.
- **Features data.** `features-chart.json` now replaces the features block from `content170.json`, and the site175 stopgap rows are gone. It brings:
  - six new rows,
  - new values for Project Studio, Team workspace, Stakeholder book, and Accounts per channel,
  - Banned participants in place of Custom blocklist,
  - and the seven Craft rows in the Craft section.

  All features renders only from it: 187 rows, with no hard-coded counts.
- **The 84 site177 SVGs** replace the site175 set, with the same keys.

## Choices made on my own

1. **Section subheads.** The chart's rows carry a section, so each group shows a small subhead where its section changes, for example Craft and Anchors in Engagement. That is where the Craft move shows. The change labels (`chg`) are for the boards and are not shown.
2. **Slower arrival.** The kit plays the fade over the first 55% of a picture's entry, about 100 px of scrolling at the bottom edge, which is too quick to see. A page rule after `readouts.css` runs it from entry to 40% cover, as the picture rises to about mid-screen. Shah approved this.
3. **Clipped frames.** `overflow: clip` on readout frames stays from site174. Without it, `.media` is a scroll container, and the arrival never plays.

## Checks

Deferred until review. Before review: `chartcheck.py` prints `features on the page: 187 of 187`, every page shows its placements and sections with no script errors, and hover, no click, no focus, and the arrival were tested in Chromium.
