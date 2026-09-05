# Midsomer Design — redesign note

## The direction

One ground colour, one ink, one green. The page is a warm off-white throughout, with near-black type and a single deep forest green used only where it earns its place: the italic word in a headline, the process line, the featured pricing plan, and the closing contact block. Nothing else is coloured. All the gradients, glows, paper-grain overlay, ticker and hover-lift-with-shadow effects are gone; they were each competing for attention and none of them was chosen.

Type does most of the work. Headlines are set in Instrument Serif — a large, quiet, slightly old-fashioned serif that reads as "studio" rather than "SaaS" — with DM Sans kept for everything else so the page still relates to `about.html`. Boxes are replaced by hairlines wherever possible, and the spacing is loose and even from top to bottom, so every section feels like it came from the same hand.

The hero follows your Squarespace instinct: centred copy at the top, and below it a large browser frame that fades into the page. Because there's no client screenshot yet, the frame holds a designed mock of a small-business site (a fictional café, "Elm & Ivy") built purely in CSS — it shows the kind of thing you make, weighs nothing, and drops out cleanly the moment you have a real screenshot. The 1.2MB illustration is no longer referenced; the whole page is now a 48KB file plus fonts.

## Running order, and why

1. **Hero** — the promise, one button, and the product preview. This is the "these people can design" moment.
2. **A single line of reassurance** — the six proof points from the old ticker and feature grid, set as one quiet row under the frame.
3. **Process (Steps 1–4)** — moved straight up to second position, as you suspected it should be. It's the best content on the page and it answers the obvious next question ("how does this actually work?") before people have to scroll for it. Layout, structure, alternating text/image and the continuous line on the left are untouched; it's been re-skinned into the new type and colour only. The image placeholders now carry a large serif numeral and an inset frame, so they read as intentional editorial panels rather than missing pictures.
4. **What's included** — the old bento boxes, rewritten as numbered hairline rows beside a sticky heading. Same copy, no boxes. It sits right before pricing because it's effectively "here's what the subscription buys".
5. **Pricing** — both tiers exactly as written. Starter is outlined; Growth is the one solid green card on the page, which makes it the obvious recommendation without a "most popular" badge.
6. **Work** — moved below pricing deliberately. With nothing to show yet, putting a portfolio near the top would undercut everything above it. Down here it's low-stakes, and the four tiles are each a different miniature site layout in a different stone/sage tone, with the honest line "Our first client sites are in production now." It looks like a section waiting for content, not a broken one.
7. **FAQ** — hairline accordion beside a sticky heading.
8. **Contact + footer** — one dark forest block to close the page, form on the right, a small "Meet the team" link to `about.html`.

Nav anchors are Process, What's included, Pricing, Work, Our Team, Book a call; the mobile menu adds Questions. Every link resolves.

## Mobile

Designed at 390px first. The menu is a full-screen panel with large serif links (Menu/Close toggles, closes on link tap, Escape, or resize). The hero preview reflows to a single column; the reassurance row becomes a dashed list; the process becomes a single column with the line still running down the left; pricing stacks with Growth second; the contact form goes single-column with a full-width button. No horizontal scroll at any width.

## Accessibility

All text is at or above AA (lowest ratio on the page is the tertiary grey at 4.6:1; most body copy is 7:1+). Visible focus rings on everything interactive (white on the dark block). FAQ buttons carry `aria-expanded`; the menu button carries `aria-expanded`/`aria-controls`; form fields have real labels, `autocomplete` attributes and native validation. `prefers-reduced-motion` kills the reveal animations and smooth scroll.

## What I'd commission to finish it

In order of impact:

1. **One real client site screenshot for the hero frame.** Even a work-in-progress build. Shoot it at 1440px wide, export as a WebP under 200KB, and replace the `.site` block inside `.frame` with `<img>`. This single image is worth more than everything else on this list.
2. **Four process photographs, square.** Warm, natural light, un-staged: a phone call or a coffee-shop meeting (Step 1), a laptop with a design open (Step 2), a small business owner in their shop (Step 3), a follow-up conversation (Step 4). Drop each into `.step-visual` as `<img>` — the numeral will be covered automatically. Same photographer for all four so they match.
3. **Portfolio screenshots as they launch**, 4:3, one per tile. Replace `.wire` with `<img>` and update the project name and sector.
4. **Re-skin `about.html`** to the same system (Instrument Serif headlines, this palette, hairlines). It'll look like a different site until that's done.
5. Optional: a **short Sydney-based photo of the team** for the contact block, and a **favicon** — the site has none.

## Practical

- Single self-contained `index.html`, inline CSS and JS, no build step. Google Fonts: Instrument Serif and DM Sans.
- The previous `index.html` is in git history if you want to compare.
- The contact form still has no backend; it validates and shows a confirmation message on submit. Formspree or Netlify Forms would slot in with one attribute change on the `<form>` when you're ready.
