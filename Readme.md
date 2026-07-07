# ECLYPSE — Landing Page

A cinematic, single-file landing page for **ECLYPSE**, a premium private strength club. Built as a dark, high-contrast experience anchored by a scroll-driven "Z-axis" hero sequence, with a full front-end system covering brand philosophy, facilities, membership, coaching, and community.

---

## Live Preview

Open `eclypse.html` directly in any modern browser — it's fully self-contained (images embedded, no build step, no server required).

---

## What's Inside

- **Hero** — Three background photos pinned during scroll, with a scroll-scrubbed "push-through" sequence: each layer sinks back and the next scales forward from blur/opacity-0, mimicking a fake 3D depth transition without any real 3D assets.
- **Brand Philosophy** — Headline + three supporting pillars (Raw Execution, Precision Coaching, Measurable Evolution).
- **The Eclypse Experience** — A horizontal-scroll rail of six facility cards (Strength Arena, Performance Lab, Recovery Chamber, Nutrition Studio, Elite Coaching, Community Lounge), including a hover-reveal crossfade on the Nutrition Studio card.
- **Memberships** — Three-tier pricing (Essential / Elite / Legacy), with the Legacy tier carrying a distinct copper accent to signal its premium position.
- **Meet the Architects** — Coaching section with a full-width trust-building banner image, followed by three coach profile cards.
- **Social Proof** — Quantified client outcome cards instead of generic testimonials.
- **Gallery** — A mixed photo/typographic mosaic grid.
- **Community** — Full-bleed photographic section with ambient floating particles and centered copy.
- **Strength Arena Anchor + Final CTA** — A last visual anchor immediately before the closing call-to-action, reinforcing value right at the decision point.
- **Footer** — Standard nav/contact/legal footer.

---

## Design System

| Token | Value | Usage |
|---|---|---|
| `--black` | `#0a0a0a` | Base background |
| `--panel` / `--panel-2` | `#121316` / `#17181c` | Card surfaces |
| `--white` | `#ffffff` | Primary text |
| `--steel` / `--steel-dim` | `#9a9ea6` / `#767a82` | Secondary/tertiary text (WCAG AA-checked against black) |
| `--blue` | `#00E5FF` | Primary accent — neon signature, used for links, primary CTAs, and hover states |
| `--copper` | `#C08552` | Secondary accent — reserved exclusively for the Legacy/Obsidian tier and the coach banner. Never combined with blue in the same element |

**Type**
- Headlines (`h1`, `h2`): **Clash Display**, loaded from Fontshare
- Everything else: **Inter**, weights 300–900

**Spacing scale:** `4 / 8 / 16 / 24 / 40 / 64 / 96 / 140px`, applied via CSS custom properties for consistency across sections.

---

## Accessibility & Performance Notes

- All body text colors verified at 4.5:1+ contrast against the base background.
- Visible `:focus-visible` outlines on every interactive element for keyboard navigation.
- `prefers-reduced-motion` is fully respected — disables the cursor glow, the scroll-scrubbed hero sequence (falls back to a static final frame), and floating particles.
- The one real `<img>` element below the fold uses `loading="lazy"`.
- Favicon, meta description, and Open Graph tags are included for link previews.

---

## Known Limitations / Next Steps

- **Images are currently base64-embedded** for portability as a single shareable file. Before production deployment, convert to properly hosted, optimized WebP assets with responsive `srcset`.
- **Three Experience cards still lack real photography** (Performance Lab, Recovery Chamber, Community Lounge) — currently placeholder dark tiles.
- **Trainer cards use initials, not headshots** — swap in real photos once available (same lens/lighting recommended for visual consistency).
- **No backend** — membership signup, coaching booking, and dashboard functionality are intentionally out of scope for this pass; this file is front-end only.
- Horizontal-scroll "bento" mechanic for the Experience section was implemented as a scroll-snap rail rather than a full GSAP-horizontal-scroll-hijack — a reasonable trade-off for performance and simplicity, worth revisiting if a more dramatic interaction is desired later.

---

## File Structure

This is intentionally a **single HTML file** — all CSS, JS, and image assets live inline. No build process, no dependencies to install, no `node_modules`. Just open it.

---

## Credits

Design, copy, and front-end build assembled iteratively with Claude. Photography sourced from AI-generated reference images, cropped/retouched to remove generation artifacts before use.