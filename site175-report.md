# site175

## What was built

site174, brought up to site170 first, then the site175 readouts. Served as `index.html` and as `thinkwell-site175.html`.

**site170**, which was never built before now:

- `content170.json`: new headlines on 13 pages, and "local coverage" in place of "local jurisdictions".
- `components.css`: the h1 measure goes to 20ch, plus the `.uc` list, `.reads`, and `text-wrap: pretty`. The `.reads` rules that site168 kept in its own CSS are removed, so there is one definition.
- `nowidow.js`: `tieAll` runs after every render: route changes, which cover the language switch, plus modals, the phone menu, Home's tabs, and the features table. It replaces site174's stand-in.
- Feature details: three featured scenarios as a `.uc` list, from `feature_scenarios`.

**site175:**

- 84 readouts inline, focusable, with their own alt text. The 25 slots and 28 product cards are as in site174.
- 18 sections on 17 pages, before the closing call to action. Ten end with "See every {group} feature", linking to `#/features?group=…`, which opens that group and scrolls to it.
- Hover and focus dim the rest and the ring breathes. Click, tap, Enter, or Space shows the reveal and pops the ring, and it clears after 2.5 seconds.
- All features holds all 187 rows: every chart row, its sub-rows, and six source groups ("Sources: Recording" and the others) with their own columns. Closed groups stay in the page, hidden. "Show all" opens all 15.

## Choices made on my own

1. `readouts.js` attached its handlers once at load, but this site redraws each page. The same behavior runs as one delegated click and key listener. Readouts inside a link, such as the product overview tiles, stay plain pictures, so a click follows the link.
2. The kit's `/features#group` links don't work with the hash router, so they use `#/features?group=…`.
3. Shah supplied values for six new rows (Map, Issues, Tenant site, Persona provenance, Evidence graph, and Lobbying and stock chart). "Custom blocklist" is now "Banned participants", counted in people. Each new row's description is its picture title from the kit. The values are in `rows175.json` in the build.
4. site174's motion fixes stay, after `readouts.css`: `overflow: clip` on readout frames, and the wider arrival ranges.
5. On phones, source rows show each value with its column name, since there is no header row there.

## Waiting on

The updated content file, which carries the new values for Project Studio, Team workspace, Stakeholder book, and Accounts per channel, and moves the seven Craft rows. It isn't on the Mac yet. When it arrives, it replaces `content170.json` in the build.

## Checks

Deferred until review. Before review: `chartcheck.py` prints `features on the page: 187 of 187`. Every page with placements shows its readouts and sections in order, with no script errors. Hover, click, Enter, and the 2.5 second clear were tested in Chromium.
