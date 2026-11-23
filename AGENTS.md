# AGENTS.md — The Avenella Agency site

One file, `index.html`: inline CSS and JS, no build step, no libraries. Edit it directly. Keep it self-contained.

## Brand
- Name: **The Avenella Agency** (the agency arm of the **Avenella Group**).
- Palette: dark ink `#0B0B0D`, warm paper `#F6F4F1`, coral→gold gradient accent (`--grad`, coral `#E0785F` to gold `#C8A96E`). No second accent colour.
- Type: **Gabarito** (headlines, extra bold) and **Onest** (body), via Google Fonts.
- Voice: direct, witty, human. British English. No em dashes. No emojis.

## Structure (in order)
Hero → statement → promise marquee → **Our services** (`#work`, horizontal sweep) → client logo strip (`#clients`) → **Selected work** (`#again`, spinning wheel) → **Insights** (`#insights`) → **Contact** (`#contact`, typeform) → footer.

## Keep (do not break)
- Colour/type tokens live in `:root` (`data-8b-part="tokens"`). `--page` / `--ink` / `--ink-muted` flip with the light/dark toggle; `--color-1..7` are fixed.
- The scroll motion is CSS scroll-driven animation gated by `data-8b-live` (set in `motion-gate`) plus the inline `motion-kit` and `scene-script:*` blocks. Keep the `data-8b-*` attributes, the scene `<style>`/`<script>` blocks, and section `id`s.
- Light/dark toggle: `theme-gate` (head) + `theme-toggle` script + `data-theme="dark"` on `<html>`, saved to localStorage.
- Every section heading ends in the gradient dot (`<span class="m-dot">`).
- Forms post to Formspree `formspree.io/f/xeevolwo`.
- The Google Analytics tag and the "Design by Avenella Agency" footer credit.

## Content that must stay true (never invent)
Client names, results, rates, addresses, phone numbers and dates. Ask the owner. Insight card titles are editorial placeholders until real articles are supplied.

## Assets
Images are referenced by filename at the repo root (see README). Missing images degrade gracefully.
