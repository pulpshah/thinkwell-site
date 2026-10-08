# site178

## What changed from site177

- **Readouts.** The site178 SVGs and `readouts.css` are in. On hover, each picture plays its own loop:
  - bars regrow,
  - lines redraw,
  - waveforms pulse,
  - parts appear in order,
  - text types,
  - a loader turns,
  - or a live mark blinks.

  Nothing dims. There is no click behavior and no script. Each of the nine loop types was tested on a placed picture.
- **No placeholders.** Every "Saved for later" slot now shows a readout, 88 in all:
  - **Home:** the hero gets `sources`, and its six remaining use case tabs get their use case's picture.
  - **Scenario pages (81):** each gets the picture of the most specific feature it uses, meaning the feature that lists the fewest scenarios, from `feature_scenarios` and `features-coverage.json`.
- **More on Home.** Each of the four reads (What was said, Who said it, How it was argued, What it changed) has a picture: `transcript`, `voices`, `appeals`, and `claims`. With pictures, the reads sit two across, so picture text stays above 7.5 px, and one across under 720 px.
- **Logo.** The wordmark was drawn in `currentColor` on a link with no color, so it showed link blue, then red while pressed. It is now `--ink` in every look and link state, matching the reference logo. The mark keeps its pink.
- **Arrival.** The slower arrival range and `overflow: clip` from site177 stay.
- **Fixes from the gates.**
  - Sections holding readouts no longer use `content-visibility: auto`. Their real height (about 1,570 px at 720 px wide) is far over the 900 px estimate, so everything below them was placed too high, then jumped when they rendered.
  - The "See every … feature" links are 44 px tap targets.

## Checks

On 35 pages: every product, use case, and industry page, Home, the product overview, All features, and six scenario pages.

- `svgcheck.py`: svg label issues: 0
- `readsize.py`: readouts below 7.5 px: 0
- `chartcheck.py`: features on the page: 187 of 187
- No placeholder remains on any of the 125 routes or Home's tabs.
- site170 `site_gates.py` on the 30 changed routes, at 8 widths in 3 looks: every view passes. The performance budget reports one 61 to 70 ms long task at load. The live site168 measures the same, so it is renderer startup, as the site168 report found, not this change. Layout shift is 0, a route change takes 15 ms, and a modal opens in 17 ms.
