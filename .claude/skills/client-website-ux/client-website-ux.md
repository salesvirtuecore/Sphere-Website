---
name: client-website-ux
description: UX/conversion design rules for client-facing marketing websites and landing pages (Science Sphere, Merci Boxing, Sphere Exam Academy, Adriel-template sites, and future VirtueCore client sites). Covers above-the-fold layout, CTA prominence, visual hierarchy, testimonials sectioning, and the behavioural-psychology principles behind them. Use whenever building, redesigning, or reviewing any public marketing page, landing page, or VSL page for a client — NOT the internal VirtueCore app (see vc-app-design for that).
---

# Client Website UX — Conversion Design Rules

Distilled from real, shipped changes to the Science Sphere site (logged in the
Variable Tracker) plus the behavioural-psychology research behind them. These
are defaults for every client marketing/landing page VirtueCore builds or
edits — not the internal `app.virtuecore.co.uk` dashboard, which has its own
design system in the `vc-app-design` skill.

## Non-negotiable rules (proven on a live site)

1. **CTA above the fold, and above the VSL/hero video.** The primary call to
   action must be the first interactive thing a visitor sees on load — before
   they've scrolled, before any video has to load or play. If a page has both
   a CTA button and a video/VSL, the CTA sits above it, not after it.
2. **The whole "first screen" is fully rendered on load** — no lazy-loaded
   gaps, no content cut off mid-element, no layout shift once fonts/images
   settle. A visitor should be able to see hero headline + CTA + primary
   proof point without scrolling or waiting.
3. **Size and weight encode importance.** The CTA button, the headline, and
   the primary proof/testimonial are the largest, boldest elements on the
   page. Supporting copy, secondary links, and legal/meta text are visibly
   smaller and lighter. If two elements look the same size, they should be
   equally important — if they aren't, fix the sizing, not the copy.
4. **Testimonials get their own clearly titled section** — a distinct block
   (e.g. "What parents/clients say") containing testimonial + the person's
   name/role, visually separated from surrounding content, not scattered as
   asides throughout the page.
5. **Cut low-value friction, don't just add more content.** The FAQ section
   was removed outright on Science Sphere rather than trimmed — if a block of
   content is answering objections nobody is actually raising, or adding
   choices before the CTA, remove it rather than shrinking it.
6. **Most important content lives at the top of the page**, not just above
   the fold in isolation — front-load value; nothing critical belongs
   halfway or two-thirds down a long scroll.

## Before shipping any page — checklist

- [ ] Can I see the CTA within 0–1 seconds of the page loading, with zero scrolling?
- [ ] Is the CTA visually the largest/boldest clickable element on the page?
- [ ] Does the page respond to interaction in <400ms (no visible lag on click/hover)?
- [ ] Are testimonials in one named section, not sprinkled loosely?
- [ ] Is there an FAQ, disclaimer, or options block sitting *before* the CTA that could be cut or moved after it?
- [ ] Count the choices/links visible above the fold — if it's more than ~7, cut or group some (Miller's Law).
- [ ] Nav and links are styled distinctly from body text (color/weight), consistently across the whole site.
- [ ] The single most differentiated/distinctive element on the page is the thing you most want remembered (Von Restorff).

## The psychology behind the rules

| Principle | What it says | Apply it as |
|---|---|---|
| **Heatmap reality** | Clicks/move/highlight maps show visitors act on what's visible immediately; nav consistently gets meaningful click share | CTA must be visible with zero scroll; treat nav as a real conversion path worth testing, not just utility |
| **Aesthetic-Usability Effect** | Users perceive more attractive designs as more usable, and forgive more | Polish shouldn't be treated as separate from function — a cleaner-looking page will test as more "usable" even at equal functionality |
| **Doherty Threshold** | Productivity/engagement spikes when the system responds in under ~400ms | No visible lag on any interaction; optimize perceived load time of the hero/CTA above all else |
| **Fitts's Law** | Time to reach a target shrinks as the target gets bigger and closer | Make CTAs, testimonial cards, and VSL play buttons large and easy to hit — never small or tucked in a corner |
| **Hick's Law** | More/more-complex choices = slower decisions | Fewer options near the CTA; break multi-step actions (booking, signup) into small single-decision steps |
| **Jakob's Law** | Users expect your site to behave like every other site they use | Don't reinvent nav, button, or form conventions — familiar patterns convert better than novel ones |
| **Law of Similarity** | The eye groups visually similar elements as one unit | Style nav/links distinctly from body copy, and keep that styling consistent site-wide so it reads instantly as "clickable" |
| **Miller's Law** | Working memory holds about 7±2 items | Cap simultaneous choices (menu items, pricing tiers, form fields visible at once) near 5–7 |
| **Pareto Principle** | ~80% of outcomes come from ~20% of causes | Spend design effort on the CTA, hero, and proof section — not evenly across every page element |
| **Serial Position Effect** | First and last items in a sequence are best recalled; middle items are weakest | Put the strongest hook first and strongest close last; bury the least important content in the middle, never at the edges |
| **Von Restorff Effect** | An item that visually differs from its neighbors is remembered best | Make the one thing you want remembered (CTA, key stat, headline offer) visually distinct from everything around it |
| **Zeigarnik Effect** | Incomplete/interrupted tasks are remembered better than completed ones | Use progress indicators / partially-filled forms / "you're 80% done" states to pull visitors back to finish an action |

## Where this comes from

Concrete rules are changes actually shipped and logged for Science Sphere
(sciencesphere.co.uk) via the Variable Tracker (Supabase `ops_log_entries` →
n8n → Google Sheets). When in doubt about a specific client site's current
layout, check that tracker or the live site rather than assuming — this skill
is the *rule set*, not a record of any one site's current state.
