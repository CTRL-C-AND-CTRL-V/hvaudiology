# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A rebuild of the Hunter Valley Audiology website (https://hvaudiology.com.au, currently WordPress). The current stage is a **static HTML/CSS demo for client review**. It has no JavaScript, backend or build step; open `index.html` directly. README.md covers the structure, conventions and production path.

Key conventions in the demo:
- All links are relative and end in `index.html`, so pages work from disk or any host sub-path. The exception is `404.html`, which uses root-absolute paths.
- Header and footer are repeated in every page between `<!-- partial: … -->` comments. A nav or footer change must be made in all 24 HTML files.
- CSS: `assets/css/site.css` imports cascade layers in the order tokens < base < layout < components < pages < utilities. Components reference semantic tokens only, never raw hex values.
- Live features (booking, forms, reviews, maps, blog CMS, hearing screener) are only entry points, marked with `data-integration="…"`. Demo-only content is marked with `.demo-note` or `Photo:` placeholders.
- Every page has `<meta name="robots" content="noindex">` until launch.

Two planning documents are the source of truth for the rebuild:

- **`hvaudiology-site-inventory.md`** covers the content. §1 holds the business facts (addresses, phone numbers, prices, founder details) and is the single source of truth for them. §2–3 give the sitemap and the sections on each page. §5 lists the blog posts. §7 lists the problems the rebuild must fix. Longer body copy in the inventory is summarised, not verbatim, so rewrite it rather than presenting it as the original text.
- **`DESIGN.md`** is the visual system, a style reference based on Grove AI. It gives the colour, type, spacing, radius and shadow tokens (a ready-made `:root` block and a Tailwind v4 `@theme` block are at the end), component specs, and the Do's and Don'ts.

## Design rules that are easy to get wrong

- Forest green `#0b835c` is for accents only: the signature word in a serif headline, small-caps section labels, and icons. DESIGN.md contradicts itself here. Its "Agent Prompt Guide" (example 5) calls for a green filled CTA, but the Do's and Don'ts say the filled button is always dark `#1c1c1e`. Follow the Do's and Don'ts.
- Serif (Libre Caslon Text) is for hero or display headlines only. Everything else uses Geist.
- Radii come only from the set 8/12px, 20/24px or 9999px. Never use 14–18px. Shadows are hairline, with at most 1–2px of blur.
- Body text is left-aligned, with columns about 520px wide.
- In the Quick Start CSS, the font fallback stacks for the serif fall back to sans-serif. Fix this to a serif stack when you use it.

## Project skill

`frontend-design` is installed at `.agents/skills/frontend-design/`, and `.claude/skills/frontend-design` is a junction to that folder. `skills-lock.json` pins the installed version. Some of the skill's general advice goes against DESIGN.md: it discourages colouring a single headline word and all-caps labels. The skill itself says the brief wins, so DESIGN.md takes priority for this project.

## Content constraints for the rebuild (from inventory §7)

- The landline +61 2 9184 9628 is labelled "Fax" in one place and "Phone" in another. Confirm with the user which is correct before labelling it. The mobile number is 0448 187 960.
- The clinics are in Rutherford (main) and Muswellbrook (visiting). Newcastle and Maitland are only SEO target areas, so don't present them as clinic locations.
- Don't carry over the template leftovers ("Our Advertiser Services", the footer's "Properties" links) or the typos ("Anotomy", "About-us", "Contact-us").
- The hero slide 1 artwork and the `UH_PicCampaign_Vivante…` image appear to be Unitron marketing assets. Don't reuse them until the licence is confirmed.
- The booking iframe on the current site is broken. The real booking provider is Hearing Health Portal (australia.hearinghealthportal.com).
