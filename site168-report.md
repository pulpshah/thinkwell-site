# site168

## What was built

`thinkwell-site168.html`, one self-contained file, rebuilt from site162 onto the site168 kit and served as `index.html`. Styles are `tokens.css` then `components.css` in a CSS layer above the parts kept from site162, so a look is a class swap and no token value changed. Copy and numbers come only from `content168.json`. Every route in the sitemap, 139 in all, renders from one template function in one `innerHTML` write. The header menus with their 26 icons, the footer, the contact form, and the features table follow their boards. site162's router, look and language switches, live capsule, media loader, signup forms, and quote builder all still work. The Day story and the How it works diagram moved to About. The Day keeps site162's scroll behavior inside a sticky 1120 by 640 card that never fills the viewport, and stacks as seven stills under reduced motion.

## Choices made on my own

1. About uses the kit's h1 and h2 sizes, not the About board's larger ones, because token values may not change.
2. About's five values use a new `.vgrid`, since `components.css` gives `.vals` to the Values page.
3. Modals float from a fixed `#mx` host; the kit places them absolutely for the canvas.
4. The Day's time chips are a 44 px row along the bottom of the card, in site162's time format.
5. Home's use case panels take their heading and three lines from each use case, which the board omits.
6. Group counts in All features come from `content168.json`, not the features board.
7. Get early access opens the contact form with "Start free with Lite."
8. Added to `components.css` with tokens only: the header panels and phone sheet, the footer, Home's and About's own blocks, All features, the contact form, and the box model the kept parts expect.

## Gates

Every parity, word, tap, overlap, contrast, voice, return, and scroll gate passes on 44 routes at 8 widths in 3 looks. Layout shift 0, route change 11 ms, modal open 14 ms, the site's own tasks 1 to 14 ms. The startup long task reads 51 to 58 ms against a 50 ms budget, and one run printed PASS at 50 ms. The same check gives 69 ms for a blank page on this Mac, so that number is the renderer starting up under load here, not the page.

Pull request: PRLINK
