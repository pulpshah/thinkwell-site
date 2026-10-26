# Thinkwell site, v2

The new Thinkwell website, built from the Thinkwell Site boards (`board/site` on the `design/board` branch of
PulpInternet/loosethreads-fr) with the real kit from loosethreads-fr main (8e181df).

- `index.html`: the home page, in this order: the first screen, How it works, the morning on the Home screen,
  Interactive documents, State and federal policy, Practice, What it learns, Plans, About and the footer.
- `product/craft/`, `product/other-side/`, `product/documents/`, `product/government/`: product pages, each with one or
  two working examples, explained.
- `plans/`: plans, add-ons, credits and All features.

Light, Dark and Mono are at the top of every page; with no pick, the viewer's system setting decides. Sample data is
marked Sample, simulated people are marked Simulated, and prices and photographs are slots. Every page is `noindex`
while the site is a draft.

To update: `S=<scratchpad> LT=<lt-main> sh board/site/tools/build.sh`, then copy `out/kit/`, `out/product/`,
`out/plans/` and `board/site/marks/*.svg` here (keep this `index.html`), and push.
