# Minimal notebook

Study-notes feel: white ruled paper with a red margin line, clean bold sans
headlines, yellow highlighter, handwritten annotations and arrows, a sticky
note or two. Best for concepts explained to students and cheat sheets.
Template: `templates/minimal-notebook.html`

## Tokens

| Token | Value |
|---|---|
| Paper | `#FFFFFF` |
| Ruled lines | `#E3EAF3`, 2 px every 56 px |
| Margin line | `#F2A7A7`, 3 px vertical at x = 110 px |
| Ink | `#16181D` |
| Pen blue (accent) | `#2453D6` |
| Highlighter | `#FFE66B` |
| Sticky note | `#FFF3A3`, shadow `0 12px 24px rgba(0,0,0,0.10)` |
| Muted | `#5B6270` |

Fonts (Google Fonts): **Inter** 500/700/800 (headlines + body),
**Caveat** 600/700 (handwritten notes, counter, footer).

```css
background-color:#FFFFFF;
background-image:
  linear-gradient(90deg,transparent 109px,#F2A7A7 109px,#F2A7A7 112px,transparent 112px),
  repeating-linear-gradient(#FFFFFF 0 54px,#E3EAF3 54px 56px);
```

Content starts right of the margin: left padding 150 px, right 80 px.

## Components

- **Header:** handle Caveat 700 40 px pen blue, top-left at x 150; counter Caveat 700 40 px `p. 2/8` top-right.
- **Headline:** Inter 800 88–110 px, letter-spacing −3 px, line-height 1.0, ink.
- **Highlight:** wrap key words in
  `background:linear-gradient(transparent 58%,#FFE66B 58%,#FFE66B 92%,transparent 92%)` with 0 6 px padding.
- **Handwritten note:** Caveat 700 48–56 px, pen blue, rotated −3°, with a hand-drawn
  SVG arrow (single `path`, stroke 4 px, round caps) pointing at the thing.
- **Numbered point:** Caveat 700 64 px pen-blue number + Inter 500 38 px text.
- **Circled word:** inline SVG ellipse, stroke pen blue 4 px, behind the word.
- **Sticky note:** butter `#FFF3A3`, square corners, rotated 2–4°, Caveat 44 px ink. One per slide max.
- **Code:** Inter is fine for prose; commands in a light box `#F4F6FA`, radius 12, monospace 32 px.
- **Footer:** Caveat 700 46 px "turn the page →" bottom-right.

## Cover recipe

Small Caveat note at top ("study notes") → huge Inter 800 headline with one highlighted phrase →
handwritten subline with arrow → sticky note with "8 slides · save it".
Keep lots of white space; this style lives on restraint.
