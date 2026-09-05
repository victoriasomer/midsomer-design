# Brief for Fable — Midsomer Design visual overhaul

*(Paste everything below the line into Fable, along with `index.html`.)*

---

## The business

Midsomer Design builds websites for small businesses. There's no upfront cost — clients pay a simple monthly subscription that covers design, hosting, updates and ongoing support. We're based in Sydney.

The site attached is our one-page marketing site (a single static `index.html`, inline styles and scripts, served from GitHub Pages at midsomerdesign.com).

## What I want

A complete overhaul of how the site **looks**, and a free hand on how it's **arranged**.

The problem is simple: **this is a website design studio, and the website doesn't sell that.** It looks competent and generic. It looks like a template. Someone landing here should immediately think "these people can design", and right now they won't. That's the bar — every decision should serve it.

Treat this as a real design commission, not a tidy-up. You're the designer here; I'm not going to tell you how to solve it. I'll tell you what I want it to feel like and what has to stay.

## Structure — your call

I'm not attached to the current running order, and I don't think it's necessarily right. Rearrange it however you think the page works best.

To be specific about where I'm unsure: **the bento-style feature boxes sitting just under the hero don't do much for me.** I'm not convinced that's the right thing to hit people with first, and I'm not convinced they need to be boxes at all. Maybe the step-by-step process should come up there instead — that's the strongest content we have, and leading with it might be smarter than leading with a grid of features. That's a hunch, not a decision. You decide.

More broadly: reorder sections, merge them, cut what isn't earning its place, or introduce something new if the page needs it. The content is roughly right; the arrangement is genuinely open. Build the page you think converts best and reads best.

## The one thing that must not change

The **process section** — the numbered Step 1 to Step 4 sequence, with the alternating text-and-image layout and the continuous vertical line running down the left edge.

I love this. It's the best thing on the page and it's the piece I'd point at if someone asked what our work looks like. Keep its layout, its structure and its character intact. Re-skin it only as far as you need to so it sits inside whatever visual system you build — it should still be recognisably this section when you're done.

**It can move anywhere on the page** — that's the layout freedom above. It's the design *of* that section I want protected, not its position.

Use it as the benchmark. The rest of the page currently looks cheaper than this section does; the job is to bring everything else up to it, not to bring it down to everything else.

## Direction

I want it to feel like **Squarespace's own marketing site** — that's the reference. Confident, quiet, expensive. Space used generously. Very few tricks; the impression comes from typography, restraint and one or two genuinely beautiful moments. Nothing shouty.

One specific thing I'd like you to try: **Squarespace's hero approach** — the text centred at the top of the page, and a large preview of the product sitting below it. I think that suits us better than what we have now. If you think there's a stronger way to open the page, show me that too, but that's my instinct.

Beyond that, priorities in order:

1. **It should feel designed as one thing.** At the moment each section looks like it was made on a different day. I want a single consistent system running through the whole page — type, colour, spacing, the way components behave.
2. **It should feel considered.** Fewer, better decisions. Right now there's a lot going on and none of it feels chosen.
3. **The empty state has to look intentional.** Our portfolio images and process images aren't ready yet. As it stands the placeholders make the site look unfinished, which is fatal for a design studio. Design them so the page still looks deliberate and complete before real images go in.
4. **Mobile matters more than desktop.** Most of our audience will see this on a phone. Every section needs to be properly designed at small sizes, not just stacked.

Restraint over novelty throughout. If the choice is between "more interesting" and "more expensive-looking", go expensive-looking.

## Practical constraints

- Ship a **single self-contained `index.html`** — inline `<style>` and `<script>`, no build step and no framework. It's on GitHub Pages. Google Fonts links are fine.
- Keep the `about.html` link, the page title and meta description, and a working mobile menu. If you restructure the page, update the nav anchors to match whatever sections you end up with — just make sure every nav link goes somewhere.
- Keep the copy and both pricing tiers substantially as written. Trimming or re-splitting text to suit a new layout is fine; rewriting the offer isn't.
- Accessible: AA contrast, sensible focus states, and honour `prefers-reduced-motion`.
- The contact form has no backend — it just needs to look and behave right.
- Watch the weight. The current hero image is 1.2MB; don't add to that problem.

You have a free hand on everything else — colour, type, layout, imagery, motion.

## What I'd like back

The redesigned `index.html`, plus a short note on the direction you took, the running order you settled on and why you ordered it that way, and anything you'd recommend I commission — photography, screenshots, illustration — to finish it off properly.
