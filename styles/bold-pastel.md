# Bold pastel

Scroll-stopper: each slide is one big flat pastel colour, giant tight
grotesque type, chunky rounded white or ink cards. No texture. Best for hot
takes, myths vs facts, single big numbers.
Template: `templates/bold-pastel.html`

## Tokens

| Token | Value |
|---|---|
| Lavender | `#CDB8FF` |
| Mint | `#B8F2D6` |
| Peach | `#FFC9A8` |
| Butter | `#FFE98A` |
| Sky | `#B9DCFF` |
| Ink | `#1A1530` |
| Card | `#FFFFFF` or ink, radius 48, no shadow |
| Soft ink | `rgba(26,21,48,0.72)` for secondary text |

Font (Google Fonts): **Bricolage Grotesque** 500/700/800.
Headlines 800, letter-spacing −4 px, line-height 0.92.

## Colour rhythm

Cover = lavender. Then rotate mint → peach → butter → sky → lavender…
CTA slide = ink background with a butter card. Never two neighbours the same colour.
All text is ink (or white on ink) — pastels never carry text colour.

## Components

- **Header:** handle Bricolage 700 34 px ink top-left (x 72, y 60); counter top-right — row of
  N dots, 14 px, ink at 25 % opacity, current dot solid ink and 40 px wide pill.
- **Headline:** Bricolage 800 120–160 px, ink, max 3 lines.
- **Giant stat:** Bricolage 800 260–320 px ink, label 40 px below.
- **Myth / Fact pair:** two rounded cards — white card labelled `MYTH` (ink pill, white
  700 28 px), ink card labelled `FACT` (butter pill, ink text), body 40 px.
- **List card:** white, radius 48, padding 44; items Bricolage 500 40 px separated by
  2 px `rgba(26,21,48,0.12)` lines; number in 700.
- **Sticker blob:** one inline SVG blob/star 200–260 px in a neighbouring pastel,
  half off the edge, behind text. Decorative only.
- **Pill:** ink fill, white Bricolage 700 32 px, radius 999.
- **Footer:** ink pill "swipe →" bottom-right (x 72 from edge, y 64).

## Cover recipe

Lavender ground → blob top-right → headline (3 short lines, one word in a white
pill-highlight `background:#FFFFFF; border-radius:24px; padding:0 18px`) →
40 px subline → two ink pills → swipe pill.
